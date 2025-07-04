## FRB20240114A_Python_Scripts
This repository holds the python scripts used for processing and analysing UBB observations of FRB20240114A conducted with Effelsberg.

## Usage of the Scripts:
# 1) batch_plotter_13May2025.py:
This script gets burst archives from a single band of UBB and plots dynamic spectra and temporal flux profile. The archives should be flux calibrated otherwise, the logic to plot the timeseries needs to be changed for eg. if you want to plot S/N. The script also performs reduced chi-square minimizing multigaussian fitting to the bursts and computes the burst properties as mentioned in Limaye et al. 2025. Since the default archives are 1-second long, there may be more than one burst in a single archive. The script handles this by using the logic of overlaps between the gaussian fits to each profile in order to give independent results for independent bursts and same result for burst with sub-components respectively.
# 2) Band1_2_burst_properties.py:
This script is specially designed to combine any two consecutive, continuous bands of the UBB receiver. The purpose of the script is to compute the burst properties of the events overlapping between these two bands.
# 3) Band2_3_burst_properties.py:
This script is specially designed to combine Band2 and Band3 considering the gap between the two. The purpose of the script is to compute the burst properties of the events overlapping between these two bands.
# 4) Full_UBB_Plotter.py:
This script combines all the UBB bands considering the band gap in order to produce broadband burst spectra. The spectra can be produced using different zoom-in windows around the burst as follows:\
1s window : 1023 samples\
100ms window : 102 samples\
10ms window : 20 samples
