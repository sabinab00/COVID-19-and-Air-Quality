# Exploring the Relationship between COVID-19 and Air Quality in NYS

# Advanced Visualization Tools - Final Project

## Introduction
Research shows that the cease of social and economic activities due to the pandemic had resulted in improved air quality and decreased water movement in 2020. This project aims to portray the correlation between the number of cases and the air quality in NYC from January 2020 to December 2020. 

## Methods
After downloading all datasets, open Tableau (version ```2021.4``` was used in this project). Connect the ```covid_cases.csv``` dataset to all the AQI datasets for each pollutant using ```Date``` and ```County``` as the relationships.

### Dashboard: Cases Map
In the ```Cases Map``` dashboard, a map of the COVID-19 confirmed cases per county was created using ```county``` as a geo dimension. ```Sum of Confirmed Cases``` was used as a mark via a red hue: the paler the county, the fewer cases it has, and the darker the county, the more cases it has. ```County``` and ```Month``` were utilized as filters, so that users could choose which county or month to see in a dropdown menu on the ```Cases Map``` dashboard. The map automatically changes to show the information based on their preferences.

### Dashboard: AQI Map
To create the ```AQI Map``` dashboard, several worksheets were used. Each sheet contained the AQI information on a map for each pollutant. This was done to show the pollutant-specific data for each county that was included in their respective dataset, since not every county was measured for each pollutant. In each sheet, a map
of NY was generated using ```county``` as a geo dimension. The AQI value was changed to ```average``` instead of the default ```sum```, since the average values would better represent the data. The AQI values for each respective pollutant was utilized as mark via color. ```Month``` and ```County``` were used as filters so that users could have the option to choose which information to see, similar to the ’Cases Map’ dashboard. Another dimension was added as a filter: ```Display Sheet.``` This filter was generated by creating a parameter, in which the respective sheet was added as an option. This was repeated for the other pollutants and their respective sheets as well, so that the ```Display Sheet``` filter dropdown menu in the dashboard would contain seven options: ```All```, ```CO```, ```NO2```, ```Ozone```, ```PM2.5```, ```PM 10```, and ```SO2```. Thus, the different pollutants could be seen in one dashboard, and users have the option to select a specific pollutant’s sheet to view its corresponding AQI values for each county.

### Dashboard: AQI Per County
A third dashboard, ```AQI per County``` was created to illustrate the average AQI values of all pollutants per county. Three sheets were constructed to represent three views of the data: map view, bar graph view, and scatter plot view. In the ```Map``` sheet, ```County``` was used to generate a map view, and the AQI values of all the pollutants were utilized as marks so that the information for each pollutant’s air quality level would be displayed on the map. For the ```Bar``` sheet, ```Month``` was set as the column values, while ```Measure Values``` was set as the row values. The AQI values of all the pollutants were used as measure values. Like the ```Map``` sheet, ```Month```, ```County```, and ```Display Sheet``` were utilized as filters. The ```Scatter``` sheet contained ```County``` as the column values and ```Sum of Positive Cases``` as both the row values and measure values. As a measure value, the positive cases was set as an orange-red color mark to signify caes from low to high counts. The AQI values of all the pollutants were also used as measure values. For all the sheets/visualizations, ```County``` was set as a filter, as well as ```Display Sheet```, using a parameter which was generated using the respective sheet (```Map```, ```Bar```, ```Scatter```), similar to the ```AQI Map``` dashboard. This would allow users to choose which visualization of the data they wanted to view. Stories were created from each dashboard.

### Dashboard: AQI vs Case Count
The number of cases and average AQI values for each month in 2020 were set side by side in six bar graphs from six sheets as seen in the dashboard. These six sheets were created using the parameter ```Select a Pollutant``` as a filter, following the same steps in creating the ```AQI Map``` dashboard above. Blue was used to signify the AQI values, while red illustrated the count of cases. For each bar graph, the AQI value for each pollutant was used as a row value and marked with a blue color. 

## Visualizations
Stories were created from the dashboards generated. The dashboards containing all visualizations can be donwloaded from this repository (```Cases vs AQI.twb``` and ```AQI Per County.twb```) or accessed via the links below:

https://public.tableau.com/app/profile/sabina.bhuiyan6947/viz/shared/GCKNW2GHJ
https://public.tableau.com/app/profile/sabina.bhuiyan6947/viz/AQIDataPerCounty/AQIperCounty

## Conclusions
Results vary for the pollutants visualized; the decreased AQI values for CO, NO2, PM 2.5, and PM 10 pollutants indicate that the air quality improved in Manhattan during the time period that restrictions took place in NYC in 2020. However, the opposite is true for the AQI levels for ozone and SO2. Further research could be conducted to explore why this was the case, as well as to determine the relationship, if any, between air quality and case rate in regards to poverty rates, population size, etc.


