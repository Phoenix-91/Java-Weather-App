# Java Weather App (Swing GUI)

A desktop weather application built with Java Swing and the OpenWeatherMap free API.

---

## Project Structure

```
WeatherApp/
├── src/
│   ├── WeatherApp.java      ← Main entry point
│   ├── WeatherGUI.java      ← Swing GUI
│   ├── WeatherService.java  ← API calls
│   └── WeatherData.java     ← Data model
├── lib/
│   └── json-20231013.jar    ← JSON parser (download separately)
└── README.md
```

---

## Setup

### 1. Get an API Key
- Sign up at https://openweathermap.org
- Go to API Keys and copy your key
- Open `WeatherService.java` and replace `YOUR_API_KEY_HERE`

### 2. Download the JSON library
- Download from: https://mvnrepository.com/artifact/org.json/json
- Place the `.jar` file inside the `lib/` folder

### 3. Compile
```bash
javac -cp lib/json-20231013.jar src/*.java -d out/
```

### 4. Run
```bash
# On Mac/Linux:
java -cp out:lib/json-20231013.jar WeatherApp

# On Windows:
java -cp out;lib/json-20231013.jar WeatherApp
```

---

## Features
- Search weather by city name
- Displays temperature, humidity, wind speed, feels-like
- City + country code shown
- Current date displayed
- Background thread for API calls (no UI freeze)
- Error dialogs for invalid city or bad API key
