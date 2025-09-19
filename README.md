# ⚔️ RuneSync
A personal dashboard combining fitness tracking, live weather, in-game news, and item price tracking in a nostalgic RuneScape-themed interface.

![RuneSync Demo](/resources/demo.png)

# Features:

### 🌤️ Weather
- **Customizable Location:** Select any city and fetch live weather data
- **Daily Snapshot:** Get today's maximum temperature and local sunrise/sunset times
- **Real-time Conditions:** Check the current condition and wind level
- **Precipitation Forecast:** See the chance of rain in the next 3 hours

### 🏃‍♂️ Fitness Tracking
- **Strava Integration:** Automatically syncs your Strava activities
- **Customizable Targets:** Track weekly running distance and weight training hours with progress bars

### 📈 Price Tracking
- **Real-time Prices:** Search any OSRS item by name and get current market prices (updated every 6 hours)
- **Price History:** Display a chart of the previous 7 days, plus daily and weekly percentage change


### 📰 News
- **Latest Updates:** Automatically fetches the latest OSRS news, complete with image and summary

# Quick Start:

### 💻 Prerequisites
- Python 3.8+
- [Strava API access](https://www.strava.com/settings/api/)
- [OpenWeatherMap API key](https://openweathermap.org/)

### 📁 Installation

**1) Clone the repository:**
   ```bash
   git clone https://github.com/chmcbs/RuneSync.git
   cd RuneSync
   ```

**2) Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

**3) Run the application:**
   ```bash
   python3 runesync.py
   ```

### ⚙️ Configuration

RuneSync requires several configuration files to function properly. Copy the example files and fill in your API credentials:

**1) Set up Strava integration:**
   ```bash
   cp strava_config.example.json strava_config.json
   cp strava_auth.example.json strava_auth.json
   ```
   - Edit `strava_config.json` with your Strava app credentials:
     - Get your client ID and client secret from [Strava API settings](https://www.strava.com/settings/api)
     - Replace `"CLIENT_ID"` and `"CLIENT_SECRET"` with your actual credentials
     - Keep the default `redirect_uri` as `http://localhost:5000/callback`
   - Run the application once to generate the authentication URL
   - Visit the provided URL to authorize RuneSync with your Strava account

**2) Set up weather data:**
   ```bash
   cp weather_config.example.json weather_config.json
   ```
   
   - Edit `weather_config.json` with your OpenWeatherMap API key:
     - Get your free API key from [OpenWeatherMap](https://openweathermap.org/api)
     - Replace `"OPENWEATHERMAP API KEY"` with your actual API key

**3) Configure user preferences:**
   ```bash
   cp user_preferences.example.json user_preferences.json
   ```

### 🔧 Customisation

Edit `user_preferences.json` to personalize your dashboard:

```json
{
  "weather": {
    "chosen_city": "london",              // Your city name
    "default_units": "metric"             // "metric" or "imperial"
  },
  "fitness_targets": {
    "running_km_per_week": 10,            // Your weekly running goal
    "weight_training_hours_per_week": 2   // Your weekly weight training goal
  },
  "tracked_item": "dragon bones"          // OSRS item to track prices for
}
```

# License:
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# Acknowledgments:
- **[Lost City](https://github.com/LostCityRS)** for the RuneScape assets
- **[RuneStar](https://github.com/RuneStar)** for the RuneScape fonts
- **[Old School RuneScape Wiki](https://oldschool.runescape.wiki/)** for item data and images
- **[OpenWeatherMap](https://openweathermap.org/)** for weather data
- **[Strava](https://developers.strava.com/)** for fitness tracking
- **[Proddy](https://github.com/hampo)** for technical support
- **[Jagex Limited](https://www.jagex.com/)** for creating RuneScape
