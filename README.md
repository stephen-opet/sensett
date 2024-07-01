███████╗███████╗███╗   ██╗███████╗███████╗████████╗████████╗
██╔════╝██╔════╝████╗  ██║██╔════╝██╔════╝╚══██╔══╝╚══██╔══╝
███████╗█████╗  ██╔██╗ ██║███████╗█████╗     ██║      ██║   
╚════██║██╔══╝  ██║╚██╗██║╚════██║██╔══╝     ██║      ██║   
███████║███████╗██║ ╚████║███████║███████╗   ██║      ██║   
 ╚══════╝╚══════╝╚═╝  ╚═══╝╚══════╝╚══════╝   ╚═╝      ╚═╝  

<p align="center">
  <a>
    <h1 align="center">Sensett</h1>
    <h2 align="center"><a href="https://ddamakertech.com">By DDA Maker Tech</a>
  </a>
</p>
<p align="center">
  A CLI-driven module for reading custom sensors & publishing data to MQTT as an automatic background service, designed for use with 3D printers running Klipper/Moonraker
</p>

## Purpose

I dont want to fuss about adding custom sensors to my Pi and importing data to Klipper/Moonraker/Mainsail. Sensett automates the entire process with a command-line interface for ease-of-use by posting sensor data to MQTT and providing users with the correct configuration to add into Moonraker.conf

## Supported Sensors

Sensett currently supports the following sensors:
- SGP40
- SHT31

If you want to add support for a new sensor, feel free to either fork this repo & modify it yourself, or otherwise leave some notes as an issue


## Installation

SSH into your printer's Pi and run the following commands:
  ```
  sudo apt-get update && sudo apt-get install git -y
  cd ~ && git clone https://github.com/stephen-opet/sensett.git
  ```
... that's it!

## Config and Execution

To manage your Sensett config, execute the bash script (you may need to configure file permissions to make the file executable):
  ```
  sudo chmod 777 sensett/sensett.sh
  ./sensett/sensett.sh
  ```
This will launch the command-line interface, from which you can configure your hardware sensors, link them to an MQTT sensor, generate moonraker.conf settings, and for the Nevermore guys - link a fan to a sensor!
