
# BLE Configuration Web Interface for ESP32

This project is a browser-based user interface for configuring and communicating with an ESP32 device over Bluetooth Low Energy (BLE). It allows users to connect via Web Bluetooth, send real-time clock (RTC) settings, and update device preferences such as display timeout, slideshow interval, 12h/24h time format, and BLE device name.

## 🔧 Features
- Web Bluetooth-based BLE connection to ESP32
- Send current system time to ESP32 (`SETTIME`)
- Configure ESP32 settings via BLE:
  - BLE device name (`BLE_NAME`)
  - Slideshow interval in milliseconds (`interval`)
  - Display timeout in milliseconds (`screenTimeout`)
  - Time format: 24-hour or 12-hour (`is12hFormat`)
- Responsive and clean interface using HTML, CSS, and vanilla JavaScript
- Modal-based loading indicator for connection status

## 🧪 Requirements
- A browser that supports Web Bluetooth API (e.g., Chrome)
- ESP32 device with BLE services using:
  - Service UUID: `4fafc201-1fb5-459e-8fcc-c5c9c331914b`
  - Characteristic UUID: `beb5483e-36e1-4688-b7f5-ea07361b26a8`

## 🚀 How to Use
1. Open the web page in Google Chrome or another Web Bluetooth-compatible browser.
2. Click **"Connect BLE"** to pair with your ESP32 device.
3. Once connected, you can:
   - Click **"Send Time"** to synchronize time.
   - Configure settings and click **"Save Settings"** to apply.

## 📁 File Structure
```
index.html          # Main UI and BLE logic
/images/favicon.ico # Optional icon
```

## 📌 Notes
- Ensure your ESP32 firmware can parse the sent `SETTIME` and `SETCFG` commands.
- Works best over HTTPS or localhost due to Web Bluetooth restrictions.

## 👨‍💻 Author
Developed for use with the BayMax ESP32 Watch & Health Monitor Project.
