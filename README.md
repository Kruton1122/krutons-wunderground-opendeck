# ⚡ Krutons Wunderground Plugin for OpenDeck

Display live weather data from your personal **Weather Underground** station directly on your OpenDeck device. Built for the Ajazz AKP153E and compatible with any OpenDeck-supported hardware.

![Weather conditions](https://img.shields.io/badge/conditions-sunny%20%7C%20cloudy%20%7C%20rain%20%7C%20snow%20%7C%20night-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![OpenDeck](https://img.shields.io/badge/OpenDeck-2.5%2B-orange)

---

## Features

- **Live conditions** pulled directly from your personal Weather Underground station
- **Dynamic weather backgrounds** — the button art changes automatically based on current conditions (sunny, partly cloudy, cloudy, rain, snow, night)
- **Fully customizable** — choose your own background color, text color, font size, and which data to display
- **Configurable refresh** — auto-refresh every 1, 2, 5, 10, 15, or 30 minutes, or manually on button press
- **Any WU station** — use your own PWS or any public station by ID
- **Imperial or metric** units
- Shows **temperature**, **humidity**, **precipitation rate**, and **location name**

---

## Screenshots

| Sunny | Rainy | Night | Cloudy |
|-------|-------|-------|--------|
| Blue sky + sun icon | Dark sky + raindrops | Dark sky + moon | Grey sky |

---

## Requirements

- [OpenDeck](https://github.com/nekename/OpenDeck) 2.5 or newer
- [Node.js](https://nodejs.org) 20.0 or newer (LTS recommended)
- A free [Weather Underground API key](https://www.wunderground.com/member/api-keys)
- A Weather Underground station ID (your own PWS or any public station)

---

## Installation

1. Download the latest `com.yourstation.wunderground.zip` from the [Releases](../../releases/latest) page
2. In OpenDeck, go to **Plugins → Install from file**
3. Select the downloaded `.zip` file
4. The **WU Temperature** action will appear in your actions list

---

## Setup

1. Drag the **WU Temperature** action onto any button
2. Click the button to open its settings panel
3. Enter your **Station ID** (e.g. `KNYIROND27`)
4. Enter your **Weather Underground API key**
5. The button will update automatically

### Getting your API key

1. Create a free account at [wunderground.com](https://www.wunderground.com)
2. Go to [wunderground.com/member/api-keys](https://www.wunderground.com/member/api-keys)
3. Copy your key and paste it into the plugin settings

### Finding a station ID

- Your own PWS station ID can be found in your Weather Underground dashboard
- To find a nearby public station, go to [wunderground.com/find](https://www.wunderground.com/find) and click any station on the map

---

## Settings

| Setting | Description |
|---------|-------------|
| **Station ID** | Any Weather Underground PWS station ID |
| **API Key** | Your WU API key |
| **Units** | Imperial (°F) or Metric (°C) |
| **Temperature Size** | Font size slider from 16 to 40px |
| **Show Location** | Display the station neighborhood name |
| **Show Humidity** | Display humidity percentage |
| **Show Precip Rate** | Display precipitation rate (only shown when raining/snowing) |
| **Auto Refresh** | How often to pull new data (1–30 min, or manual only) |
| **Background** | Weather-based auto, black, dark grey, or custom color |
| **Text Color** | Auto, white, black, or custom color |

---

## Weather Conditions

The background and icon update automatically based on live station data:

| Condition | Detection |
|-----------|-----------|
| ☀️ Sunny | Daytime, high solar radiation, low humidity |
| ⛅ Partly Cloudy | Daytime, moderate solar radiation or humidity |
| ☁️ Cloudy | Daytime, low solar radiation |
| 🌧️ Rainy | Precipitation rate > 0, temp above freezing |
| ❄️ Snowy | Precipitation rate > 0, temp at or below 33°F |
| 🌙 Night | Local time between 8pm and 6am |

---

## License

MIT — free to use, modify, and distribute. Contributions welcome!

---

*Built for the OpenDeck community. Not affiliated with Weather Underground or IBM.*
