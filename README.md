# ESP32 LoLin32 Lite Lora Shield for RFM95 or RN2483

This shield is used to hold LoRa modules such as HopeRF [RFM95][4] or Mictrochip [RN2483][7] with WeMos ESP32 [LoLin32-Lite][22] boards it has the followong features:
- I2C Pullups placement
- Classic I2C connector with SCL/SDA and 3V3/GND reversable pin by solder pad
- Groove I2C connector
- Footprint for RFM95/96/98 or RN2483/RN2903 Lora module
- Footprint for choosing single Wire, SMA or u-FL Antenna type 
- 1 x WS2812B Type LED for visual indication
- 1 x Push Button
- Added footprint for Microchip 24AA02E64 64 bits serial number (DEVEUI)

Take care that WeMos has different Lolin32 boards, you need the [Lite][22] model. They Provide WeMos [Lolin32][20], [Lolin32 Pro][21] or this one [Lolin32 Lite][22]

You can also check the shield for the [Lolin32 (not Lite)][9] classic version. 

# Detailed Description

Look at the schematics for more informations.

SPI connexion is classic (MOSI/MISO/CLK), 

Other pins that may need be adapted into code (for example if you use TTN network gateway code) according to the following pinout

```
Lolin32-Lite   RFM9x Module
  IO5   <-------> SEL 
  IO19  <-------> MISO
  IO23  <-------> MOSI
  IO18  <-------> CLK
  IO27  <-------> DIO0
  IO26  <-------> DIO1
  IO4   <-------> DIO2
  IO25  <-------> RST
  IO35  <-------> DIO5

Lolin32-Lite   RN2xx3 Module
  IO4   <-------> RESET
  IO25  <-------> RX
  IO35  <-------> TX

Lolin32-Lite   Shield Feature
  IO12  <-------> I2C SCL
  IO14  <-------> I2C SDA
  IO13  <-------> WS2812 LEDS
  IO15  <-------> Push Button


Lolin32-Lite Free I/O
  IO0  -> Also used for Flash
  IO2 
  IO16 
  IO17
  IO22 -> On Board LoLin32-Lite LED
  IO32
  IO33 
  IO34 
```

**Do not forget to join (solder) the correct LoRa antenna trace** depending on module you place (RFM95 or RN2483), see picture below.

<img src="https://github.com/hallard/LoLin32-Lora/raw/master/pictures/LoLin32-Lora-Solder-Pad-Antenna.jpg" alt="Antenna Solder Pad">

And as classic advice, **connect the LoRa antenna before powering** the board to avoid any damage to LoRa module

# Schematic  

<img src="https://github.com/hallard/LoLin32-Lite-Lora/raw/master/pictures/LoLin32-Lite-Lora-sch.png">

# Firmware  

There is no firmware available, but you can have a large demo of features and a full working LoRa node (with RFM95) with this excellent [ESP32-Paxcounter](https://github.com/cyberman54/ESP32-Paxcounter/) software, it's a must see.

# Boards  

<img src="https://github.com/hallard/LoLin32-Lite-Lora/raw/master/pictures/LoLin32-Lite-Lora-top.png" alt="Top">&nbsp;
<img src="https://github.com/hallard/LoLin32-Lite-Lora/raw/master/pictures/LoLin32-Lite-Lora-bot.png" alt="Bottom">

You can order the PCB of this board at [PCBs.io][8]. PCBs.io give me some reward when you order my designed boards from their site. This is pretty good, because I can use these rewards to create and design new boards and order them for free, so if you don't care about PCB manufacturer please use PCBs.io.

# Assembled boards (TBD)

Not assembled yet but you can see approx what it looks like with the [Lolin32 (not Lite)][9] version. 

## With RFM95

<img src="https://github.com/hallard/LoLin32-Lora/raw/master/pictures/LoLin32-Lora-RFM95-Assembled.jpg" alt="LoraNode32 with RFM95">

## With RN2483

<img src="https://github.com/hallard/LoLin32-Lora/raw/master/pictures/LoLin32-Lora-RN2483-Assembled.jpg" alt="LoraNode32 with RN2483">

# License

<img alt="Creative Commons Attribution-NonCommercial 4.0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png">   

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/)    
If you want to do commercial stuff with this project, please contact [CH2i company](https://ch2i.eu/en#support) so we can organize an simple agreement.

# Misc

See news and other projects on my [blog][2] 
 
[2]: https://hallard.me
[3]: https://PCBs.io/share/zO3Ye
[4]: http://www.hoperf.com/rf_transceiver/lora/
[5]: https://github.com/hallard/ESP-1ch-Gateway/
[6]: https://github.com/matthijskooijman/arduino-lmic/pull/34
[7]: https://www.microchip.com/wwwproducts/en/RN2483
[8]: https://PCBs.io/share/4Qvx1
[9]: https://github.com/hallard/LoLin32-Lora

[10]: http://www.banggood.com/WeMos-LOLIN32-V1_0_0-WiFi-Bluetooth-Board-Based-ESP-32-4MB-FLASH-p-1164252.html

[20]: https://wiki.wemos.cc/products:lolin32:lolin32
[21]: https://wiki.wemos.cc/products:lolin32:lolin32_pro
[22]: https://wiki.wemos.cc/products:lolin32:lolin32_lite
