# 🌱 AgroSense: Arduino-Based Smart Agriculture & Environmental Monitoring System

## 📌 Project Overview

**AgroSense** is an Arduino-based multi-sensor monitoring system designed to monitor important environmental and farm conditions.

The project uses a **Soil Moisture Sensor, DHT11, PIR Sensor, and LDR** to collect different types of information. The readings and sensor status are displayed on a **16×2 I2C LCD**.

The system also uses an LED that responds to the LDR sensor based on the detected light condition.

---

## 🎯 Objectives

* Monitor soil moisture level.
* Measure temperature and humidity.
* Detect movement using a PIR sensor.
* Detect light conditions using an LDR.
* Display sensor information on an LCD.
* Control an LED according to the light condition.
* Gain practical experience in sensor interfacing and Arduino programming.

---

## 🛠️ Components Used

| Component            | Purpose                           |
| -------------------- | --------------------------------- |
| Arduino              | Main microcontroller              |
| Soil Moisture Sensor | Detects soil moisture level       |
| DHT11                | Measures temperature and humidity |
| PIR Sensor           | Detects motion                    |
| LDR Sensor           | Detects light condition           |
| 16×2 I2C LCD         | Displays sensor information       |
| LED                  | Indicates/control based on LDR    |
| Jumper Wires         | Connections                       |
| Breadboard           | Circuit prototyping               |

---

## 🔌 Pin Connections

| Component            | Arduino Pin |
| -------------------- | ----------- |
| Soil Moisture Sensor | D4          |
| PIR Sensor           | D2          |
| LDR Sensor           | D7          |
| LED                  | D8          |
| DHT11 Data           | A0          |
| LCD SDA              | A4          |
| LCD SCL              | A5          |

> **Note:** The I2C LCD uses the Arduino's I2C pins. For an Arduino Uno, SDA = A4 and SCL = A5.

---

## ⚙️ Working Principle

The system continuously checks the connected sensors.

### 1. 🌱 Soil Moisture Monitoring

The soil moisture sensor is connected to **digital pin D4**.

The Arduino reads its digital output and displays the soil moisture status on the LCD.

Example:

```text
SML is high
```

or

```text
SML level is low
```

---

### 2. 🚶 PIR Motion Detection

The PIR sensor is connected to **D2**.

When motion is detected, the LCD displays:

```text
Motion detected
```

When there is no motion:

```text
No Motion dected
```

---

### 3. 🌡️ Temperature & Humidity Monitoring

The **DHT11 sensor** is connected to **A0**.

The Arduino reads:

* Temperature
* Humidity

The LCD displays both values.

Example:

```text
Temp: 28.00C
Humidity: 65.00%
```

---

### 4. 💡 LDR-Based Light Detection

The LDR is connected to **D7** and the LED is connected to **D8**.

The Arduino reads the LDR's digital output and controls the LED accordingly.

This demonstrates basic **automatic light control** using a sensor.

---

## 🖥️ LCD Display

The LCD is used to display the sensor information one after another.

The system displays:

1. Soil moisture status
2. PIR motion status
3. Temperature and humidity

Each screen is displayed for approximately **2 seconds**.

---

## 💻 Software & Technologies

* **Arduino IDE**
* **Embedded C/C++**
* **Arduino**
* **I2C Communication**
* **Sensor Interfacing**
* **Digital Input/Output**

### Libraries Used

```cpp
#include <LiquidCrystal_I2C.h>
#include <Wire.h>
#include <DHT.h>
```

---


## 🧠 Skills Demonstrated

This project helped me gain practical experience in:

* Arduino programming
* Embedded C/C++
* Sensor interfacing
* DHT11 interfacing
* PIR sensor interfacing
* LDR interfacing
* Soil moisture sensor interfacing
* I2C LCD interfacing
* Digital input/output
* Hardware debugging
* Combining multiple sensors in one embedded system

---

## 🔮 Future Improvements

The project can be further improved by adding:

* 📡 Wi-Fi connectivity using ESP32
* 📱 Mobile application monitoring
* ☁️ Cloud data storage
* 💧 Automatic water pump control
* 📊 Real-time sensor graphs
* 📩 SMS alerts
* 🌐 Remote farm monitoring
* 🔋 Solar-powered operation

---

## 👩‍💻 Author

**Rakshitha**

BE – Electronics & Communication Engineering

Interested in **Embedded Systems, Embedded C, Microcontrollers, and Electronics**.

---

## ⭐ Project Highlights

> A practical Arduino-based project demonstrating **multi-sensor interfacing, LCD communication, environmental monitoring, and automatic control** in an embedded system.

If you found this project useful, feel free to ⭐ the repository!
