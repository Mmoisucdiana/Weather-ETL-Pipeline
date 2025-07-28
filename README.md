# Weather-ETL-Pipeline
This project implements a simple ETL (Extract, Transform, Load) pipeline in Python that collects current weather data for a given city using the WeatherAPI.

## 🔍 Overview

The script performs the following:

- **Extract**: Connects to the WeatherAPI and pulls current weather data for a specified city.
- **Transform**: Parses the JSON response, selects relevant fields (e.g., temperature, humidity, condition), and adds a local timestamp.
- **Load**: Appends the data to a local CSV file (`weather_data.csv`). Duplicate entries (based on `location` and `last_updated`) are ignored to ensure data integrity.

## 🧪 Technologies

- Python 3
- Requests
- Pandas
- WeatherAPI (https://www.weatherapi.com/)

## 📦 File
 `weather_data.csv`: Output CSV file storing the collected data.

## ✅ Features

- Incremental data load (no duplicates).
- Can be scheduled using a cron job or Airflow DAG.
- Easily extensible to collect data for multiple cities or load into a database.
