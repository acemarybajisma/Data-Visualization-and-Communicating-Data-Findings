# Data-Visualization-and-Communicating-Data-Findings
This projects focused on data cleaning, data visualization and data findings communication of Ford GoBike Dataset
# (Ford GoBike Data Exploration)
## by (Ace Mary Bajisma)


## Dataset

The name of this dataset is FordGoBike which was gotten from the Udacity Classroom. The data set initially contained 183412 rows and 16 columns before wrangling, 9 of which were numerical in nature and 7 were strings. The dataset contained individual attributes of bike trips.
The first thing done was to import all necessary packages and load the dataset. I then dropped all unnecessary columns from the dataset that were not needed for my analysis which included start_station_id, start_station_latitude, start_station_longitude, end_station_id, end_station_latitude and end_station_longitude. After this was done, I noticed that the data type of some colums were not in the right type which I changed. I cahnged the member_birth_year column data type from float to integer and the start_time and end_time columns datatype from object to datetime. I noticed that there were some rows with null values in the columns start_station_name, end_station_name, member_birth_year and member_gender which I dropped using the pandas dropna function. I used the pandas striftime function in the date module to extract the date, hour, month and week day from the start_time column. I checked for the number of unique start station and end station names in the dataset using pandas nunique function. After performing these wrangling steps, the number of rows in the dataset became 174952 and the columns became 14 (3 numeeicaland 11 strings). The cleaned copy of the dataframe was then stored in a csv file named FordGoBike_cleaned.csv to be used for the presentation.


## Summary of Findings

Below are the findings discoverd from exploration:

-From the distribution of trip duration, it was discovered that most of the durations are less than 2000 seconds with the peak around 600-700 seconds.
-The number of users that were subscribers were more compared to the users that were customers with a total of 90.5%.
-Male had the highest percentage count in the dataset with a total of 74.6%.
-Market St at 10th St station was the start station that passengers entered from the most with a total of 3649.
-San Francisco Caltrain Station 2 (Townsend St at 4th St) station was the end station that passengers alighted from the most with a total of 4624.
-The category with no bike share for all trip was high in percentage with a total of 90.1% compared to the ones with bike share.
-The peak age was around 35 years and there was an inverse relationship between an increase in age and the count (As the age increased, the count reduced).
-There were more trips on Thursdays compared to other week days with a total of 33712.
-Users that were subscribers spent lesser time in their trips compared to the users that were customers by almost twice.
-Gender didn't have any effect on the trip duration. The median from the violin plot seemed the same for all the gender categories which is about 500 seconds.
-Bike share didn't have any effect on the trip duration. The median from the violin plot seemed the same for whether there was bike share or not which is about 500 seconds.
-The gender in the other category spent more time in their trips on Sundays.
The female customers spent the highest time in their trips while male subscribers spent the lowest time in their trips.


## Key Insights for Presentation

-I started with a histogram visual to depict the distribution of the trip duration on a logarithmic scale.

-Next was a histogram visual showing the distribution of age across the dataset on a standard scale.

-Then I depicted a bar chart to show the week day that had the highest trip. This showed that there were more trips on Thursdays compared to other days. This might be because of an event that takes place every Thursdays.

-I then presented a violin plot to show the relationship between the trip duration and user type. This gave a clear understanding of the fact that lesser time was spent on trips from subscribers than customers.

-Finally I presented a clustered bar chart to show the relationship between trip duration and gender based on the user types. This showed that the female customers spent the highest time in their trips while male subscribers spent the lowest time in their trips.
