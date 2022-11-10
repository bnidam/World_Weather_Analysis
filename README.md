# World_Weather_Analysis

## Project
This project uses collected weather data from over 500 cities around the world to create a PlanMyTrip app where the user can filter for their weather preferences to identify potential travel destinations and nearby hotels. Users can then choose four cities from these potential travel destinations and create a travel itinerary that includes a travel route between the four cities.

## Tools used for this project
The tools used for this project include Python and jupyter notebook: pandas, matplotlib, numpy, citipy, requests, gmaps; OpenWeather, Google Maps, and Google Places APIs.

## Project process

### Identifying cities around the world
A database of cities were generated using a random number generator to produce 2,000 pairs of latitude and longituded for both the northern and southern hemisphere. Using citipy, these lat/lon pairs were used to locate the city nearest to these points. The cities, along with the lat/lon pairs, were added to a dataframe. 

### Retrieving weather data
The city lat/lon pairs were used with an API call to OpenWeather.com to retrieve a list of specific weather data for each city. This weather data included maximum temperature, humidity, cloudiness, windspeed, and a description of current weather. The country was also identified. All of this information was saved in a dataframe, reorganized and saved in a csv file.

### User preferences
Input boxes were created to collect the user's minimum and maximum temperature preferences.

### Identifying potential travel destinations and nearby hotels
The user's preferences were used to identify cities in the dataframe mentioned above that fit with the user's preferences. A set of basic parameters and a Google Maps API call were used to locate nearby hotels in those identified cities. These hotels and potential travel destinations were saved into a new dataframe. 

### Map of potential travel destinations with markers and info boxes
A heatmap was created showing the potential travel destinations based on the user's preferences with markers and infoboxes showing the hotel name, city, maximum temperature, and current weather.
![Cities Hotels Markers Infoboxes](https://github.com/bnidam/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map_infobox.png)

### Travel itinerary
A travel itinerary was also created from a selection of four relatively nearby cites, showing the travel route by driving.  This map also has markers and infoboxes with the same information as above.
The example in this project shows a travel destination to Sri Lanka and an excursion to four cities along the southern coast.
![Travel Itinerary in Sri Lanka](https://github.com/bnidam/World_Weather_Analysis/blob/main/Vacation_Itinerary/weatherPy_travel_map1.png)















