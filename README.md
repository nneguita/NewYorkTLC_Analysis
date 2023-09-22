# New York City Taxi & Limousine Commission (TLC) Analysis

## Contents
1. [Introduction](#introduction)
2. [Stakeholders](#stakeholders)
    1. [NYC TLC](#nyc-tlc)
    2. [New York Taxi and Limousine Companies](#new-york-taxi-and-limousine-companies)
3. [Dataset](#dataset)
    1. [Glossary](#glossary)
5. [Objective](#objective)
6. [Analysis Overview](#analysis-overview)
7. [Tools and Technologies](#tools-and-technologies)
8. [Conclusion and Recommendations](#conclusion-and-recommendations)
9. [Additional Resources](#additional-resources)

## Introduction <a name="introduction"></a>
The **Taxi & Limousine Commission (TLC)** is a regulatory body responsible for overseeing taxi and for-hire vehicle services across various cities and regions. Its mission is to maintain the safety, quality, and legality of these services. The TLC ensures a balance between the interests of passengers and service providers, contributing to an efficient and well-regulated transportation ecosystem.

## Stakeholders <a name="stakeholders"></a>
### NYC TLC <a name="nyc-tlc"></a>
The primary regulatory authority, the **Taxi & Limousine Commission (NYC TLC)**, governs and supervises taxi and for-hire vehicle services within New York City. It works in conjunction with the **New York City Department of Transportation (DOT)** to manage the city's transportation infrastructure, ensuring the safety and efficiency of transportation systems within the city.

### New York Taxi and Limousine Companies <a name="new-york-taxi-and-limousine-companies"></a>
These companies operate within the city and are significant contributors to the taxi and for-hire vehicle landscape, providing essential transportation services to the public. They collaborate with NYC TLC and DOT to maintain the seamless flow and safety of the city's transportation network.

## Dataset <a name="dataset"></a>
The dataset under analysis is sourced from the NYC TLC and compiled by **Creative Mobile Technologies** and **VeriFone** as part of the **Livery Passenger Enhancement Program (LPEP)**. It offers an extensive collection of records documenting taxi and for-hire vehicle journeys within New York City, providing valuable insights into the city's dynamic transportation landscape.

### Glossary <a name="glossary"></a>
| Feature | Description |
| --- | --- |
| LPEP_ID | LPEP Provider Code that provided the record. <br> 1. Creative Mobile Technologies, LLC <br> 2. VeriFone Inc.
| PU_DateTime | Date and Time when meter was engaged.
| DO_DateTime | Date and Time when meter was disengaged.
| Passenger_Qty | Number of passengers in the vehicle, driver-entered value.
| Distance | Elapsed distance in miles by the taximeter.
| PULocationID | TLC Taxi Zone where the taximeter was engaged.
| DOLocationID | TLC Taxi Zone where the taximeter was disengaged.
| RatecodeID | Final rate code in effect at the end of the code. <br> 1. Standard Rate <br> 2. JFK <br> 3. Newark <br> 4. Nassau/Westchester <br> 5. Negotiated Fare <br> 6. Grouped Ride
| Reserved_Status | This flag indicates whether the trip record was held in the vehicle memory before sending to the vendor, aka “store and forward,” because the vehicle did not have a connection to the server. <br> Y = store and forward trip <br> N = not a store and forward trip
| Payment_Type | A numeric code signifying how the passenger paid for the trip. <br> 1 = Credit card <br> 2 = Cash <br> 3 = No charge <br> 4 = Dispute <br> 5 = Unknown <br> 6 = Voided trip
| Base_Fare | The time-and-distance fare is calculated by the meter. Extra Miscellaneous extras and surcharges Currently, this only includes the $0.50 and $1 rush hour and overnight charges.
| Extra_SCG | Extra charges that covers e-hail service fee/TLC regulated tax/Rush hour extra/overnight extra/trip distance extra (Airports/Counties)
| MTA_Tax | $0.50 MTA tax that is automatically triggered based on the metered rate in use.
| Improvement_SCG | $0.30 improvement surcharge assessed on hailed trips at the flag drop, Used to improve for-hire vehicles services. Began in 2015.
| Tip | This field is automatically populated for credit card tips. Cash tips are not included.
| Tolls_Fee | The total amount of all tolls paid in the trip.
| Total_Fare | The total amount charged to passengers. Does not include cash tips.
| Trip_Category | A code indicating whether the trip was a street hail or a dispatch that is automatically assigned based on the metered rate in use but can be altered by the driver. <br> 1 = Street-hail <br> 2 = Dispatch
| Congestion_SCG | $2.50 congestion surcharge for peak traffic hours in Manhattan area. Began in 2019
| PU_Hour | Pickup Hour taken from PU_DateTime
| DO_Hour | Dropoff Hour taken from DO_DateTime
| PU_TimeDay | Pickup Category based on their Hours
| DO_TimeDay | Dropoff Category based on their Hours
| PU_Day | Pickup Day Name based on calendar
| DO_Day | Dropoff Day Name based on calendar
| Trip_Duration | Elapsed Duration between Pickup and Dropoff
| PULocation Name | Pickup borough Name based on PULocationID
| DOLocation Name | Dropoff borough Name based on DOLocationID

## Objective <a name="objective"></a>
This analysis aims to explore various facets of the dataset, uncovering patterns, trends, and potential areas of interest related to taxi and for-hire vehicle journeys in New York City. It seeks to offer stakeholders valuable insights to enhance service quality, operational efficiency, and overall user experience.

## Analysis Overview <a name="analysis-overview"></a>
The analysis delves into several aspects of the dataset, including:
- **Trip Duration Analysis:** Examines the distribution of trip durations and identifies common durations for taxi journeys.
- **Passenger Count Analysis:** Explores the typical number of passengers per trip and the variations in passenger count.
- **Payment Type Analysis:** Investigates the preferred payment methods used by passengers.
- **Trip Distance Analysis:** Analyzes the distribution of trip distances and uncovers trends in travel distances within the city.
- **Time-Based Analysis:** Breaks down trips based on pickup and drop-off times to identify peak hours and patterns related to time.
- **Location Analysis:** Utilizes the provided taxi zone lookup data to map location IDs to Boroughs, offering insights into the popular locations for taxi rides in the city.

### [Link to the Analysis Notebook](https://github.com/nneguita/NewYorkTLC_Analysis/blob/master/NYC%20TLC%20Trip%20Record%20Analysis.ipynb)

## Tools and Technologies <a name="tools-and-technologies"></a>
- **Python:** The primary programming language used for performing data analysis.
- **Jupyter Notebook:** An open-source web application that allows the creation and sharing of documents that contain live code, equations, visualizations, and narrative text.
- **Pandas:** A fast, powerful, flexible, and easy-to-use open-source data analysis and manipulation library for Python.
- **Matplotlib & Seaborn:** Visualization libraries in Python for creating static, animated, and interactive visualizations.
- **Tableau:** Visualization application for creating interactive visualization consisting of story and dashboard.

## Conclusion and Recommendations <a name="conclusion-and-recommendations"></a>
The analysis provides a comprehensive overview of taxi and for-hire vehicle services in New York City, enabling stakeholders to make informed decisions and implement strategies to optimize service delivery, improve user satisfaction, and enhance operational efficiency.

**Key Recommendations:**
- **Optimizing Fleet Management:** By leveraging insights on peak hours and high-demand locations, companies can optimize fleet management to ensure the availability of vehicles during high-demand periods.
- **Enhancing Customer Experience:** Insights on passenger preferences, such as payment methods, can help in tailoring services to meet customer needs and expectations, thereby improving user satisfaction.
- **Strategic Planning:** The analysis of trip durations, distances, and passenger counts can aid in strategic planning and policy formulation to address the varying needs and preferences of passengers effectively.

## Additional Resources <a name="additional-resources"></a>
- **[NYC TLC Trip Record Analysis Notebook](https://github.com/nneguita/NewYorkTLC_Analysis/blob/master/NYC%20TLC%20Trip%20Record%20Analysis.ipynb)**
- **[NYC TLC Trip Record Dataset](https://github.com/nneguita/NewYorkTLC_Analysis/blob/master/Dataset/NYC%20TLC%20Trip%20Record.csv)**
- **[Taxi Zone Lookup Dataset](https://github.com/nneguita/NewYorkTLC_Analysis/blob/master/Dataset/taxi%2B_zone_lookup.csv)**
