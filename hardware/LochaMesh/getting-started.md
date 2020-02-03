
Before getting started with its recommended to first read the readme: https://github.com/MeshedPotato/Project-Plans/blob/master/hardware/LochaMesh/README.md

To get (dev) node running we need to install the [Turpial firmware](https://github.com/btcven/turpial-firmware/) on the dev board (ESP32), after that we can setup the radio board (CC1312R1) with the right firmware and then connect both of the boards.

# 356-ESPWROVER-KIT-VB (ESP32)

## windows

### Install ESP-IDF
- Download: https://dl.espressif.com/dl/esp-idf-tools-setup-2.2.exe
- Install esp-idf-tools-setup-2.2.exe
- When prompted choose release/v4.0 (release branch)

### Clone Turpial firmware

### Open ESP-IDF Command Prompt (cmd.exe) (From start menu)
- `cd [turpial repo directory]`
- `idf.py build`
- Keep this Command Prompt open

### Check jumpers on ESP32
- The jumpers lister here should be in place
  - RDX - TXD0
  - TDX - RXD0
  - USB_5V (alligned with the USB_5V text)

### Plug ESP32 in pc with usb cable

### Switch on device

### Go to ESP-IDF Command Prompt (that was left open)
- `idf.py flash`
- If only one ESP is connected it should start flashing
- If there are multiple connected ESPs you might have to specify a port
- (To find out which ones are in use, follow these steps to flash)
  - Check wich COM port
  - Windows + R
  - `devmgmt.msc`
  - Enter
  - Check on the "COM & LPT Ports" section, the port should be listed there
  - `idf.py -p PORT flash`

### Device is flashed!
- You can now power off the board and unplug
- Next steps should be setting up the radio board below

## MacOS & Linux
comming soon

# LaunchPad CC1312R1
steps comming soon

# Connecting the boards
steps comming soon
