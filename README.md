# City-of-Chicago-Crimes-Project
## Overarching business questions of this project
  +	Provide an overview of the reported crime cases reported to the City of Chicago police department
  +	Identify any relationship between crime rate and a community area’s poverty level

## Based on the overarching business questions, the project aims to provide the following analysis
  1. Analysis of the data
      -  a. Primary crime types
      -  b. Locations where incidents occurred
      -  c. Trend in the chronological data 
  5. About the communities
     - a. Top community areas with the most reported cases
     - b. Economic standing on the community level
  6. Socio-economic impacts
     - a. Relationship revealed from the data between criminal activity and poverty level in the communities

## Data
  [City of Chicago Crimes – 2001 to Present](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/about_data)
  - 1.a. Primary crime types
  - 1.b. Locations where incidents occurred
  - 1.c. Trend in the chronological data
  - 2.a. Top community areas with the most reported cases

  [Census Data - Selected socioeconomic indicators in Chicago, 2008 – 2012](https://data.cityofchicago.org/Health-Human-Services/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2/about_data) was used to answer questions in combination with City of Chicago Crimes - 2001 to Present: 
  - 2.b. Economic standing on the community level
  - 3.a. Relationship revealed from the data between criminal activity and poverty level in the communities

## Tools and methodology
1.	A dashboard was created using Microsoft Power BI, including
    - Total number of cases
    - Total number of arrests
    - Percentage of households that are below poverty level during 2008 and 2012
    - A heatmap that lists the number of cases reported in different locations
    - Top 10 crime locations
    - Top 10 crime types identified from the dataset
    - Number of reported cases and arrests from 2001 to present
    - SES Indicators and the number of cases in Chicago’s 77 community areas from 2018 to 2012
    - Top community areas with the most reported cases and their average per capita income level

  In addition, filters are located on the top of the dashboard to allow users to select individual or multiple community area, primary crime type, location descriptions, and years, if a specific subgroup of data is of interest. 

![Capture](https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/82abcdd1-6477-4cc1-ac61-2b1e5fe5c3e4)

2. A variety of data visualizations and regression analyses were created using Python. Libraries used include:
    - Pandas
    - Numpy
    - Matplotlib
    - Seaborn
    - Sklearn (Sklearn.linear_model)
    - Geopandas
    - Geoplot

## Findings
### Analysis of the data
#### Question 1.a. Primary crime types
  - Top 3 primary crime types include **Theft**, **Battery** and **Criminal Damage**  
<img width="668" alt="Picture1" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/517240fb-dc38-48f4-a1de-e9cbfa63d0e7">
  
  - The multi-plot grids also showed that **Theft**, **Battery**, **Criminal Gamage** and **Narcotics** are the most prevalent crime types in the city over the years. 
<img width="668" alt="Picture2" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/b1d1fb38-76ec-4371-8c4d-9278e161a614">

#### Question 1.b. Locations where incidents occurred
  - Top 3 locations where most crimes occurred are **Street**, **Residence** and **Apartment**
<img width="668" alt="Picture3" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/b8f13a3c-90cb-47f1-9351-57d30be0c531">

#### Question 1.c. Trend in the chronological data
  - Overall, the total number of crimes declined from 2001 to present. A peak of criminal activities was witnessed in 2002 with a total number of 486815 cases reported.        In year 2020 and 2021, the total number of crimes decreased to a large extent (a reasonable assumption is that this is likely due to COVID and lockdown mitigations         implemented at the time, however, the number climbed back up starting 2022.
<img width="668" alt="Picture4" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/f6fad89b-6d09-4dc6-a963-f5a76bc04e4a">

### About the communities 
#### Question 2.a. Top community areas with the most reported cases
  - **Austin**, **Near North Side** and **South Shore** are the top 3 community areas with the most reported cases. Austin had almost twice cases reported than Near North       Side, the community area that has the second most total reported criminal cases. 
<img width="668" alt="Picture5" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/5de08b0e-f546-42ce-88d6-110f0632beb0">

  - A choropleth map was created to visualize the density of crime cases among Chicago’s 77 community areas. Neighborhoods that showed high crime numbers are filled with dark colors.
<img width="668" alt="Picture6" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/7584c728-fa3d-4135-9816-21c44c2eed93">

#### Question 2.b. Economic standing on the community level
Seven SES indicators were specified in the Census Data - Selected socioeconomic indicators in Chicago, 2008 – 2012. They are:
  - Percent aged under 18 or over 64
  - Percent households below poverty (% of households living below the federal poverty level)
  - Percent housing crowed (% of occupied housing units with more than one person per room)
  - Percent aged 16+ unemployed
  - Percent aged 25+ without high school diploma
  - Per capita income (sum of tract-level aggregate incomes divided by the total population)
  - Hardship index (overall score that incorporates each of the six indicators above)
<img width="822" alt="Picture7" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/58f5a6b4-a2ea-4450-b3f7-3b0ac632e6cf">

#### Question 3.a. Relationship revealed from the data between criminal activity and poverty level in the communities
So, does high poverty lead to high crime in Chicago communities? Unfortunately, Our data shows that it may not always be the case. The correlation between crime and poverty level varies community area by community area.  

A linear regression model was fitted to understand the relationship between total number of reported cases and hardship index. The results show a positive correlation between the two variables and that when hardship index goes up by 1, the total number of cases will increase by 200.87. 

<img width="668" alt="Picture8" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/8542752e-8429-4f2e-8936-2e210c08682e">

A linear regression model was fitted to understand the relationship between total number of reported cases and household poverty level. The results show a positive correlation between the two variables and that when the percentage of households below poverty goes up by 1% in that community area, the total number of cases will increase by 770.81. 

<img width="668" alt="Picture9" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/c14979b1-f83d-4533-8520-a7799bb736b2">

A linear regression model was fitted to understand the relationship between total number of reported cases and community per capita income level. The results show a slightly negative regression between the two variables and that when the per capita income drops by 1 USD in that community area, the total number of cases will decrease by 0.098. 

<img width="668" alt="Picture10" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/4b182e82-a229-4dee-a719-348991b663d1">

Although three regression models all suggested that the number of crimes are related to the socio-economic status of the community, the R squared is low for all three models, and they are 0.05, 0.08 and 0.004 respectively, indicating that the large portion of the variances in the dependent variable (number of crime cases) remain unexplained by the present independent variable. 

When looking at the choropleth maps side by side, although in some neighborhoods, high poverty may come with high crimes. This is true with Englewood, North Lawndale and West Englewood. 

However, we can also see that community areas with high poverty level are not always associated with high crimes, and vice versa. For example, Riverdale and Fuller Park are neighborhoods that are economically disadvantaged, but the total number of crime cases within those areas are low. West Town and Near North Side are two of the most affluent neighborhoods in Chicago, however, they both see soaring high criminal activities. 
<img width="868" alt="Picture11" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/c9cd35e4-524c-4f7b-8870-a26e7dcf6676">

## Summary
   - From 2001 to 2024, the overall number of reported cases in the city of Chicago has decreased over the years, except a slight uptick from 2016 to 2018.
   - The number of cases has been dropped from over 487k (2002) to 261k(2023).
   - During the peak of the Covid-19 global pandemic (2020 and 2021), the overall number of reported cases decreased, however, cases started to increase again in 2022.
   - The most reported crime types are theft, battery and criminal damage.
   - Most reported cases occurred on the street, followed by residence and apartment.
   - Austin (community area 25) has the most total number of reported cases over the years, followed by Near North Side (community area 8) and South Shore (community area 43).
   - Combining two data sources, link between crime and poverty level can be found in some community areas, for example, North Lawndale (community area 29), West Englewood (community area 67), and Englewood (community area 68).
   - However, crime was also prevalent in some wealthy neighborhood areas, such as Near North Side (community area 8) and West Town (community area 24).
   - More up-to-date data and indices are needed to further investigate the relationship between crime and poverty.

## Update - Most Prevalent Crime Type in Each Neighborhood
[A list](https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/blob/main/City_of_Chicago_Crime_Update.ipynb) of the most dominant type of crime (the type of crime that has the most reported cases) in each one of the 77 Chicago’s community areas has been retrieved from the dataset.

Clustering of the same crime type can be observed from the map generated to display the most prevalent type of crime in Chicago (left). The variable Crime Type seems to correlate with both proximity and the economic standing of the neighborhoods. The top 1 type of crime in all City of Chicago is Theft, and it seems to happen mostly in affluent areas, such as the north side of the city, including West Town (Community Area 24), and areas scattered around the southwest side, such as Beverly (Community Area 72). Battery occurred mostly in both central and south side of Chicago in areas with lower economic standings, for example, West Englewood (Community Area 67) and North Lawndale (Community Area 29). Narcotics happened the most around the west side of the city in Austin (Community Area 25), West Garfield (Community Area 26) and the neighborhoods adjacent to them.

<img width="1043" alt="Screen Shot 2024-04-25 at 12 12 56 PM" src="https://github.com/TaylorTS/City-of-Chicago-Crimes-Project/assets/99664400/d9ee4f7d-ddfc-4643-b859-8a239e2964f2">



