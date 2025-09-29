# ESP32 Blynk + BLE Car 🚗

An ESP32-based smart car project with **dual-mode control**:
- **Wi-Fi Mode** → Controlled via Blynk IoT app (virtual pins for motor, lights, buzzer, battery, Wi-Fi RSSI).
- **BLE Mode** → Controlled via Bluetooth commands (`F`, `B`, `L`, `R`, `S`).

## ✨ Features
- Forward / Backward / Left / Right motor control
- Headlight & Buzzer control (Blynk or BLE)
- Battery percentage monitoring
- Wi-Fi signal strength reporting
- Dual mode switching (Wi-Fi / BLE)

## 🛠 Hardware Required
- ESP32 development board
- L298N Motor Driver
- 4 DC motors (BO motors)
- Car chassis
- Battery pack (7.4V–12V)
- Buzzer
- LED (Headlights)

## ⚡ Circuit Diagram
![Circuit Diagram](diagrams/wiring_diagram.png)

### Wiring:
- **ESP32 → L298N Motor Driver**
  - IN1 → GPIO 14
  - IN2 → GPIO 27
  - IN3 → GPIO 26
  - IN4 → GPIO 25
- **Buzzer** → GPIO 32
- **Headlight LED** → GPIO 33
- **Battery voltage sense** → GPIO 34
- **Mode switch** → GPIO 13 (LOW = Wi-Fi, HIGH = BLE)

## 📲 Blynk Setup
- Template ID: `TMPL3GNtZJ5Jo`
- Template Name: `CAR`
- Virtual Pins:
  - V1: Forward
  - V2: Backward
  - V3: Left
  - V4: Right
  - V5: Battery %
  - V6: Wi-Fi RSSI
  - V7: Buzzer
  - V8: Headlights

## ▶️ Getting Started
1. Clone this repo.
2. Open `ESP32_Blynk_BLE_Car.ino` in Arduino IDE / PlatformIO.
3. Install required libraries:
   - `Blynk`
   - `WiFi`
   - `BluetoothSerial`
4. Upload to ESP32.
5. Connect via Blynk app or BLE.

---
