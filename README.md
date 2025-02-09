<h1 align="center">ESP32 2.4GHz Jammer by KEI</h1>

![Insert Image of ESP32 Jammer Here](https://github.com/KEI4251/ESP32-Jammer-/blob/files/imgs/esp32%20jammer.jpg)

### ⚠️ NOTE: This project is for **educational purposes only**. Signal jamming is **illegal** in many regions. Use responsibly and comply with local laws. ⚠️

<h4 align="center">
  <a href="https://github.com/KEI4251/ESP32-Jammer-/blob/main/README.md#kei-24ghz-jammer-overview">📌 Overview</a>
    <span> | </span>
  <a href="https://github.com/KEI4251/ESP32-Jammer-/blob/main/README.md#required-components">🛠️ Required Components</a>
    <span> | </span>
  <a href="https://github.com/KEI4251/ESP32-Jammer-/blob/main/README.md#gpio-pin-layout-for-esp32-and-nrf24">🔌 GPIO Pin Layout</a>
    <span> | </span>
  <a href="https://github.com/KEI4251/ESP32-Jammer-/blob/main/README.md#web-flasher">💻 Web Flasher</a>
</h4>

### KEI 2.4GHz Jammer Overview
the **KEI 2.4GHz Jammer** operates in the 2.4 GHz frequency range, utilizing an **ESP32** and **nRF24 PA LNA** module to interfere with signals within this band. It is capable of disrupting various wireless communications, including **Bluetooth**, **BLE (Bluetooth Low Energy)**, **Wi-Fi**, and **RC (Remote Control) drones**.

The jammer works by transmitting noise signals on the 2.4 GHz frequency, overpowering or disrupting the normal communication signals of devices within range. It offers four different operational modes: Bluetooth, BLE, Wi-Fi, and RC drones, allowing you to target specific types of devices.

Keep in mind that the range of the jammer may vary depending on the environment and equipment used. By equipping the device with a high-gain antenna or an RF amplifier, the effective range of interference can be significantly extended, allowing it to disrupt signals over longer distances.

> **Warning:** Use for educational purposes only. Always ensure you're complying with local regulations when using devices that transmit RF signals.

## Required Components

- 1x ESP32-WROOM-32U
- 2x nRF24L01 PA/LNA Module
- Prototype Pcb board
- Jumper wires
- 10uF Capacitors for stable operation (optional but recommended)
- 3.7v battery (optional)
- spdt swtich (optional)
- lx-lcbst 5v boost battery changer (optional)

## GPIO Pin Layout for ESP32 and nRF24

### HSPI
| nRF24L01 | HSPI Pin (ESP32) | 10uf Capacitor |
|----------|------------------|-----------------|
| VCC      | 3.3V             | (+) Capacitor  |
| GND      | GND              | (-) Capacitor  |
| CE       | GPIO 16          |                 |
| CSN      | GPIO 15          |                 |
| SCK      | GPIO 14          |                 |
| MOSI     | GPIO 13          |                 |
| MISO     | GPIO 12          |                 |
| IRQ      |                  |                 |

### VSPI
| nRF24L01 | VSPI Pin (ESP32) | 10uf Capacitor |
|----------|------------------|-----------------|
| VCC      | 3.3V             | (+) Capacitor  |
| GND      | GND              | (-) Capacitor  |
| CE       | GPIO 22          |                 |
| CSN      | GPIO 21          |                 |
| SCK      | GPIO 18          |                 |
| MOSI     | GPIO 23          |                 |
| MISO     | GPIO 19          |                 |
| IRQ      |                  |                 |

### Battery modification (Optional)
| 3.7V Li-Ion battery | LX-lcbst 5v Charging Module | Mini Slide Switch | ESP32 |
|---------------------|-----------------------------|-------------------|-------|
| (+) Battery         | Bat +                       |                   |       |
| (-) Battery         | Bat -                       |                   |       |
|                     | OUT +                       | Switch in         |       |
|                     | OUT -                       |                   |  GND  |
|                     |                             | Switch out        |  5V  |
## nRF24L01 and ESP32 Images

![Insert Image of nRF24L01 Here](https://github.com/KEI4251/ESP32-Jammer-/blob/files/imgs/nRF24L01%20pin%20out.png)

![Insert Image of ESP32 Here](https://github.com/KEI4251/ESP32-Jammer-/blob/files/imgs/esp32%20wroom32%20u%20picture.jpeg)

## Web Flasher

To easily flash the ESP32 with the KEI Jammer firmware, visit the [Web Flasher](https://kei4251.github.io/ESP32-Jammer-/).

![Insert Screenshot of Web Flasher Here](https://github.com/KEI4251/ESP32-Jammer-/blob/files/imgs/WEBFLASHER.png)

### How to Use the Web Flasher

1. **Open the Web Flasher**: Go to the [Web Flasher](https://kei4251.github.io/ESP32-Jammer-/) link.
2. **Connect Your ESP32**: Make sure your ESP32 is connected to your computer using a USB cable.
3. **Select Firmware**: Click on the firmware you want to install from the available options.
4. **Choose the COM Port**: If your ESP32 is not already selected, choose the correct COM port where your device is connected.
5. **Start Flashing**: Press the "Flash" button to begin flashing the firmware onto the ESP32. Wait until the process is complete.
6. **Done**: Once the flashing is done, the ESP32 will restart and will be ready to use with the new firmware.

### If ESP32 Doesn't Appear in COM Port

If your ESP32 doesn't show up in the COM port list, you will need to install the appropriate driver for your ESP32 board. 

1. **Download the Driver**: Visit the link below to download the driver.
   - [ESP32 Driver Download](insert-your-link-here)
   
2. **Install the Driver**: Follow the installation instructions for your operating system. Make sure to restart your computer after installing the driver.

3. **Reconnect the ESP32**: After installation, reconnect your ESP32 to your computer. It should now appear in the COM port list when you go back to the Web Flasher.

## Warning

⚠️ **Warning:**  
This tool is for educational purposes only. Use it at your own risk! The creator is not responsible for any damage or misuse caused by this tool.

## Additional Notes

- Ensure that the ESP32 and nRF24L01 are wired correctly before flashing the firmware.
- This tool is designed to work with the KEI Jammer firmware for the ESP32.
- Follow the provided GPIO pin layout for both the HSPI and VSPI configurations to ensure proper operation.

---
