<div align="center">

  <h1>⚡ Smart Energy Monitoring System ⚡</h1>
  
  <p>
    <b>Real-time Analytics • Energy Conservation • IoT Powered</b>
  </p>

  <p>
    <a href="#">
      <img src="https://robu.in/wp-content/uploads/2020/11/835800-3.jpg" alt="ESP32" width="150">
    </a>
    <a href="#">
      <img src="https://makerbazar.in/cdn/shop/files/PeacefairPZEM-004TACMulti-functionElectricEnergyMeteringPowerMonitor.jpg?v=1702982310" alt="PZEM-004T" width="150">
    </a> 
  </p>

</div>

---

## 📖 Overview

Welcome to my **first IoT project**! This system is designed to tackle the growing problem of energy wastage in homes and industries. By utilizing the **ESP32** microcontroller and the high-precision **PZEM-004T** module, this project monitors electrical parameters in real-time.

The data collected helps users analyze consumption patterns, identify power-hungry devices, and take actionable steps to reduce their carbon footprint and electricity bills.

---

## 🌟 Key Features

<table>
  <tr>
    <td align="center">
      <h3>📊<br>Real-Time Tracking</h3>
      <p>Instant visualization of Voltage, Current, Power, and Energy consumption.</p>
    </td>
    <td align="center">
      <h3>🌐<br>IoT Connectivity</h3>
      <p>Seamless WiFi integration to push data to the Cloud.</p>
    </td>
  </tr>
  <tr>
    <td align="center">
      <h3>🛡️<br>Non-Invasive</h3>
      <p>Uses a Split-Core CT sensor for safe and easy installation on main lines.</p>
    </td>
    <td align="center">
      <h3>📉<br>Wastage Control</h3>
      <p>Analyze historical data to detect anomalies and cut down on waste.</p>
    </td>
  </tr>
</table>

---

## 🛠️ Hardware Stack

<div align="center">
  <table>
    <thead>
      <tr>
        <th align="center">Component</th>
        <th align="center">Role</th>
        <th align="center">Spec</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td align="center"><b>ESP32 Dev Kit</b></td>
        <td align="center">Main Controller & WiFi</td>
        <td align="center">30 Pins, 2.4GHz WiFi</td>
      </tr>
      <tr>
        <td align="center"><b>PZEM-004T v3.0</b></td>
        <td align="center">AC Metering Module</td>
        <td align="center">80-260V AC, 100A</td>
      </tr>
      <tr>
        <td align="center"><b>CT Sensor</b></td>
        <td align="center">Current Sensing</td>
        <td align="center">Split Core Coil</td>
      </tr>
    </tbody>
  </table>
</div>

---

## 🔌 Circuit Connection

> **⚠️ SAFETY WARNING:** Working with AC Mains (110V/220V) is extremely dangerous. Ensure the main power is **OFF** before clamping the sensor or touching the AC side of the module.

The **PZEM-004T** communicates with the **ESP32** via Serial (UART).

| PZEM Pin | ESP32 Pin | Note |
| :--- | :--- | :--- |
| **VCC** | VIN | Power source |
| **GND** | GND | Common Ground |
| **TX** | GPIO 17 (RX2) | Data Out from Sensor |
| **RX** | GPIO 16 (TX2) | Data In to Sensor |

<div align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRqIzY9RWIOnNU2OilvTlhWaa78e7TpWg1yDQ&s" alt="Wiring Diagram" width="500">
  <p><i>Figure: Basic Wiring Diagram for ESP32 and PZEM-004T</i></p>
</div>

---

## 💻 Getting Started

### 1. Prerequisites
* Install **Arduino IDE**.
* Install **ESP32 Board Manager** in Arduino IDE.

### 2. Required Libraries
Install the following via Arduino Library Manager (`Ctrl+Shift+I`):
* `PZEM004Tv30` (by Mandulaj)

### 3. Installation
1.  Clone this repository:
    ```bash
    git clone [https://github.com/bansalmannatbansal/AC-Energy-Monitering-System.git](https://github.com/bansalmannatbansal/AC-Energy-Monitering-System.git)
    ```
2.  Open `EnergyMonitor.ino` in Arduino IDE.
3.  Update your WiFi credentials:
    ```cpp
    const char* ssid = "YOUR_WIFI_SSID";
    const char* password = "YOUR_WIFI_PASS";
    ```
4.  Upload to your ESP32 board!

---

## 🔮 Future Roadmap

* [ ] Add **Relay Control** to turn off devices remotely.
* [ ] Integrate **Home Assistant** via MQTT.
* [ ] Create a custom **Web Server** interface.
* [ ] Add **Cost Calculation** (Currency/kWh).

---

## 🤝 Contribution

This is an open-source learning project! If you have ideas to improve the code or efficiency, feel free to **fork** this repo and submit a **pull request**.

<div align="center">
  <p>Created by <b>Mannat Bansal<b></p>
</div>
