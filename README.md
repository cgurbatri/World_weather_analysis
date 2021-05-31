# World Weather

## Project Overview
PlanMyTrip is a travel company specializing in internet-related services in the hotel and lodging industry. Their user-interface team is interested in helping their clients find their ideal hotel based on weather in that area. The following deliverables will be executed to accomplish this goal:
1. Using the OpenWeather API, weather data will be retrieved from cities across the world.
2.  Using the Google Maps and Places API, maps will be generated indicating destination cities within user-provided temperature ranges.
3. Using Google Map Directions API, custom itinerary maps will be generated.

Additionaly, linear regression analysis performed on weather features and hemispheres to determine if certain weather features in cities can be predicted by the user-interface team.

## Resources

Software: Python 3.8.5, Anaconda 4.10.1, Jupyter Notebook 6.1.4
Data sources: citipy, jupyter gmaps, openweather API, google maps and places API, google maps and directions API

## Results
[WeatherPy_Database.csv](https://github.com/cgurbatri/World_weather_analysis/files/6572101/WeatherPy_Database.csv)
is a CSV file of randommly generate cities and their cooresponding weather information including: maximum temperature, cloudiness, wind speed and current weather conditions. Other identifying information includes country and latitude and longitude coordinates. Please note, this file can also be found in the Weather_Database folder. 

Method: Random module in Numpy was used to generate 2,000 sets of longitude and latitude coordinates. Citipy module can then be used to identify the nearest city to each set of coordinates. Finally, a request through the openweather API was used to retrieve the weather information the generated cities. 

Based on user preference regarding maximum and minimum temperature for their ideal destination city, the dataframe of the CSV file above is filtered, generating the following CSV file [WeatherPy_vacation.csv](https://github.com/cgurbatri/World_weather_analysis/files/6572192/WeatherPy_vacation.csv)

**Fig. 1** below is an example of a map the user would see, where markers indicate cities that meet their temperature criteria. When a marker is clicked, the following information is also displayed: a nearby hotel, country name, city name, and current weather conditions.

**Fig. 1**
[Uploading WeatherPy_vacation_map.png…]()

Please note, files related to and including Fig. 1 can be found in the Vacation_Search folder. 

Finally, this map can be further customized to display the travel route between 4 chosen cities, as shown in **Fig. 2** In this example, a route between 4 cities in Sri Lanka is shown. 

**Fig 2**
<img width="710" alt="WeatherPy_travel_map" src="https://user-images.githubusercontent.com/45336910/120242134-2b90df00-c232-11eb-90a3-0e15c241cc2c.png">

This map can also be generated with clickable markers that display the city name, country, nearby hotel, current weather description, and the maximum temperature, as shown in **Fig. 3.**

**Fig 3**
![WeatherPy_travel_map_markers](https://user-images.githubusercontent.com/45336910/120242270-832f4a80-c232-11eb-90da-98937c6b9718.png)

Method: Jupyter gmaps and Google Maps and Places API were used to generate Fig. 1 -3 and the corresponding csv files.
