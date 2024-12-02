## Overview

### Part 1: WeatherPy
The **WeatherPy** project aims to analyze the relationship between weather variables (Temperature, Humidity, Cloudiness, and Wind Speed) and latitude. The data is fetched from the OpenWeatherMap API. The project generates several scatter plots to visualize the relationships between these weather variables and latitude and computes linear regression to analyze the correlation in both the Northern and Southern Hemispheres.

### Part 2: VacationPy
The **VacationPy** project leverages the weather data and uses the Geoapify API to help find the best vacation destinations based on weather conditions. For each city in the dataset, the program visualizes the city on a map, filters cities based on ideal weather conditions (temperature, humidity, etc.), and uses the Geoapify API to find nearby hotels within 10,000 meters.

## Technologies Used

- **Python 3.x**: The primary programming language used for the project.
- **Pandas**: Data manipulation and analysis.
- **Matplotlib**: For creating the plots and visualizations.
- **Seaborn**: Used for advanced visualizations and statistical plots.
- **SciPy**: For performing linear regression.
- **Requests**: For making API requests to OpenWeatherMap and Geoapify.
- **Folium**: For map visualizations.
- **Geoapify API**: Used to fetch nearby hotels based on coordinates.

## Part 1: WeatherPy

### 1.1 Weather Data Retrieval

The project uses the **OpenWeatherMap API** to retrieve weather data for a list of cities. The data includes key weather variables such as:

- Temperature
- Humidity
- Cloudiness
- Wind Speed

### 1.2 Plots and Visualizations

Several scatter plots are generated to visualize the relationship between:

- Latitude and Temperature
- Latitude and Humidity
- Latitude and Cloudiness
- Latitude and Wind Speed

Each plot is generated using `matplotlib` and `seaborn` for effective visualization.

### 1.3 Linear Regression Analysis

Linear regression is performed on weather variables against latitude for both the **Northern Hemisphere** (latitudes > 0) and the **Southern Hemisphere** (latitudes < 0). Linear regression helps analyze and predict trends such as how temperature changes as you move towards the poles or the equator.

#### Linear Regression Plots:
- Temperature vs. Latitude (for both hemispheres)
- Humidity vs. Latitude (for both hemispheres)
- Cloudiness vs. Latitude (for both hemispheres)
- Wind Speed vs. Latitude (for both hemispheres)

## Part 2: VacationPy

### 2.1 Map Visualization

A map is created using the **hvplot** library in pandas, displaying each city's coordinates along with weather information like temperature. The cities are plotted as points on the world map.

### 2.2 Ideal Vacation Conditions

The cities are filtered based on the following ideal weather conditions:

Only cities that meet these conditions are selected for vacation recommendations.

### 2.3 Geoapify API for Hotels

The assignment uses the **Geoapify API** to find hotels within 10,000 meters of the selected cities that meet the ideal weather criteria. Hotel names and country details are added as hover information on the map.

