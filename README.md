# Metro-Op
## Metro Operations Optimization using Python
Metro Operations Optimization refers to the systematic process of enhancing the efficiency, reliability, and effectiveness of Metro services through various data-driven techniques and operational adjustments.

I've collected this dataset from kaggle and it contains several files, as follows:

Agency: Information about the Delhi Metro Rail Corporation, including name, URL, and contact details.

Calendar: Service schedules delineating the operation days (weekdays, weekends) and valid dates for these schedules.

Routes: Details of metro routes, including short and long names, type of route, and descriptions.

Shapes: Geographical coordinates of routes, providing the precise paths taken by the metro lines.

Stop Times: Timetables for each trip indicating arrival and departure times at specific stops.

Stops: Locations of metro stops, including latitude and longitude coordinates.

Trips: Information linking trips to routes, including details like trip identifiers and associated route IDs.


## Analysis

1. Plotting the geographical routes on a map to visualize the network.
   
2. Examining the frequency and scheduling of trips across different days of the week.
   
3. Analyzing coverage by examining the distribution of stops and their connectivity.

![image](https://github.com/Koninikax/Metro-Op/assets/96631757/f8c23e40-c613-4b5e-8658-ab87ef9579b4) 

The map visualization shows the geographical paths of the Delhi Metro routes. Each line (identified by a unique colour) represents the path of a different route defined in the shapes dataset. This visual helps to understand how the Metro covers the geographical area of Delhi, demonstrating the connectivity and spread of the network.

![image](https://github.com/Koninikax/Metro-Op/assets/96631757/567556c7-8f26-497c-9283-58b7ba1f0e85)

The bar chart illustrates the number of trips scheduled for each day of the week for the Delhi Metro. As we can see, the number of trips from Monday to Friday is consistent, indicating a stable weekday schedule designed to accommodate regular commuter traffic. In contrast, the trips decrease slightly on Saturday and even more on Sunday, reflecting lower demand or a reduced service schedule on weekends.

This finding suggests that the Delhi Metro strategically scales its operations based on the expected daily ridership, which likely peaks during weekdays due to work and school commutes.

![image](https://github.com/Koninikax/Metro-Op/assets/96631757/a1a8644e-9e72-4ad2-9dab-af2c3a406825)

The scatter plot above shows the geographical distribution of Delhi Metro stops. Each red dot represents a metro stop, and their distribution across the map illustrates how the stops cover different areas of Delhi.

From the plot, we can see a widespread distribution, suggesting that the Delhi Metro provides good spatial coverage, allowing access to a broad area and facilitating efficient travel across the city.

The stops are fairly evenly spread, but there are denser clusters, which indicates areas with higher transit needs or central hubs that connect multiple lines.

![image](https://github.com/Koninikax/Metro-Op/assets/96631757/eeca3b28-54be-419d-9b78-5179713de650)

The scatter plot above represents the number of routes that pass through each Delhi Metro stop. Stops are visualized in different colours and sizes based on the number of routes they connect, providing insights into the complexity of the network at various locations. Key observations are:

Hubs and Transfer Points: Larger circles (in warmer colours) indicate stops where multiple routes intersect. These stops serve as major transfer points within the network, facilitating easier cross-city travel for passengers.
Distribution: Stops with fewer routes, shown in cooler colours and smaller sizes, tend to be more peripheral or on less busy lines. The central areas and more populated zones have stops with greater connectivity.

![image](https://github.com/Koninikax/Metro-Op/assets/96631757/3bfada0f-f9cb-4d65-bf5f-0d25e271c387)


The bar chart above displays the average interval between trips on the Delhi Metro during different parts of the day: morning, afternoon, and evening. This data provides insight into the service frequency and how it is adjusted based on the expected demand throughout the day. Key findings are:

Morning: Shorter intervals between trips are observed in the morning hours, which likely corresponds to the morning rush hour when commuters are heading to work or school.
Afternoon: The intervals increase slightly during the afternoon, which may indicate a reduction in demand after the morning peak.
Evening: In the evening, intervals decrease again, likely to accommodate the evening rush hour as people return home.

To get a basic understanding of how service levels vary throughout the day, we’ll classify the intervals as:

Early Morning: Before 6 AM
Morning Peak: 6 AM to 10 AM
Midday: 10 AM to 4 PM
Evening Peak: 4 PM to 8 PM
Late Evening: After 8 PM


![image](https://github.com/Koninikax/Metro-Op/assets/96631757/b345f9b4-e7cb-448d-bbe0-4b1f2bd311cf)

The bar chart displays the number of trips scheduled for each time interval in the Delhi Metro system. From this visualization, we can observe the following:

Early Morning: There is a relatively low number of trips, indicating less demand or fewer scheduled services during these hours.

Morning Peak: There is a significant increase in the number of trips compared to the early morning, likely due to morning commute hours as people travel to work or school.

Midday: The number of trips remains high, perhaps sustaining the morning rush or due to other midday travel needs.

Evening Peak: This period sees a slight decrease compared to midday but remains one of the busier times, probably reflecting the evening commute.

Late Evening: The number of trips drops again, but remains higher than in the early morning, likely catering to people returning home late or involved in evening activities.


## Optimization Operations
To reduce the overcrowding in the Delhi Metro, we can adjust train frequencies based on time interval analysis. For instance, if certain time intervals like the morning or evening peaks show signs of overcrowding, increasing the number of trips or adjusting the timing of the trips could help alleviate this issue.
An assumption here is that morning and evening peaks need a 20% increase in service, while midday and late evening might handle a 10% reduction without impacting passenger service negatively.

![image](https://github.com/Koninikax/Metro-Op/assets/96631757/54a0cd89-b63c-444c-9880-e9641bfd1d54)


The bar chart illustrates the original versus adjusted number of trips per time interval for the Delhi Metro, based on our hypothetical adjustments to better align service levels with inferred demand:

Morning and Evening Peaks: We increased the number of trips by 20%, anticipating higher demand during these hours. This adjustment aims to reduce overcrowding and improve passenger comfort and service reliability.

Midday and Late Evening: We decreased the trips by 10%, assuming that the demand drops during these times, allowing for more efficient use of resources without significantly impacting service quality.

By implementing these adjustments, Delhi Metro can potentially improve operational efficiency and customer satisfaction, especially during peak hours.
