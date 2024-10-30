# ESP8266 OTA Bootloader

## Overview

This project implements a basic Over-the-Air (OTA) bootloader for the NodeMCU (ESP8266). The bootloader allows for seamless firmware updates over Wi-Fi, enabling easy deployment of new features and bug fixes without physical access to the device.

## Features

- **Wi-Fi Connectivity**: Connects to a specified Wi-Fi network.
- **OTA Firmware Updates**: Supports Over-the-Air updates for new firmware.
- **Progress Monitoring**: Provides feedback during the update process.
- **Error Handling**: Notifies users of any errors encountered during updates.

## Requirements

### Hardware

- NodeMCU (ESP8266) development board

### Software

- Arduino IDE with ESP8266 board package installed
- `ESP8266WiFi`, `ESP8266WebServer`, `ArduinoOTA` libraries (included with ESP8266 board package)

## Setup Instructions

1. **Install Arduino IDE**:
   - Download and install the [Arduino IDE](https://www.arduino.cc/en/software).

2. **Install ESP8266 Board Package**:
   - Open the Arduino IDE.
   - Go to `File` > `Preferences`.
   - In the "Additional Board Manager URLs" field, add:
     ```
     http://arduino.esp8266.com/stable/package_esp8266com_index.json
     ```
   - Go to `Tools` > `Board` > `Board Manager`, search for "ESP8266", and install the package.

3. **Clone or Download the Repository**:
   - Clone this repository or download it as a ZIP file and extract it.

4. **Open the Code**:
   - Open the provided `.ino` file in the Arduino IDE.

5. **Configure Wi-Fi Credentials**:
   - In the code, replace `your_SSID` and `your_PASSWORD` with your actual Wi-Fi credentials.

6. **Upload Initial Code**:
   - Connect your NodeMCU to your computer.
   - Select the appropriate board and port in the Arduino IDE (`Tools` > `Board` > `NodeMCU 1.0 (ESP-12E Module)` and `Tools` > `Port`).
   - Click the upload button to upload the initial firmware.

## Usage

- Open the Serial Monitor to observe the connection status to the Wi-Fi network.
- Use the Arduino IDE to upload new firmware to the NodeMCU by selecting "Upload" while connected to the same network.
- The bootloader will handle the OTA update process and provide progress feedback.

## Error Handling

- If an error occurs during the update process, the bootloader will output the error code to the Serial Monitor, allowing for easier debugging.

## Future Enhancements

- **Custom Update Interface**: Create a web interface for manual firmware uploads.
- **Version Management**: Implement version checking to ensure compatibility of uploaded firmware.
- **More Robust Error Handling**: Expand error handling for better reliability during updates.

## License

This project is licensed under the MIT License. Feel free to modify and use the code for your own projects.
