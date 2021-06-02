# Python API Project: &nbsp;What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. &nbsp;So let's use Python requests, APIs, and JSON traversals to answer a fundamental question: &nbsp;"What's the weather like as we approach the equator?"

Now, we know what you may be thinking: &nbsp;_"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it? 

## Part I - WeatherPy

In this example, we will be creating a Python script to visualize the weather of 500+ cities across the world, at varying distances from the equator. &nbsp;To accomplish this, we will be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

The first objective is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

The second objective is to run linear regression on each relationship. &nbsp;This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

The final notebook will:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

## Part II - VacationPy

Now let's use weather data to plan future vacations. &nbsp;Use jupyter-gmaps and the Google Places API for this part of the project.

This objective:

* Created a heat map that displays the humidity for every city from Part I.

* Narrowed down the DataFrame to find the ideal weather condition. &nbsp;For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

* Used Google Places API to find the first hotel for each city located within 5,000 meters of located coordinates.

* Plotted the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.
