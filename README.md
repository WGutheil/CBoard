# CBoard
Matlab program to analyzed checkerboard data for synergistic antibiotic combinations
README file for CBoard

CBoard is a MATLAB program for the analysis of checkerboard data. From the to be submitted manuscript:

ABSTRACT
This study presents a checkerboard data analysis approach using a Hill  function (y = 1/(1+(x/K)n) to fit each column and row of checkerboard assay data. Column fits give a K (MIC) value in units of row concentration for each column antibiotic concentration (MIC_row vs [Col]), and row fits give an MIC_col value for each row antibiotic (MIC_row vs [Row]). Since the corresponding row and column concentrations are themselves MICs, this provides two sets of MIC vs MIC data pairs which can be plotted together as an isobologram. These MIC_A vs MIC_B values can be subjected to a second round of Hill function fitting, separately in x-y and y-x directions. Finally, a fit based on overlapping Hill functions is developed that allows x-y and y-x dimension fits to be performed simultaneously. Formula for fractional inhibitory concentrations (FICIs) as a function of fit parameters, and other features of these curves, are derived. This analysis also provides “n” (steepness) values from column and row fits, which are themselves dependent on the other antibiotic concentration and can be exceptionally, as in the case of ceftobiprole alone (n>10). This synergistic checkerboard analysis approach is implemented in MATLAB, which performs the fits and provides statistics variable values and alternative models significance. 

To run CBoard on demonstration files:

1) Unpack ZIP files to chosen location.

2) Open MATLAB.

3) Navigate to "0. CBoard_v1" directory in Matlab.

4) Open the "A_CBoard.m" file. This is a MATLAB script that runs the analysis. It will can process multiple data files, or multiple data sheets within one file, or a combination of both.

5) Navigate up one directory in MATLAB, and add the "0. CBoard_v1" directory to the Matlab path (right click for this option).

6) To process the example data file used in the main text of the paper navigate down to the "1. Example 1_8_8x11" directory, and run the "A_CBoard" script from the MATLAB command window.

7) To process the extra example data files navigate to the "2. Example 2_Cefto_Data" directory and run the "A_CBoard" script from the MATLAB command window.


Notes of data file syntax:
See the example data files and follow their syntax.
A1 contains the antibiotic name and concentration serially diluted down the plate. The format is "IDX_(units)" or "IDX (units)". Keep this short to avoid Matlab table variable length problems.
A2 contains the antibiotic name and concentration serially diluted accross the plate in the same format.

Row 4 starting in A4 and going down contains the A1 associated concentration values.
B3 and across contains the A2 associated concentration values.

Variable checkerboard data sizes are automatically accommodated. Replicate plate analyses are not currently supported. We perform checkerboards in triplicate, and average the plate results prior to running CBoard, Eventually replicate analysis will be added.

