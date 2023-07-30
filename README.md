# Google Data Analytics Capstone Project Case Study 1

## Ask
* Problems to solve:
   1. How do annual members and casual riders use Cyclistic differently?
   2. Why would casual riders buy Cyclistic annual memberships?
   3. How can Cyclistic use digital media to influence casual riders to become members?

* ### Identify business task and Consider key stakeholders

  * **Business Task**: We are trying to encourage more casual riders to take up the annual membership.
  * Insights generated from this would help to determine what methods would attract casual riders to purchase the annual membership.
  * **Key stakeholders** in this business task include 1) casual riers, 2) Lily Moreno(Director of Marketing), 3) Cyclistic Marketing team, 4) Cyclistic Executive team

## Prepare
* Data sources
  * [Data used](https://divvy-tripdata.s3.amazonaws.com/index.html)
  * [Data license](https://ride.divvybikes.com/data-license-agreement)
  * Downloaded trip data from 2019 Q2 to 2020 Q1
* The data is likely to be in United States
* THe data is organised by Ride ID, type of bike, start and end timings, start and end station names, station IDs and station latitudes and longtitudes, as well as member type.
* As the data come from the company managing the service, it is **Reliable**, **Cited** and **Original**. The data has all the critical information of member type and length of ride, making it **Comprhensive**. The data used in this analysis is the most **Current** available.
* Data integrity is ensured by standardising the columns available for use throoughout the 12 month period investigated.

## Process
* The first tool I would use would be Excel to fill up those empty cells with 'NIL' to avoid having empty cells.
* I would also use SQL to select wrong data types that could have been inside the dataset to have a consistent data type in the column, ensuring data integrity.
* *Steps Taken*
   * Included column of "ride_length" to determine length of rides by converting date time data into 'hh:mm:ss' format
   * Included column of "day_of_week" to determine which day the ride took place, with 'Monday' being 1 and 'Sunday' being 7

## Analyze
* I should hide rows that are not relevant to this analysis such as 'ride_id'
* Checked formatting by using the 'Filter' function to ensure no empty cells are involved in the 'started_at', 'ended_at' and 'member_casual' columns as these 3 are the crucial part of analysis
* One surprise in the data was that some points had the 'statrted_at' time being later than the 'ended_at' time, which does not make sense.
* Create a pivot table to have a better understanding of the data
* ![image](https://github.com/dtwl0401/gdc1/assets/107090466/05233dac-757d-4ee3-90e8-1133088fa3f0)
* **Type of member vs Average ride length**
* ![image](https://github.com/dtwl0401/gdc1/assets/107090466/424d043b-6a1d-4908-867e-e7a64047f896)
* **Type of member vs Average ride legnth with Day of week**

## Share
* Casual members have higher average ride length as compared to members in 2020 Q1
* Casual riders may actually benefit from becoming members due to longer ride times
* The casual riders can receive in-app notifications when to open the app to offer them member, or through email to encourage them to pickup membership
* A table with days of week as x-axis, where each day has two columns of average member ride length and average casual ride length to see the difference between the averages for both parties
   ### Steps taken
   1. Load dataset from 2019 Q2 to 2020 Q1 into R environment, naming it *'q2_2019'* and so on.
   2. Run 'colnames(dataset)', where dataset is *'q2_2019'* and so on, to check all columns in all four datasets are the same
   3. Column names for Q2 2019 was different from others, so we would have to change it to standardize all the column names to be the same
   4. The data type for 2019 are different, so we mutate it
   5. Combine all 4 quarters worth of data into one data frame
   6. 
