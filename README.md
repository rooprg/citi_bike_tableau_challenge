**CITI BIKE VISUALIZATIONS & ANALYSIS**

This challenge includes generating reports and analysis for city officials to help boost New York City's Citi Bike program.
Using program data housed on their System Data website (https://citibikenyc.com/system-data) for the past decade plus on bike utilization, I have generated visualizations, dashboards, and a story via Tableau, plus documented my analysis of the data used.


**(1) Data:**

I have used 2022 monthly data from Jersey City, New Jersey, which also includes certain data outside New Jersey (e.g., stations in Manhattan where bikes were returned).
I compiled twelve months of Jersey City data into a single file for my review, visualization, and analysis. I am not able to load the master file on Git Hub due to space restrictions; however, all twelve individual .csv files are present in the “Data” folder.

Pandas library was used to compile, clean, and organize the data into a DataFrame and subsequently saved to the large .csv file mentioned above. The code for these operations is found in the “Cleaning” folder.


**(2) Visualizations:**

My visualizations (plus dashboards and story) are posted at:

(1) https://public.tableau.com/views/tableau_challenge_roop_final/OverallStory?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link on Tableau Public

and

(2) in the Outputs folder of this repository.


**(3) Questions:**

I set out to research the below questions within this exercise-

(1)  Are there any insights to be gleaned from user behavior in 2022 over the course of a full week?

(2) Are there any patterns that emerge from 2022 when season or weather is assessed that might boost bike usage?


**(4) Visualizations and Dashboards:**

For Question 1, I started by looking at the Average Rental Duration (and the Percent Difference in Average Rental Duration) over the course of the week (Sunday through Friday) for all of 2022. Each day of the week has a greater Average Rental Duration (ADR) than 3.85 minutes (min). It is interesting that Wednesday has the highest ADR at 7.41 min. I visualized this trend with this line graph:

![Behavior Change](/Output/behavior_change.png)


Interest in who might be increasing the ADR on Wednesday lead to generation of the below bar chart, where there is uniformity in the ADR for members, of which a great proportion may be commuters. There is more variability in the casual bikers, peaking on Wednesday as noted here:

![Who Are They](/Output/who_are_they.png)


If casual bikers increase the ADR for Wednesdays, perhaps we can gain insights into which type of bike that are using. The below box plot indicates that Docked Bikes have a wider variation in ADR and for the most part, ADR is equal to or greater for Docked Bikes than both Electric Bikes and Classic Bikes. Wednesday is the third highest ADR at 22.94 min, which is higher than the Median. This may indicate Docked Bikes are an important part of the Casual Biker experience. This could be leveraged to boost the program in general.

![Act Casual](/Output/act_casual.png)


I created a dashboard, Rider Behavior, to describe my progress through this question and phenomenon. Overall, looking a rider behavior, particularly stations and bike type, more vigorously may provide input on further strategies to boost program usage.

![Rider Behavior](/Output/rider_behavior.png)


As for Question 2, I continued my assessment of biker behavior with respect to seasonal and/or weather factors. The longest and shortest days (the Summer Solstice and the Winter Solstice, respectively) of the year occur 6 months apart and usually have different weather patterns.
By looking at Total Rides over the course of 2022, a line graph can be generated that meets our expectation of what weather conditions might do to bike utilization, namely arise through the Spring of the North Hemisphere; remain high through Fall; and dip when Winter arrives. This visualization denotes this trend:

![Warmer Times](/Output/warmer_times.png)


If we look at Rental Duration again, but this time in the context of a summed metric individually for 21-Jun-2022 and 21-Dec-2022, respectively, we see something that might need more investigation. As can be seen below, the Sum of Rental Duration (SRD) for 21-Dec-2022 is larger in terms of minutes than the SDR for 21-Jun-2022. With warmer conditions, we might expect for riders, particularly Casual Riders, to bike for longer periods or expect that with long days, there would be more time in the day and potentially, more bike rentals per day, leading to a larger SDR.
![Long & Short of It](/Output/long_and_short_of_it.png)


A simple table shows there are indeed more bike rides on 21-Jun-2022:

![Rides by Solstice](/Output/rides_by_solstice.png)


By drilling down into the data more and looking at the Sum of Distance (in miles) for 21-Jun-2022 and 21-Dec-2022, then partitioning the data by bike type, we might see another interesting behavioral metric:

![Electricity](/Output/electric.png)


The use of Classic Bikes and Docked bikes are similar on these two dates as noted below. Using Sum of Distance (SoD), the below stacked bar chart shows 1,174 miles for Classic Bikes on 21-Jun-2022 and 1,043 for Classic Bikes on 21-Dec-2023. These are virtually the same, as are the Docked Bikes (2 versus 9, respectively. The big difference is in Electric Bike usage, where almost a four fold difference is seen (905 versus 230, respectively). Again, this is an indicator that might lead to more evaluation and/or strategies to boost the program.


I created a dashboard, Bike Drivers, to delineate my way through this question and phenomenon. Adding availability of certain types of bikes at select stations may prompt more rides by both types of riders. It appears that electric bikes may be tied to long rides, which could be applied to both member and casual users.

![Bike Drivers](/Output/bike_drivers.png)


I generated a map to visualize where bike rides most often terminate. I appears that the stations where the most rides terminate is on the harbor side. This area is rich with transportation hubs. There are connections to trains and ferries, including a ferry that visits the Statue of Liberty. This means the potential exists for both commuters and sightseers to use Citi Bikes for work and/or pleasure, which bodes well for continued success and perhaps even boosts to rentals.

![End Stations by Zip Map](/Output/end_stations_by_zip_map.png)


**(5) Analysis and Story:**

There are many reasons for wanting the Citi Bike program to prosper, including helping to mitigate car traffic; assist with noise and air pollution; and health/exercise benefits to name a few. 

My analysis only covers 2022, but insights gained might be applicable to other years and the past decade. I’m sure you are constantly considering new approaches to ensure the continued viability of and propagation of the Citi Bike program.

My story is outlined here:

![Overall Story](/Output/overall_story.png)

Considering the above visualizations, dashboards, and story, changes in numbers of bikes at certain locations; availability of specific bike types to certain riders at certain times; and increased focus on metrics for stations at or near transportation hubs; parks; and sightseeing activities may be advantageous increasing ridership and positive feelings about the program and its benefits. Using information about what types of bike riders using specific bikes at both starting stations and terminating stations can give strategic insights on how better to deploy resources; whether new stations should be added and/or current stations should be shrunk or potentially even closed; and whether the correct mix of bikes at each station should be changed. This analysis answers some preliminary questions, but further analysis could be conducted at a granular level to support future strategic decisions. I have noted some possible directions directly below.


**(6) Next steps:**

While the scope of this analysis is narrow, additional research could be geared towards the below in ascertaining if these phenomenon exist more widely by-

(1) Expanding research beyond 2022, but focusing on the recent past may be best to maximize strategy

(2) Expanding research beyond Jersey City

(3) Using additional analytical tools to assess differences across rental metrics; biker populations; optimal times; etc.


**(7) Citations:**

(1) Questions asked of Xpert Learning Assistant include:
    (a) Haversine Formula for calculating distances

    (b) Pandas - splitting columns

    (c) Pandas concatenation


(2) Pandas concatenation: https://www.geeksforgeeks.org/how-to-merge-multiple-csv-files-into-a-single-pandas-dataframe/

