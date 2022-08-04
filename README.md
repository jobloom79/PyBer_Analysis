# PyBer_Analysis
## Rideshare analysis
### Overview of Project:
---An analysis to compare ride-sharing data by city type was conducted to determine any disparities in the service provided and recommend any improvements.
### Analysis and Challenges:
#### Deliverable 1: Create a ride-sharing summary DataFrame by city type
---In order to create the ride-sharing summary the raw data was pulled into pandas using "jupyter notebook". The 'read.csv' and 'merge 'function was ran on the ride data and city data using "city" as the common key. This allowed for a new dataframe to be created, using the groupby function paired with count and sum function allowed us to retrieve the following:
##### o total number of rides for each city type
##### o total number of drivers for each city type
##### o total sum of the fares for each city type
##### o average fare per ride for each city type
##### o average fare per driver for each city type
Finally the summary Dataframe was created and formated as shown in the figure 

![Ride_Share_Summary](https://github.com/jobloom79/PyBer_Analysis/blob/main/analysis/Ride_Share_Summary.PNG)

#### Deliverable 2: Create a multiple-line chart of total fares for each city type
---This deliverable was extremely challenging to put into a pivot and index. The first step to getting a multiline chart by total fares is to create a dataframe with multiple indices based on the filters being requested. Using pandas we can take the "groupby()" function on type and date columns of the original dataframe created with the merge data and "sum()" function on the fare column. Once the dataframe is created the index is reset and the pivot is used. This is where the challenge came in getting the pivot to read the "date" key. As a result the original dataframe was filtered using the loc method with a date range from "1-1-2029 to 4-28-2019" and put into a new dataframe and indexed to a datatime data type. Once done a new pivot was created to re-aggregate and "resample" the data into weekly bins and summed to get total fares per week as shown in the multi-line chart below. 

![PyBer_fare_summary](https://github.com/jobloom79/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.PNG)

### Results: 
---When comparing the data from the summary dataframe and chart we can see there are more rides in the urban areas and significanly more drivers in the amount of roughly 5 times the drivers. While there are more drivers the number of rides between urban and suburban is less than 3 times a difference. There is also a skew of numbers for the average cost of the ride per driver in rural and the other city types.
### Summary: 
---After reviewing the data the recommendations to V. Isualize for addressing the disparities among the city types are as follows:
##### 1. Allocate drivers from urban areas to rural in order to create more of a supply scenario and allow for more of a distribution to prevent any price gouging and potentially increase demand with affordable fares.
##### 2. Ramp up the amount of drivers across the board near the end of February to accomodate the increase in demand in all areas. This most likely coincides with an event like Spring break for college students and gives opportunity for more revenue.
##### 3. Offer incentives for the ride-share program throughout the year to increase overall demand and revenue.