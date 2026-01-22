****🌦️ Smart Weather and Power Consumption Monitoring System**

An ESP32-based IoT real-time monitoring system that tracks weather parameters and electrical power consumption, publishes data via MQTT, and provides live visualization and control through dashboards like Node-RED.

🚀 Project Overview

This project integrates environmental monitoring and energy management into a single embedded system. It continuously measures weather conditions and electrical parameters, enabling real-time analytics, remote monitoring, and intelligent control.

Designed for smart homes, smart buildings, and industrial IoT applications.

🔧 Features
🌡️ Weather Monitoring

Temperature & Humidity (DHT22)

Air Quality / Gas Level (MQ135)

⚡ Power & Energy Monitoring

Voltage, Current, Power & Energy (PZEM004T v3.0)

Real-time Power Consumption

Energy Cost Calculation (kWh-based)

Power Factor & Frequency Monitoring

📡 IoT & Communication

ESP32 with Wi-Fi connectivity

MQTT-based real-time data publishing

Node-RED dashboard integration

Bi-directional control (Load/Bulb ON-OFF)

🖥️ Display & Interface

20x4 I2C LCD for local data visualization

Live updates without refresh

Status indicators and alerts

🧠 System Architecture
Sensors → ESP32 → MQTT Broker → Node-RED Dashboard
              ↓
           I2C LCD

🧰 Hardware Components
Component	Description
ESP32-WROOM-32	Main Microcontroller
DHT22	Temperature & Humidity Sensor
PZEM004T v3.0	Voltage, Current & Energy Meter
20x4 I2C LCD	Local Display
Relay Module	Load Control
🧑‍💻 Software Stack

Arduino IDE

ESP32 Board Package

MQTT (EMQX / Mosquitto / HiveMQ)

Node-RED / mqtt panel app

Embedded C / C++

📂 Project Structure
Smart-Weather-and-Power-Consumption-Monitoring-System/
│
├── src/
│   ├── main.ino
│   ├── sensors.h
│   ├── mqtt_handler.h
│   ├── lcd_display.h
│
├── docs/
│   ├── block_diagram.png
│   ├── circuit_diagram.png
│
├── node-red/
│   └── flow.json
│
├── README.md
└── LICENSE

🔌 MQTT Topics (Example)
#define TEMP_TOPIC         "esp32/home584/temp"
#define HUMI_TOPIC         "esp32/home584/humi"
#define VOLTAGE_TOPIC      "esp32/home584/voltage"
#define CURRENT_TOPIC      "esp32/home584/current"
#define POWER_TOPIC        "esp32/home584/power"
#define ENERGY_TOPIC       "esp32/home584/energy"
#define FREQUENCY_TOPIC    "esp32/home584/frequency"
#define PF_TOPIC           "esp32/home584/pf"
#define COST_TOPIC         "esp32/home584/cost"
#define POWER_STATUS_TOPIC "esp32/home584/power_status"
#define LED1_CONTROL_TOPIC "esp32/home584/led1"
#define LED2_CONTROL_TOPIC "esp32/home584/led2"
#define LED1_STATUS_TOPIC  "esp32/home584/led1/status"
#define LED2_STATUS_TOPIC  "esp32/home584/led2/status"
#define RESET_ENERGY_TOPIC "esp32/home584/reset_energy"

📊 Dashboard Preview

Live gauges for voltage, current, power

Line charts for energy consumption

Toggle switch for load control

Alerts for abnormal conditions

🛠️ Installation & Setup

Clone the repository

git clone https://github.com/your-username/Smart-Weather-and-Power-Consumption-Monitoring-System.git


Open the project in Arduino IDE

Install required libraries:

DHT Sensor Library

PZEM004Tv30

PubSubClient

LiquidCrystal I2C

Configure:

Wi-Fi credentials

MQTT broker details

Energy tariff rate

Upload code to ESP32

🎯 Applications

Smart Home Energy Monitoring

Industrial Power Analytics

Weather Stations

IoT Learning & Research Projects

Academic Final-Year Projects

📈 Future Enhancements

Web-based dashboard

Cloud storage & analytics

Mobile app integration

AI-based energy prediction

OTA firmware updates

👨‍💻 Author

Yuvaraj-Embeded-Systems-32
Embedded Systems | IoT | ESP32 | STM32 | Arduino
