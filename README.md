# World Weather Analysis

## Overview of the project
The goal of the project is to retrieve weather data from OpenWeatherMap API and build a heatmap on Google map showing max temperature.
User can define the range of desired max temperature for the next vacation. Based on their choice heatmap and tags with offered hotels are built. Also, there is a possibility to build a route on map for round trip through 4 cities.

To complete the project, I used python with pandas, numpy, gmaps, requests libraries.

## Results
First of all, I’ve generated random coordinates (latitude and longitude) using numpy library. Based on these coordinates I retrieved cities’ name, which are nearest to the generated coordinates, with a citipy library. 
When I got list of cities, I made API request to retrieve weather data from OpenWeatherMap and stored the result in [WeatherPy_Database.csv](https://github.com/angkohtenko/World_Weather_Analysis/blob/main/Weather_Database/WeatherPy_Database.csv) 

Then I took the input from a user. The user defined range of comfortable temperature. I filtered cities which are within the range and using Google API I found hotels in these cities. I created the heat map with tags for selected hotels and cities.

![](https://github.com/angkohtenko/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)

Finally, using the Google Maps Directions API, I created a travel route between the four cities.

![](https://github.com/angkohtenko/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png)

