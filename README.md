# flight-controller-progress-documentaion

# 1. Introduction
The goal of this report is to document the progress made in the development of flight controllers for UAV (Unmanned Aerial Vehicle) vehicles using three different platforms: STM32F11CEU6, ESP32, and Teensy 4.0. Each project aimed to address specific requirements and take advantage of the unique features offered by each microcontroller, ultimately culminating in a comprehensive toolkit for building and operating UAV vehicles.

# 2.  Project 1: Flight Controller Using STM32F11CEU6 Development Board
link-https://github.com/saranshj29/flight-controller-development

## 2.1  Overview
In this project, the STM32F11CEU6 development board was selected for its robustness and capabilities in handling flight control tasks. The aim was to develop a flight controller that could process data from various sensors to stabilize the aircraft during flight.

## 2.2 Hardware Setup
Components Used:

STM32F11CEU6 Development Board
MPU6050 or LSM9DS1 (IMU)
BMP280 (Barometer)
GPS Module (Robotbanao NEO-6M)
Flysky FS-i6 Transmitter and Receiver
ESCs and Brushless Motors
Assembly: The setup included soldering pin headers, connecting the IMU, GPS, barometer, and configuring the radio system.

## 2.3 Software Configuration
INAV Firmware: Installed and configured INAV firmware to support the STM32F11CEU6 board.
Calibration: Calibrated the IMU, barometer, and compass to ensure accurate readings.


## 2.4 Progress and Outcomes
Successfully assembled hardware and integrated various components.
Installed INAV firmware and configured settings for stable flight.
Conducted initial flight tests, achieving satisfactory stability and control.


## 2.5 Challenges Encountered
Communication issues between the receiver and flight controller were resolved by verifying wiring and configurations.
Sensor interference required repositioning components to improve accuracy.


# 3. Project 2: Flight Controller Using ESP32
link-https://github.com/saranshj29/esp32-based-flight-controller
## 3.1 Overview
For this project, the ESP32 was chosen as the flight controller due to its cost-effectiveness, built-in Wi-Fi and BLE capabilities, and high processing speed. The goal was to develop a responsive flight controller that could communicate wirelessly.

## 3.2 Hardware Setup
Components Used:
ESP32 Development Board
MPU6050 (IMU)
ESCs and Brushless Motors
Flysky Transmitter and Receiver
Assembly: The IMU was connected via I2C, and the ESCs were wired to control the motors.

## 3.3 Software Configuration

Code Files:
Anglemode_flightcontroller_ver3: The main code for flight control, requiring initial calibration on a level surface.
Receiver_PWM_ESP32: Tested the receiver and transmitter signals.
Motors Calibration: Ensured the ESCs were calibrated to start simultaneously.

## 3.4 Progress and Outcomes
Completed hardware setup and code upload without major issues.
Successfully calibrated the gyro and ESCs.
Established reliable communication between the receiver and ESP32.

## 3.5 Challenges Encountered
Library compatibility issues were resolved by ensuring the correct versions were used.
Careful monitoring of calibration timing was necessary to avoid instability.

# Project 3: Flight Controller Using Teensy 4.0
 link-https://github.com/saranshj29/flight-controller-using-teensy-4.0-micro-controller


## 4.1 Overview
The Teensy 4.0 was utilized to create a versatile flight controller capable of supporting a wide range of UAV configurations. This project aimed to build on the lessons learned from the previous two projects, providing a more robust and modular platform.

## 4.2 Hardware Setup
Components Used:

Teensy 4.0 Microcontroller
MPU6050 IMU
ESCs and Brushless Motors
Various servos for control surfaces
Assembly: Included soldering connections, wiring the IMU, and connecting ESCs and servos based on the project specification

## 4.3 Software Configuration
Code Structure: The code was modular, facilitating easy updates and maintenance. Key sections included initialization, control loops, and data processing.
Libraries: Utilized libraries for I2C communication, PID control, and servo operation.

## 4.4 Progress and Outcomes
Achieved a successful integration of hardware and software components.
Completed calibration of the IMU and tuning of the PID controller.
Conducted comprehensive flight tests, demonstrating stable flight performance.

## 4.5 Challenges Encountered
Required iterative tuning of PID parameters to achieve optimal performance.
Performance testing revealed minor adjustments needed in control response, which were addressed in subsequent tests.

# 5. Combined Insights and Future Work
## 5.1 Comparative Analysis
STM32F11CEU6: Provided a solid foundation for learning about flight control systems but faced challenges with communication and sensor interference.
ESP32: Enabled wireless communication features but required careful attention to calibration and library management.
Teensy 4.0: Offered high processing capabilities and modularity, proving to be the most versatile option for complex flight dynamics.

## 5.2 Future Enhancements
Autonomous Flight Capabilities: Implementing advanced algorithms for autonomous navigation and path planning.
Enhanced Sensor Integration: Adding support for additional sensors (e.g., LiDAR, GPS) to improve performance and functionality.
Community Contributions: Encouraging collaboration and sharing of modifications within the user community to foster innovation.

## 6. Conclusion
The development of flight controllers using the STM32F11CEU6, ESP32, and Teensy 4.0 has provided valuable insights into the design and functionality of UAV systems. Each project contributed to building a comprehensive toolkit, allowing for flexibility and customization in the creation of aerial vehicles. The journey has been marked by iterative learning, problem-solving, and a commitment to innovation in the field of UAV technology.
