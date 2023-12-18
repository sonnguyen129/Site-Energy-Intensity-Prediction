# Site Energy Intensity Prediction

## Introduction

The dataset consists 100k observations of building energy usage records collected over 7 years and a number of states within the United States. It is about building characteristics (e.g. floor area, facility type etc), weather data for the location of the building (e.g. annual average temperature, annual total precipitation etc) as well as the energy usage for the building and the given year, measured as Site Energy Usage Intensity.

We use the trained models to compute this variable for each row of the test dataset and evaluate the models in terms of the Root Mean Square Error, which is defined as a scaled version of the L2-distance between the vector of predicted values and the vector of true values of the target variable in the test dataset.

## Data Overview

- year_factor: anonymized year in which the weather and energy usage factors were observed
- state_factor: anonymized state in which the building is located
- building_class: building classification
- facility_type: building usage type
- floor_area: floor area (in square feet) of the building
- year_built: year in which the building was constructed
- energy_star_rating: the energy star rating of the building
- elevation: elevation of the building location
- january_min_temp: minimum temperature in January (in Fahrenheit) at the location of the building
- january_avg_temp: average temperature in January (in Fahrenheit) at the location of the building
- january_max_temp: maximum temperature in January (in Fahrenheit) at the location of the building

Similarly for all other months

- cooling_degree_days: cooling degree day for a given day is the number of degrees where the daily average temperature exceeds 65 degrees Fahrenheit. Each month is summed to produce an annual total at the location of the building.
- heating_degree_days: heating degree day for a given day is the number of degrees where the daily average temperature falls under 65 degrees Fahrenheit. Each month is summed to produce an annual total at the location of the building.
- precipitation_inches: annual precipitation in inches at the location of the building
- snowfall_inches: annual snowfall in inches at the location of the building
- snowdepth_inches: annual snow depth in inches at the location of the building
- avg_temp: average temperature over a year at the location of the building
- days_below_30F: total number of days below 30 degrees Fahrenheit at the location of the building
- days_below_20F: total number of days below 20 degrees Fahrenheit at the location of the building
- days_below_10F: total number of days below 10 degrees Fahrenheit at the location of the building
- days_below_0F: total number of days below 0 degrees Fahrenheit at the location of the building
- days_above_80F: total number of days above 80 degrees Fahrenheit at the location of the building
- days_above_90F: total number of days above 90 degrees Fahrenheit at the location of the building
- days_above_100F: total number of days above 100 degrees Fahrenheit at the location of the building
- days_above_110F: total number of days above 110 degrees Fahrenheit at the location of the building
- direction_max_wind_speed: wind direction for maximum wind speed at the location of the building. Given in 360-degree compass point directions (e.g. 360 = north, 180 = south, etc.).
- direction_peak_wind_speed: wind direction for peak wind gust speed at the location of the building. Given in 360-degree compass point directions (e.g. 360 = north, 180 = south, etc.).
- max_wind_speed: maximum wind speed at the location of the building
- days_with_fog: number of days with fog at the location of the building
- building_id: building id

Target variable
- site_eui: Site Energy Usage Intensity is the amount of heat and electricity consumed by a building as reflected in utility bills

**Dataset structure:**

*Training data synopsis:*

- Number of observations: 85462
- Number of columns: 64
- Number of integer columns: 37
- Number of float columns: 24
- Number of object columns: 3
- Number of duplicate observations: 0
- Constant columns: None
- Number of columns with missing values: 6
- Columns with missing values: year_built, energy_star_rating, direction_max_wind_speed, direction_peak_wind_speed, max_wind_speed, days_with_fog


*Test data synopsis:*

- Number of observations: 85462
- Number of columns: 64
- Number of integer columns: 37
- Number of float columns: 24
- Number of object columns: 3
- Number of duplicate observations: 0
- Constant columns: year_factor, days_above_110F
- Number of columns with missing values: 6
- Columns with missing values: year_built, energy_star_rating, direction_max_wind_speed, direction_peak_wind_speed, max_wind_speed, days_with_fog

The training set contains information of six years (year_factor = 1 to year_factor = 6) and the test set contains information of the seventh year (year_factor = 7)






