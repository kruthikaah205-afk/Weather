 # 🌤️ Real-Time Weather Forecasting Web Application

A simple and user-friendly **Real-Time Weather Forecasting Web Application** built using **Python, Flask, HTML, and CSS**.

The application allows users to search for any city and view its current weather conditions along with a **7-day weather forecast**. Weather information is retrieved in real time using the **Open-Meteo API**.

## 📌 Features

- 🔍 Search weather by city name
- 📍 Display city, state, and country
- 🌡️ Show current temperature
- 🌡️ Display feels-like temperature
- 💧 Display relative humidity
- 💨 Display wind speed
- 🌧️ Display current precipitation
- ☀️ Weather condition icons and descriptions
- 📅 7-day weather forecast
- 🌡️ Daily minimum and maximum temperatures
- 🌧️ Daily precipitation probability
- 🇮🇳 Prioritizes Indian locations during city search
- 📱 Responsive web interface for desktop and mobile
- ⚠️ Error handling for invalid cities and API failures

## 🛠️ Technologies Used

- **Python**
- **Flask** – Web application framework
- **Requests** – API requests
- **HTML** – Web page structure
- **CSS** – User interface styling
- **Open-Meteo Geocoding API** – City/location search
- **Open-Meteo Weather API** – Real-time weather and forecast data

## 📂 Project Structure

```text
Weather-App/
│
├── wheather.py
└── README.md
```

The project currently uses a **single Python file** containing the Flask application, HTML template, CSS styling, API integration, and application routes.

## ⚙️ Requirements

Make sure Python is installed on your computer.

Install the required Python packages:

```bash
pip install flask requests
```

## 🚀 How to Run the Project

### 1. Clone or download the project

Place `wheather.py` inside your project folder.

### 2. Open the project folder in VS Code

Open a terminal in the same folder.

### 3. Install dependencies

```bash
pip install flask requests
```

### 4. Run the application

```bash
python wheather.py
```

The Flask server is configured to run on:

```text
http://127.0.0.1:5000
```

The application starts through Flask's `app.run()` configuration with port `5000`.

### 5. Open the application

Open your browser and visit:

```text
http://127.0.0.1:5000
```

## 🔄 How the Application Works

### Step 1: Enter a City

The user enters a city name into the search box.

```text
Enter city name...
```

The application accepts the city through a POST request.

### Step 2: Find the Location

The application sends the city name to the Open-Meteo geocoding service to obtain:

- Latitude
- Longitude
- City name
- State/region
- Country

The application also gives preference to Indian locations and specifically handles Karnataka/Bengaluru results.

### Step 3: Fetch Weather Data

The latitude and longitude are passed to the Open-Meteo forecast API.

The application retrieves current:

- Temperature
- Relative humidity
- Apparent temperature
- Precipitation
- Weather condition
- Wind speed

It also requests daily forecast information for **7 days**.

### Step 4: Convert Weather Codes

The application converts numerical weather codes into readable descriptions and emojis.

Examples include:

```text
☀️ Clear sky
🌤️ Mainly clear
⛅ Partly cloudy
☁️ Overcast
🌧️ Rain
⛈️ Thunderstorm
❄️ Heavy snow
```

This conversion is handled by the `weather_description()` function.

### Step 5: Display the Results

The web page displays the current weather in a visually styled dashboard, including temperature, humidity, wind speed, precipitation, and weather condition.

The application also displays a 7-day forecast containing:

- Date
- Weather condition
- Weather icon
- Minimum temperature
- Maximum temperature
- Rain probability

## 🎨 User Interface

The application uses a responsive HTML/CSS interface with:

- Gradient background
- Weather cards
- Search box
- Responsive forecast grid
- Mobile-friendly layout
- Weather emojis

The CSS includes responsive layouts for screen widths below 800px and 500px.

## ❗ Error Handling

The application handles several common errors:

### Empty City

If the user does not enter a city:

```text
Please enter a city name.
```

### City Not Found

If the geocoding API cannot find the city:

```text
City not found.
```

### Weather API Failure

If weather data cannot be retrieved:

```text
Failed to fetch weather data.
```

These conditions are handled in the Flask route.

## 🔌 APIs Used

### Open-Meteo Geocoding API

Used to convert a city name into geographic coordinates.

```text
https://geocoding-api.open-meteo.com/v1/search
```

### Open-Meteo Weather API

Used to retrieve current and forecast weather data.

```text
https://api.open-meteo.com/v1/forecast
```

The application uses Python's `requests` library to communicate with these APIs. 
## 🧪 Example

Search for:

```text
Bengaluru
```

The application can display information such as:

```text
📍 Bengaluru, Karnataka, India

🌤️ 28 °C
Mainly clear

🌡️ Feels Like: 29 °C
💧 Humidity: 65%
💨 Wind Speed: 12 km/h
🌧️ Precipitation: 0 mm

📅 7-Day Forecast
```

*The actual values depend on the live API response.*

## 🔐 API Key

This project does **not require an API key** for the Open-Meteo endpoints used by the application.

## 🚀 Future Enhancements

The project can be improved by adding:

- 📍 Automatic user location detection
- 🗺️ Interactive weather map
- 🌅 Sunrise and sunset information
- 🌙 Dark/light mode
- 🔔 Weather alerts
- 📊 Weather graphs and charts
- 🌡️ Hourly forecast
- 📱 Progressive Web App support
- 🌍 Weather comparison between multiple cities
- 🗣️ Voice-based city search
- 🤖 AI-powered weather summaries
- 📈 Historical weather analysis

## 👩‍💻 Author

**Kruthika AH**

## 📄 License

This project is created for **educational and academic purposes**.

---

## ⭐ Conclusion

The Real-Time Weather Forecasting Web Application provides a simple way to retrieve and visualize live weather information. By combining **Python Flask**, **Open-Meteo APIs**, HTML, and CSS, the application provides current weather conditions and a 7-day forecast through an easy-to-use web interface.
