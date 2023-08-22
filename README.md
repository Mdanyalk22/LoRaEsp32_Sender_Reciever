# LoRaEsp32_Sender_Reciever
LoRa Receiver with OLED Display - README

This repository contains Arduino code for a LoRa receiver with an OLED display. The receiver listens for LoRa packets and displays received data along with RSSI (Received Signal Strength Indicator) information on an OLED screen.
Table of Contents

 1   Introduction
 2   Components
 3   Wiring
 4   Setup
 5  Adjusting Parameters
 6    License

1. **Introduction**

This Arduino sketch is designed to work with LoRa devices using the SX1278 module. The code sets up a LoRa receiver, which listens for incoming packets and extracts data from them. The extracted data is then displayed on an SSD1306 OLED screen along with the RSSI information.
Components
2. **Components**
    Arduino board (e.g., Arduino Uno, Arduino Nano)
    SX1278 LoRa module
    SSD1306 OLED display

3.**Wiring**

Before uploading the code, make sure to wire the components correctly:

    SCK: Connect to GPIO5 on the LoRa module
    MISO: Connect to GPIO19 on the LoRa module
    MOSI: Connect to GPIO27 on the LoRa module
    SS (CS): Connect to GPIO18 on the LoRa module
    RST: Connect to GPIO23 on the LoRa module
    DI0 (IRQ): Connect to GPIO26 on the LoRa module
    SDA: Connect to SDA on the OLED display
    SCL: Connect to SCL on the OLED display

Additionally, connect VCC and GND pins of both the LoRa module and OLED display to the appropriate power sources.
Setup

    Clone or download this repository to your computer.
    Open the LoRa_Receiver_OLED.ino file using the Arduino IDE.
    Install the necessary libraries:
        SPI
        LoRa
        Wire
        SSD1306
    Connect your Arduino board to your computer using a USB cable.
    Select the appropriate board type and port in the Arduino IDE.
    Upload the sketch to your Arduino board.

5.**Adjusting Parameters**

In the sketch, you can adjust the following parameters according to your requirements:

    BAND: Set the desired LoRa frequency band in Hertz (e.g., 433E6 for 433MHz band).
    Spreading Factor and Signal Bandwidth: The lines LoRa.setSpreadingFactor(12) and LoRa.setSignalBandwidth(125E3) set the spreading factor and signal bandwidth, respectively. Adjust these values based on your application's requirements.
    LoRa.setTxPower(-14): Set the LoRa transmission power level. Adjust this value based on your specific use case.

6. **License**

This code is provided under the MIT License.

Feel free to modify this template to better suit your audience and your specific use case. Don't forget to include any additional information that might be relevant, such as troubleshooting tips or links to further resources.
