# 🌡️ Arduino-Based Temperature Monitoring and Alert System

## 📌 Project Overview
This project demonstrates an **Arduino-based temperature monitoring and alert system** using an **NTC analog temperature sensor** and a **buzzer**.  
The system continuously monitors environmental temperature and provides an **audio alert** whenever the temperature crosses a predefined safe limit.

Such systems are widely used in **industrial safety**, **equipment protection**, **home automation**, and **environmental monitoring applications**.

---

## 🎯 Project Objectives
- To interface an **NTC analog temperature sensor** with Arduino  
- To continuously monitor temperature variations  
- To trigger a **buzzer alert** during high-temperature conditions  
- To display real-time sensor values and system status on the **Serial Monitor**

---

## 🔧 Components Used
- Arduino UNO  
- NTC Temperature Sensor (Analog)  
- Buzzer  
- Jumper Wires  
- Wokwi Arduino Simulator  

---

## 🔌 Hardware Connections

### 🔹 NTC Temperature Sensor
| Sensor Pin | Arduino Pin |
|----------|------------|
| VCC (Red) | 5V |
| GND (Black) | GND |
| Signal (Green) | A0 |

### 🔹 Buzzer
| Buzzer Pin | Arduino Pin |
|-----------|-------------|
| Positive (+) | Digital Pin 8 |
| Negative (–) | GND |

---

## ⚙️ System Working Principle
- The NTC temperature sensor varies its resistance based on temperature.
- As **temperature increases**, the **analog output value decreases**.
- Arduino reads this analog value through pin **A0**.
- A **threshold value** is defined in the program to identify high-temperature conditions.

### Decision Logic:
- If sensor value **drops below the threshold** → **High Temperature → Buzzer ON**
- If sensor value **stays above the threshold** → **Normal Temperature → Buzzer OFF**

---

## 🧠 Core Logic
```cpp
if (sensorValue < threshold) {
  buzzer ON;
} else {
  buzzer OFF;
}
