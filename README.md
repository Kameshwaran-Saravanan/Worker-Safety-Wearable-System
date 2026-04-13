

# 🛡️ Worker Safety Wearable System

An **embedded system project** designed to improve worker safety in hazardous environments such as construction sites, factories, and mines.

This is a **portable, real-time monitoring wearable device** that detects dangerous situations and provides **instant alerts**.

---

##  Features

*  Detects **worker falls**
*  Monitors **hazardous gas levels**
*  Provides **instant audio + visual alerts**
*  Works **offline (no internet required)**
*  Low-cost and scalable solution

---

##  Project Overview

The system continuously monitors:

* **Worker motion** using MPU6050
* **Environmental gas levels** using MQ-2 sensor

Based on sensor data, the system:

* Detects unsafe conditions
* Triggers alerts using **LEDs and buzzer**

---

##  Project Objectives

1. **Design a wearable embedded device**

   * Compact, battery-powered, portable
   * Continuous monitoring

2. **Detect accidental falls**

   * Uses accelerometer + gyroscope
   * Identifies sudden impact and abnormal tilt

3. **Monitor hazardous gases**

   * Detects smoke, LPG, combustible gases
   * Prevents suffocation and explosions

4. **Provide immediate alerts**

   * Buzzer (audio alert)
   * LEDs (visual indication)

5. **Build a low-cost solution**

   * ₹1000–₹2000 budget
   * Suitable for real-world deployment

---

##  Components Used

| Component                 | Function                          |
| ------------------------- | --------------------------------- |
| Arduino Nano              | Main controller                   |
| MPU6050                   | Motion detection (fall detection) |
| MQ-2 Sensor               | Gas detection                     |
| LEDs (Green, Yellow, Red) | Status indication                 |
| Buzzer                    | Audible alert                     |
| Jumper Wires              | Connections between components    |
| Resistors (220Ω)          | Protect LEDs                      |


---

##  System Working

### Step 1: Power ON

Battery powers Arduino and all components.

### Step 2: Initialization

Arduino initializes:

* MPU6050
* MQ-2 sensor
* LEDs and buzzer

### Step 3: Continuous Monitoring

* MPU6050 → monitors motion
* MQ-2 → monitors gas levels

### Step 4: Data Processing

* Gas value compared with threshold
* Acceleration calculated:

```cpp
totalAccel = sqrt(x*x + y*y + z*z);
```

### Step 5: Decision Logic

```text
IF fall detected:
    Yellow LED ON + Buzzer ON

ELSE IF gas detected:
    Red LED ON + Buzzer ON

ELSE:
    GREEN LED ON
```

---

##  Alert System

| Condition      | LED       | Buzzer | Meaning               |
| -------------  | --------- | ------ | --------------------- |
| Safe           | 🟢 Green  | OFF    | Normal condition      |
| Fall Detected  | 🟡 Yellow | ON     | Worker fallen         |
| Gas Detected   | 🔴 Red    | ON     | Hazardous gas present |

---

## 📸 Project Images

### 🟢 Normal Condition (Safe)

<img width="1301" height="1599" alt="image" src="https://github.com/user-attachments/assets/575d09cf-f1c9-4f18-816d-c9002403bc91" />


### 🔴 Gas Alert

<img width="1301" height="1599" alt="image" src="https://github.com/user-attachments/assets/09feaf41-1796-4bb0-be33-b252fae3b6b7" />



### 🟡 Fall Detection 

<img width="1500" height="1567" alt="image" src="https://github.com/user-attachments/assets/38443d37-de96-48dc-b135-818fcccbc5fb" />




### 🔧 Circuit Setup (No Alert)

<img width="983" height="847" alt="image" src="https://github.com/user-attachments/assets/0da97622-4d90-40f8-b57f-cbe626dba8c4" />



---



##  Outcomes

###  Technical

* Real-time embedded system
* Sensor integration + threshold logic

###  Safety

* Detects falls and toxic gases
* Provides instant alerts

###  Practical

* Low-cost (₹1k–₹2k)
* Portable and scalable
* Suitable for industrial use

---


## 🏁 Conclusion

This project demonstrates a **low-cost, real-time wearable safety system** that enhances worker protection by detecting falls and hazardous gases and providing **instant alerts without internet dependency**.

---

## 👨‍💻 Authors

* Kameshwaran Saravanan
* Asmita Pal

---

## 📌 How to Run

1. Connect all components as per circuit
2. Upload code using Arduino IDE
3. Power using Li-ion battery
4. Open Serial Monitor (9600 baud)
5. Observe system behavior

---

## ⭐ Final Note

> *A simple, scalable solution that can save lives in hazardous work environments.*

---

