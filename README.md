# Humanforce Android Engineering Challenge

## Overview
This challenge is designed to assess your Android engineering skills through the development of a simple weather forecast application. We're looking for innovative solutions that demonstrate strong architectural thinking, clean code principles, an eye for design,and a deep understanding of Android development best practices.

## Project Objective
Implement the requirements below to create a weather forecast application using the OpenWeatherMap API to showcase your ability to design scalable, maintainable, and high-quality Android software.

# OpenWeatherMap API Information
### API Endpoints
| Endpoint | Remarks |
|---|-----|
| [5 day weather forecast](https://openweathermap.org/forecast5) | Note the 3 hour time period in forecast data, this must be aggregated to get daily min/max values. |
| [GeoCoding API](https://openweathermap.org/api/geocoding-api) | Fetch coordinates for a text based search term to use in forecast/current weather API calls. |
| [Current Weather](https://openweathermap.org/current) | Fetch current conditions for the given coordinates.

### API Configuration

#### 1. Generate an OpenWeatherMap API Key
1. Visit [OpenWeatherMap](https://openweathermap.org/api)
2. Sign up for a free account
3. Generate an API key from your account dashboard

#### 2. Configure the API Key
**IMPORTANT: Never commit API keys directly to source control**

1. In the project root directory, run `cp .env.example .env`.
2. Add your OpenWeatherMap API key to the copied `.env` file.
3. Build the project in Android Studio to inject the API key defined the `.env` file to the apps `BuildConfig`.

#### 3. Consumming the API Key
An `APIKeyManager` helper object is provided for you to access the API key. If the previous two steps are followed then the API key can simply be accessed via `APIKeyManager.apiKey` anywhere in the project.

# Project Requirements

> **Important**: Pay close attention to the requirement to aggregate 3 hour forecast windows in the 5 day forecast data to get daily min/max forecast values.

## General Requirements
These are the general requirements that apply broadyly to the specific functional requirements that are to be implemented.

> **Important**: The project must use Swift & SwiftUI

#### Weather Display
- Show weather in metric units
- Use provided OpenWeatherMap icons (or SF Symbols).

#### Error Handling
- Gracefully manage:
  - Network connectivity issues
  - API errors
  - Location permissions
---

## Functional Requirements

#### 1. Display weather for current location
  - Automatically fetch and display current weather for the user's current location
  - Display 5-day forecast for current location
  - Handle location services unavailability gracefully

#### 2. Location search and management
  - Implement city search functionality
  - Allow searching locations by city name
  - Display search results
  - Select a search result to view current weather and five day forecast
  - Show 5-day forecast for selected location

#### 3. Save Locations
  - Save favorite locations
  - Display a list of saved locations
  - Switch between saved locations

#### Bonus Points
  - Add unit tests
  - Implement offline caching
  - Support for multiple temperature units
  - Implement a homescreen widgets

## Submission Guidelines
1. Provide any additional setup instructions
2. Include comments explaining complex logic
3. Advise our talent acquisition team once you have completed the assessment so that our team can begin their evaluation.

## Time Expectation
- Estimated completion time: 6 hours
- Focus on quality over complete feature set

## Questions?
If you have any questions or need any clarifications, please reach out to your hiring manager or recruiter.

# **🎉 Good luck and happy coding! 🎉**

