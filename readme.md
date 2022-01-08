# Using Machine Learning in Structural Health Monitoring 

The dataset (Source of the dataset: https://zenodo.org/record/3745914#.YdoIVWDMJD-) used in our study was collected from structural health monitoring of a steel bridge in
Leuven, Belgium known as railway bridge KW51. KW51 is a bow-string bridge that is 12.4m
wide and 115m long consisting of two ballasted electrified tracks (A and B). To correct a
construction error, the connections of the diagonals to the arches and the bridge deck were
strengthened by retrofitting. The data was collected from October 2018 to Mid-January 2020,
and retrofit happened from May 15th to September 27th, 2019. Twelve uniaxial PCB 393B04
type accelerometers were installed on the bridge deck and the Arches to measure acceleration.
Similarly, 12 uniaxial micro-measurements CEA-06-250UN-350 type strain gauges were
installed on the bridge deck and the diagonal members to measure strain values. Both the
accelerometers and strain gauges were programmed to collect data during the train passage
two times a day. Detailed layout of accelerometers and strain gauges is shown in Figure below.   

![fig 1](https://user-images.githubusercontent.com/96390333/148661439-db786076-62da-4352-9f5f-327657e173c1.jpg)


The environmental conditions like average air temperature, average relative humidity, average vapor
pressure, average global radiation, average diffuse radiation, average direct normal radiation,
total rain, average wind speed and direction at 10m above ground were also measured as daily
average values. The data corresponding to a single train passage are stored in a separate file
with MATLAB .mat file format. The filenames are named as
“traindata_yyyymmdd_HHMMSS.mat”, where yyyymmdd_HHMMSS denotes the UTS time
corresponding to the beginning of the train passage. The file structure of the provided .mat files
are given in Figure below.

![fig 2](https://user-images.githubusercontent.com/96390333/148661493-8b1a6768-c749-49fc-a4ce-99b63cde1a15.jpg)

The data provided by Maes and Lombaert was very extensive, and due to computer space
limitations, a smaller subset of data was chosen for evaluation. The strain values and
environmental data from the dataset were used to analyse the effect of retrofit on the strain. Due
to the high volume of data, values from two months, April-2019 (Before Retrofit) and
October-2019 (After Retrofit), were considered for our analysis. The plot of strain values over
time is shown in Figure below.

![fig 3](https://user-images.githubusercontent.com/96390333/148661516-ce7d4376-e6d6-4886-961b-986bef0a6720.jpg)

There were some gaps in the data, both before and after the retrofit, which were random. These
gaps were caused due to errors or malfunctions in the gauges. The lack of data from strain
gauges #9-12 after retrofit were not random as these strain gauges were not in operation at that
time. The missing points in the dataset were removed by the process of averaging the strain
values. The strain gauges for the data analysis were selected based on their location at which
they were attached on the bridge. Since the gauges are measuring lateral strain, the strain
gauges in a single line at varying distances across the bridge were selected.
Five strain gauges (green) on line A of the bridge in Figure 1 were selected and a variable to
account their position was added to the analysis. The variable (lx) is the distance of the strain
gauge from the origin assumed at the left of the bridge (point A). Figure 4 shows the plot of
averaged strain values for the selected strain gauges.
The values for the variable lx (in m) for the strain gauges are given below.
Strain_1: lx = 34.141 m
Strain_2: lx = 48.516 m
Strain_3: lx = 59.297 m
Strain_5: lx = 80.859 m
Strain_8: lx = 95.234 m

Plot of averaged strain values during the months April-2019 and October-2019 is shown in the figure below,

![fig 4](https://user-images.githubusercontent.com/96390333/148661534-cfab4ae8-6e3b-4fcd-afc8-09b364c71985.jpg)

## The process of Exploratory Data Analysis and creation of regression model is provided in the jupyter notebook.

# References
-- Al-Khateeb, H. T., Shenton, H. W., Chajes, M. J., and Aloupis, C. (2019). “Structural
Health Monitoring of a Cable-Stayed Bridge Using Regularly Conducted Diagnostic Load
Tests.” Frontiers in Built Environment, 5.  
-- Brenner, B. R., Sanayei, M., Bell, E. S., Rosenstrauch, P. L., Pheifer, E. J., and Marr, W. A.
(2011). “The Influence of Temperature Changes on Bridge Structural Behavior.”
Cook, W. (2014). “Bridge Failure Rates, Consequences, and Predictive Trends.”
dissertation, Utah State University, Logan, UT.  
-- FPrimeC. (2019). “Structural Health Monitoring for Bridge Structures.” FPrimeC Solutions
Inc., <https://www.fprimec.com/structural-health-monitoring-for-bridge-structures/>.
Gaba, H., Singh Rai, H., Singh, S. P., and Singh, H. (2011). “Health Monitoring and
Retrofitting of Structures-A Review.” International Journal of Earth Sciences and
Engineering, 04, 681–683.  
-- Lee, Y.-S. (2007). “Development of a Structural Health Monitoring System for Bridges and
Components.” dissertation, Iowa State University, Ames, IA.  
-- Maes, K., and Lombaert, G. (2021). “Monitoring railway bridge KW51 before, during, and
after retrofitting.” Journal of Bridge Engineering, 26(3), 04721001.  
-- Svendsen, B. T., Frøseth, G. T., Øiseth, O., and Rønnquist, A. (2021). “A Data-Based
Structural Health Monitoring Approach for Damage Detection in Steel Bridges Using
Experimental Data.” Journal of Civil Structural Health Monitoring.  
