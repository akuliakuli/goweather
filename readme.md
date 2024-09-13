# Go Weather API

## Overview

This project is a simple REST API written in Go that retrieves current weather data for any city using the OpenWeatherMap API. The project demonstrates basic functionality such as handling HTTP requests, interacting with a third-party API, and parsing JSON data. 

The application provides two main endpoints:
1. **/hello**: A basic endpoint that returns a greeting message.
2. **/weather/{city}**: This endpoint fetches the current weather information for the specified city using the OpenWeatherMap API and returns the data in JSON format.

The weather data includes key information such as the city name and current temperature (in Kelvin).

## How It Works

The application loads the OpenWeatherMap API key from a configuration file (`.apiConfig`) and uses it to send requests to the OpenWeatherMap API. When a city is provided in the URL, the application fetches the current weather data for that city and returns the result as a JSON response.

The project is structured with the following key functionalities:
- **API Key Loading**: The API key is stored in a JSON config file and loaded at runtime.
- **Weather Query**: The `/weather/{city}` endpoint processes the city input, makes an external API call, and returns the parsed data.
- **Error Handling**: If there are issues with the API request or response parsing, the server responds with a suitable error message.

## Key Features

- **HTTP Server**: The Go application acts as a web server listening on port 8080.
- **OpenWeatherMap Integration**: Weather data is fetched from the OpenWeatherMap API using the API key stored in the configuration file.
- **JSON Response**: The `/weather/{city}` endpoint returns weather data in JSON format, including the city name and temperature.
- **Simple Configuration**: The API key is easily configurable through a `.apiConfig` JSON file.

## Technologies Used

- **Go**: The core programming language used for developing the server and handling HTTP requests.
- **OpenWeatherMap API**: A third-party service used to fetch real-time weather data.
- **JSON**: Data interchange format for configuration and responses.
- **HTTP**: Communication protocol for handling requests and responses.

## Next Steps

Possible enhancements for this project:
- Error handling improvements for specific HTTP status codes from OpenWeatherMap.
- Addition of unit tests to ensure reliability.
- Conversion of temperature to other units (Celsius, Fahrenheit).
- Caching responses for repeated city requests to reduce API calls.
