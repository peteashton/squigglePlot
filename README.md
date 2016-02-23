## squigglePlot

Python program to draw a squiggle plots of the event data from one or more nanopore FAST5 files

The Oxford Nanopore Technologies MinION system produces long read DNA sequence data using nanopore technology.  
The raw data from each sensor on the chip is a stream of current measurements which vary as the DNA strand passes
through the pore.  During this process, the MinKNOW software records the different current levels and the 
times that they persist before the current changes (as the 5-6 bases in the pore move forward). 

This data is stored as events in the FAST5 file that MinKNOW produces for each strand that is sequenced. 
For each event, the start time, length, mean current level and standard deviation are stored.  The FAST5 file
is then passed by Metrichor to the cloud where basecalling is performed.  

This program allows the visualisation of the event data for one or more FAST5 files. These can either be displayed 
as distinct processes (so the x-axis is the time since the strand was first recognised as being present in the
pore, or on a common time axis, so that e.g., all of the strands sequenced by a single pore can be viewed in order.

