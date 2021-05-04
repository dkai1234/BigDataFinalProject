# BigDataFinalProject
This repository is for the final project of ME-5013, Big Data Analytics in Extreme Environments

The purpose of this project is to demonstrate the course objectives of handling and analysing large datasets through the use of Python libraries.
The data chosen for this purpose is calculated values of pressure, temperature, and normalized column density for carbon monoxide (C0) from the
exhaust of a rotating detonation engine (RDE) while under operation.  The data sets are representative of 4 separate runs of the RDE under varying
equivalence ratios and mass flow rates.  The author of this project has hypothesized that there is a correlation between the amount of CO generated
and these two quanities and that correlation is detectable within the given data.

Introduction
Laser spectroscopy data was taken from a series of experiments conducted at the Air Force Research Laboratory’s (AFRL) Rotating Detonation Engine (RDE) facility.[1]  The purpose of this project is to utilize this data to establish a relationship between the carbon monoxide column density, equivalence ratio (ratio of the actual fuel-oxidizer mixture, and the stoichiometric ratio), and combined mass flow rate of the fuel and oxidizer.  Several Python modules will be used for this analysis.  This project proposal represents a basic outline for the work that will be conducted on the data found in the link above and the subsequent analysis.  A copy of the works already conducted on this dataset (see Reference [1]) can also be found in the file.
    
Data Scope
The data collected has been processed from photodetector voltage signals being triggered by the light from a quantum cascade laser that has passed through the exhaust gases of a RDE while operating.  The raw data is available; however, the original team worked for several months to develop the processing code for said data.[2]  As such, it would be outside the scope of this project to scrub and process the raw data accordingly by generating an original code.  The processed data consists of temperature, pressure, and normalized carbon dioxide column density for each test, taken at 250 or 500 million samples per second for 1.0 and 0.5 second test durations, respectively.  The mass flow rate and equivalence ratio are constant parameters for each test and, thereby, are not a part of the collected data.  All necessary information for test setup and methodology have been prepared in the referenced works.  
    
Each dataset will require extensive comparison within each test series to determine linearity between data points.  The nature of a RDE is such that a detonation wave passes the sensor at a minimum frequency of 13.5 kHz.  As such, there are several cycles worth of data within each test that will need to be averaged, compared, and analyzed.  The data sets will be incorporated and isolated as separate data frames using the Pandas python library to make accessing separate time windows easier.  Plotting of the data using the Matplotlib library in Python will be necessary for the purposes of visualizing the comparisons.  Furthermore, it is proposed that a python software suite called Cantera be used to create a numerically simulated solution of the test data for comparison.[3]  

Conclusion
It is believed by the author that the works outlined herein offer an exceptional opportunity for furthering understanding of the capability and application of Python libraries in the use of Big Data analytics.  By conducting this analysis, an extensive code will need to be produced that can examine this data in an original way.  Although work has already been completed on these figures, there has been no work conducted along the scope of what is proposed here.

References
[1]	A. P. Nair, C. Jelloian, D. S. Morrow, F. A. Bendana, D. I. Pineda, and R. M. Spearrin, “MHz mid-infrared laser absorption sensor for carbon monoxide and temperature behind detonation waves,” in AIAA Scitech 2020 Forum, 2020, no. January.
[2]	A. P. Nair et al., “MHz Laser Absorption Spectroscopy via Diplexed RF Modulation for Pressure, Temperature, and Species in Rotating Detonation Rocket Flows,” Appl. Phys. B, vol. 126, no. 8, p. 138, Aug. 2020.
[3]	B. Franzelli, J. Rocchi, P. Wolf, A. G. Coriolis, and T. Cedex, “Cantera tutorial-V2.1,” pp. 1–55, 2010.

