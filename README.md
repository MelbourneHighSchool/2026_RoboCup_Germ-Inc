# Germ Inc
## General Information
| | |
| ----------- | ---- |
| Year | 2026 |
| Year Level | 11 |
| Team Name | Germ Inc |

Team Members (in first name alphabetical order):
- Allen
- Jerold
- Kieran
- Sebastian

# REQUIREMENTS
## Software
- Visual Studio Code (text editor of choice)
- Coding Language: Python 3.11 (Raspberry Pi) & C (PCB)
- STM32 Cube IDE (Write and flash custom PCB firmware)
- Github (source control)
- RealVNC Viewer (Used to remotely access and view Raspberry Pi GUI)

## Hardware
Per robot:
- 5x Robomaster M2006 P36 BLDC motors (ran on custom Steelbar Robotics Brushless Motor Drivers)
- 4x GTF Omniwheel (50mm diameter)
- 4S 850mAh Li-Po battery
- Raspberry Pi 5 (active cooler installed)
- Raspberry Pi HQ Camera
- Adafruit BNO085 IMU
- Custom PCB
  - 12 IR sensors (TSSP4038), 32 light sensors for line detection
- On-off switch (GPIO 25)

# SETUP & INSTALLATION
On a Raspberry Pi 5 with Raspberry Pi OS installed:
1. Install circuitpython: https://learn.adafruit.com/circuitpython-on-raspberrypi-linux/installing-circuitpython-on-raspberry-pi 
2.	Install the motor driver library, and other dependencies: pip install git+https://github.com/Aw3someAndrew/SteelBar_CircuitPython_powerful_bldc_driver.git
3.	Clone the repository into a directory of choice

# DEPLOYING & USAGE
During competitions, both pi's are setup to automatically run the code on startup. To manually run the code, follow the below:
1. Activate virtual environment
2. Change directory to the folder with the github repository
3. run either 1attack.py (striker robot), or 1defense.py (goalie robot)
4. Flick the switch (wired from GPIO 25 to ground on the Raspberry Pi) to run the code, or otherwise in standby

Note: It is recommended to startup in standby as to calibrate the robot's bottom LED, compass, and goal colour
