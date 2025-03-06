

# LoRa-Speedlight-Trigger

This repository contains the CircuitPython code needed to use the USB Nugget and the LoRa Backpack to trigger a remote pin high or low using the RFM95 LoRa chip. For this specific project, I used a 5V relay to trigger a camera speedlight on and off, but the code can be adapted to control any variety of functions.

---
## Parts:

Electronics:  
	-[USB Nugget w/ LoLin ESP32 S3 Mini ](https://retia.io/products/bluetooth-nugget-esp32s3)  
	-[LoRa Backpack w/ RFM95W 915Mhz Module](https://retia.io/products/lora-breakout-for-usb-bluetooth-nugget)  
	-[5V DC Relay](https://a.co/d/1T0jNxT)  
	-[3.5mm to Flash Sync Cable](https://a.co/d/95ebfrs)  
	-Speedlight Camera Flash  

---
## Nugget Pinout:


| Nugget       | Pin  |
| ------------ | ---- |
| LEFT         | IO11 |
| RIGHT        | IO12 |
| UP           | IO13 |
| DOWN         | IO18 |
| A            | IO44 |
| B            | IO43 |
| SCK          | IO6  |
| MOSI         | IO8  |
| MISO         | IO7  |
| Neopixel     | IO10 |
| CS           | IO9  |
| RESET        | IO4  |
| SCL          | IO36 |
| SDA          | IO35 |
| CS_ACCESSORY | IO14 |

---
## Setup:

Step 1: Flash the Nugget with CircuitPython (Press "0" and then "Reset" to enter flashing mode)  
Step 2: Unzip and then drag and drop the receiver/transmitter files to your devices. Make sure to copy both the code.py and the lib folder  
Step 3: Connect the data in pin on the relay to the CS_ACCESSORY pin on the LoRa backpack  
Step 4: Press the "A" button on the transmitter to trigger the LoRa transmit function. The GPIO pin will be driven high/low on the receiver side on every packet received  
