# PLC Water Tank Control System  

## 📌 Overview  
This project implements an automated water tank control system using a Siemens PLC programmed in ladder logic. The system simulates real-world water level management using push buttons as inputs and LEDs as outputs.  

---

## ⚙️ Tools & Technologies  
**PLC:** Siemens S7-200 / S7-1200  
**Software:** STEP 7 MicroWIN  
**Programming Language:** Ladder Logic (LAD)  

---

## 🧠 Working Principle  
The system automatically controls the water pump based on tank level conditions:  

- 🔽 Low Level Detected → Pump turns ON (tank starts filling)  
- 🔼 High Level Detected → Pump turns OFF (tank is full)  

Interlocking logic is used to ensure stable operation and prevent frequent switching or unsafe conditions.  

In the below demo:
- I0.0 is treated as a low level sensor. When it turns ON, LED Q0.2 turns ON. LED Q0.2 means that pump is ON.
- I0.1 is treated as a high level sensor. When it turns ON, LED Q0.0 turns ON meaning pump is OFF.
- I0.2 is used a reset button in case of emergencies.
- Interlocking is also implemented so that the pump or tank's safety is ensured.

---

## 🔌 Hardware Abstraction  
Push buttons are used to simulate water level sensors (Low Level & High Level), while LEDs represent system states such as pump ON/OFF and tank status. 

---

## 🔌 Inputs & Outputs  

### Inputs  
- Push Button → Low Level Sensor  
- Push Button → High Level Sensor  
- Push Button → Start / Stop Control  

### Outputs  
- Pump (simulated via LED)  
- Low Level Indicator LED  
- High Level Indicator LED  

---

## 🔄 Features  
- Water level control  
- Pump ON/OFF based on tank level  
- Interlocking logic to prevent overflow  
- Dry-run protection for pump safety  
- Fault handling for invalid sensor conditions  
- Structured and modular ladder logic design  

---

## 🎥 Demonstration  
*(Attach your demo video here)*  

---

## 📦 Repository Contents  
- PLC Program File  
- Project Documentation  
- Demo Video  

---

## 📁 Project File  
- `water_tank_control.mwp` → Complete Siemens PLC project (open in STEP 7 / MicroWIN)

---

## 🚀 Future Improvements  
- SCADA system integration for monitoring  
- IoT-based remote water level tracking  
- Analog level sensor (ultrasonic/pressure-based) integration  
- Alarm system for critical water levels  
