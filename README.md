# 🌦️ Live Weather Dashboard

A live weather dashboard project that fetches real-time weather data for multiple cities using the OpenWeatherMap API and displays it through dynamic charts and a Power BI dashboard.

---

## 📁 Project Structure

live-weather-dashboard/
│
├── data/ # Contains live_weather.csv (updated via GitHub Actions)
│
├── notebooks/ # Jupyter notebooks for data exploration and testing
│
├── outputs/
│ ├── charts/ # Static weather visualizations (e.g., temperature trends)
│ └── dashboards/ # Screenshots of the final Power BI dashboard
│
├── scripts/
│ └── fetch_live_weather.py # Script to fetch and store weather data from the API
│
├── .github/
│ └── workflows/
│ └── update_weather.yml # GitHub Actions workflow for automated data updates
│
└── README.md # Project overview and instructions


---

## 📌 Features

- 🔄 **Live Data Fetching**: Automatically pulls weather data every hour using GitHub Actions.
- 🌍 **Multi-City Support**: Currently supports cities like Mumbai, Delhi, London, and New York.
- ☁️ **Weather Description & Icons**: Displays weather conditions using icons and text dynamically.
- 📊 **Power BI Dashboard**: Visual representation of temperature, humidity, wind, and weather status.
- 🔗 **API Integration**: Uses OpenWeatherMap API for real-time data.

---

## 🚀 Technologies Used

- **Python** (requests, pandas)
- **OpenWeatherMap API**
- **GitHub Actions** (CI/CD for scheduled fetches)
- **Power BI** (dashboard creation)
- **CSV & JSON** for data storage and transformation

---

## ⚙️ How It Works

1. **Weather Fetching Script**  
   The script `scripts/fetch_live_weather.py` reads a list of cities and hits the OpenWeatherMap API to gather:
   - Temperature
   - Humidity
   - Wind Speed
   - Weather Description
   - Image URL (based on weather status)

2. **Automated Scheduling**  
   A GitHub Actions workflow (`.github/workflows/update_weather.yml`) runs this script hourly and commits the updated `data/live_weather.csv` to the repository.

3. **Dashboard Visualization**  
   Power BI is used to connect the CSV file hosted on GitHub (via Google Sheets), and create dynamic visuals.

---

## 🖼️ Dashboard Preview

You can find the screenshot of the live dashboard here:

📁 `outputs/dashboards/live_weather_dashboard.png`

---

## 🔑 API Setup (for contributors)

To fetch live weather data, you need an API key from [OpenWeatherMap](https://openweathermap.org/api).

1. Create a `.env` file in the root folder:
2. Make sure to keep your `.env` file **private** and do not push it to GitHub.

---

## 🧠 Future Improvements

- Add more cities dynamically from a user input or config file
- Add forecast data (next 7 days)
- Deploy Power BI report to the web via a secure method
- Add alert system for extreme weather

---

## 👤 Author

**Om Mahajan**  
[GitHub](https://github.com/mahajanom10)

---


