# ESP32 - Smart Plant Monitoring & Automatic Watering System

A system that monitors temperature, humidity, soil moisture, and automatically waters plants using ESP32.  
Data is displayed on LCD and sent to mobile app Blynk.

## Features
- Measure environmental temperature & humidity (DHT11)
- Measure soil moisture
- Display data on LCD
- WiFi connectivity for remote monitoring
- Automatic watering based on soil moisture threshold
- Manual pump control via app

---

##  Wiring Diagram

| ESP32 Pin | Component |
|---|---|
| 3V3 | VCC DHT + Soil Sensor |
| GND | GND DHT + Soil + Relay |
| GPIO 14 | DHT Data |
| GPIO 34 | Soil Analog Output (A0) |
| GPIO 25 | Relay control |
| SDA (21) | LCD SDA |
| SCL (22) | LCD SCL |


##  Arduino Libraries Required

- WiFi.h
- DHT sensor library
- Adafruit Unified Sensor
- LiquidCrystal_I2C or Adafruit_SSD1306
- Blynk (if using app)

---

## Watering Logic
- If soil moisture `< 45%` → **Pump ON**
- If soil moisture `>= 55%` → **Pump OFF**

---

## Future Improvements
- MQTT + Home Assistant integration
- Firebase Realtime Database
- ESP32 Web Dashboard (no app needed)
- Telegram/Zalo notifications

