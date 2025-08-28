# 🚗 Driver Anti-Sleep Detection System  

An **Arduino-powered safety system** designed to detect driver drowsiness using an **eye-blink sensor** and prevent accidents by triggering alerts and controlling motorized components.  

---

## 📌 Features  
- 👁️ **Eye-Blink Sensor** detects driver drowsiness in real-time.  
- 🔔 **Buzzer Alarm** alerts the driver when eyes remain closed.  
- ⚡ **Relay Module** controls current flow between Arduino (5V) and external battery (9V).  
- 🔄 **Motorized Wheel Control** stops/starts based on driver activity.  
- 🔋 **Dual Power Supply** (two 9V batteries) for motor and buzzer/switch separation.  
- 🔒 **Safe Circuit Design** with isolated grounds for sensor/battery/relay and buzzer.  

---

## ⚙️ Hardware Components  
- Arduino UNO  
- Eye-Blink Sensor  
- Relay Module (1-channel, SPDT)  
- Buzzer  
- BO Motor + Wheels  
- Switch  
- Two 9V Batteries  
- Jumper Wires  

---

## 🔌 Circuit Explanation  
- Eye-blink sensor **GND → Arduino GND**, **VCC → 5V**, **OUT → D2**.  
- Relay module **GND → Arduino GND**, **VCC → Arduino 5V**, **IN → D8**.  
- Buzzer **– → Arduino GND**, **+ → D9**.  
- Wheel powered by **separate 9V battery**, connected via relay.  
- Switch connected between **battery and Arduino 5V**.  
- Two GND pins used separately: one for **sensor/relay/battery**, another for **buzzer**, ensuring independent operation.  
- **Flow of data:** `Eye Sensor (D2) → Arduino → Relay (D8) → Motor`.  

---

## 🚀 How It Works  
1. Driver wears the **eye-blink sensor**.  
2. If the eyes close for longer than a safe threshold, the sensor sends a signal to Arduino.  
3. Arduino activates the **buzzer** (warning the driver) and controls the **relay module** to stop the wheel.  
4. System resets when the driver’s eyes open again.  

---

## 🛠️ Skills Demonstrated  
- Embedded Systems  
- Sensor Integration  
- IoT Safety Systems  
- Circuit Design  
- Hardware-Software Interfacing  

---


## 📜 License  
This project is open-source and available under the MIT License.  

