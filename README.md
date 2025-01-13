# Visual Cue Notification System

## Overview
The **Visual Cue Notification System** is an assistive technology designed for hearing-impaired individuals living in university dormitories. This system enhances safety and accessibility by providing real-time visual alerts when motion is detected outside a door. Using two STM32 Nucleo boards and Bluetooth communication, the system wirelessly transmits motion data from a PIR sensor to an LED visual alert.

### Problem Statement
Hearing-impaired students in dormitories face challenges due to the lack of adequate accessibility infrastructure, such as visual alert systems for door knocks or fire alarms. Many existing solutions are either expensive or do not integrate well with dormitory environments. Our project aims to bridge this gap by offering an affordable, portable, and reliable notification system.

### Solution
The project implements a two-unit system:
1. **Sensor Unit**: Detects motion using a PIR sensor and transmits the data wirelessly via a Bluetooth module.
2. **Alert Unit**: Receives the motion data and triggers an LED visual alert to notify the user of activity near their door.

### Key Features
- **Wireless Communication**: The system uses HC-05 Bluetooth modules to enable reliable communication between the sensor and alert units.
- **Real-Time Alerts**: Motion detection and alert triggering occur with minimal latency, ensuring prompt notifications.
- **Low Power Consumption**: The system is designed to consume less than 100 mW of power, making it suitable for long-term usage.
- **User-Friendly Design**: Custom 3D-printed cases house the units, ensuring portability and protection of internal components.
- **Accessible for Dormitories**: The system operates without requiring modifications to existing dorm infrastructure, making it easy to deploy.

## Components
- **STM32 Nucleo Boards (x2)**: Microcontrollers that handle sensor input and alert output.
- **PIR Motion Sensor**: Detects infrared radiation to sense motion.
- **HC-05 Bluetooth Modules (x2)**: Facilitate wireless communication between the two STM32 boards.
- **LED and Resistor**: Provide the visual alert.
- **Breadboard and Jumper Wires**: Used for prototyping and connections.
- **3D-Printed Cases**: Protect the hardware and enhance portability.
- **AA Batteries**: Power the system.

## Functional Requirements
- **Motion Detection Range**: 1–3 meters with a 90-degree detection angle.
- **Visual Alert**: The LED should have a brightness between 100 and 150 lumens and respond within 500 milliseconds of motion detection.
- **Bluetooth Communication**: Reliable transmission with a range of up to 10 meters and minimal error rate.
- **Power Consumption**: The system should consume no more than 100 mW during operation.

## How It Works
1. The **Sensor Unit** continuously monitors for motion using the PIR sensor.
2. When motion is detected, the unit sends a signal via Bluetooth to the **Alert Unit**.
3. Upon receiving the signal, the **Alert Unit** activates the LED, providing a visual cue to the user.
4. The system resets and continues monitoring for further motion.

## Installation and Setup
1. Connect the PIR sensor to the first STM32 board and the LED to the second STM32 board as per the wiring instructions.
2. Power the units using AA batteries.
3. Place the **Sensor Unit** near the door and the **Alert Unit** inside the dorm room.
4. Ensure both units are within Bluetooth range for effective communication.

## Testing and Validation
The system has undergone extensive testing to ensure:
- Accurate motion detection within the specified range.
- Reliable Bluetooth communication with minimal latency.
- Consistent visual alert activation in real-world dormitory environments.
- Compliance with safety and power consumption standards.

## Future Enhancements
- **Integration with Smart Home Systems**: Adding support for smart home protocols (e.g., Zigbee, Wi-Fi).
- **Multiple Alert Types**: Incorporating vibration and sound alerts for broader accessibility.
- **Mobile App Notification**: Developing a companion app to send alerts to the user’s smartphone.

## Contributors
- **Samir Sarwar**
- **Ryan Nguyen**
