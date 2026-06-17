# Smart Wheel Misalignment and Tire Pressure Detection System for Automobiles

## Overview
The Smart Wheel Alignment and Tire Pressure Detection System is a portable, low-cost, and wireless embedded solution developed to identify wheel misalignment and tire pressure abnormalities in automobiles. The system is designed to provide a simple alternative to conventional workshop-based diagnostic equipment by enabling stationary inspection of wheel conditions using sensor-based measurements and wireless communication.

The project combines wheel alignment monitoring and tire pressure assessment into a single platform. Alignment parameters such as camber, caster, and toe are estimated using an accelerometer and steering angle sensor, while tire pressure is monitored using a pressure sensing module. The measured data are processed and transmitted wirelessly to a receiver unit, where the results are analyzed and displayed in real time.

## Problem Statement
Wheel misalignment and improper tire pressure are among the major causes of:
- Uneven tire wear
- Reduced vehicle stability
- Poor steering control
- Increased fuel consumption
- Higher maintenance costs
- Reduced road safety

Existing wheel alignment systems are typically expensive, require specialized workshop equipment, and depend on trained technicians. Regular inspection is therefore often neglected, resulting in delayed fault detection.

This project addresses these challenges by developing a compact and affordable wireless monitoring system capable of providing early detection of alignment and pressure-related issues.

## Objectives
- Detect wheel alignment deviations using sensor measurements.
- Estimate camber, caster, and toe parameters.
- Monitor tire pressure continuously.
- Enable wireless communication between sensing units and receiver.
- Provide real-time fault indication through a display interface.
- Reduce dependency on conventional workshop-based alignment systems.

## System Architecture
The system consists of four major modules:

### 1. ADXL345 Alignment Sensor Node
Measures wheel inclination and provides data for:
- Camber angle estimation
- Caster angle estimation

### 2. AS5600 Steering Sensor Node
Measures steering rotation and is used for:
- Toe angle estimation
- Steering deviation analysis

### 3. MPX5700AP Pressure Sensor Node
Measures internal tire pressure and classifies it as:
- Low Pressure
- Normal Pressure
- High Pressure

### 4. ESP32 Receiver Unit
Receives data through ESP-NOW wireless communication and:
- Processes sensor readings
- Performs alignment calculations
- Applies threshold evaluation
- Displays results on OLED display

## Hardware Components
| Component | Purpose |
|---|---|
| ESP32 / ESP32-C3 | Wireless processing and communication |
| ADXL345 Accelerometer | Camber and caster estimation |
| AS5600 Magnetic Rotary Encoder | Steering angle measurement |
| MPX5700AP Pressure Sensor | Tire pressure monitoring |
| OLED Display | Real-time result display |
| Power Supply Module | System operation |

## Software and Technologies
- Arduino IDE
- Embedded C/C++
- ESP-NOW Protocol
- OLED Display Library
- Sensor Interface Libraries

## Working Principle

### Camber Estimation
The ADXL345 accelerometer measures wheel inclination relative to gravity. The obtained tilt values are used to estimate the camber angle.

### Caster Estimation
The longitudinal orientation of the wheel assembly is evaluated using accelerometer readings to determine the caster angle.

### Toe Estimation
The AS5600 rotary encoder measures steering angle. Ackermann steering geometry is used to compare measured and expected wheel orientation, allowing detection of toe-in and toe-out conditions.

### Tire Pressure Monitoring
The MPX5700AP pressure sensor measures tire pressure and converts the sensor output into pressure values. The measured pressure is compared with predefined thresholds to determine tire condition.

### Wireless Data Transmission
Sensor nodes transmit measured values to the receiver using ESP-NOW. The receiver performs calculations and displays wheel alignment and tire pressure status on the OLED screen.

## Features
✔ Wireless operation using ESP-NOW
✔ Portable and compact design
✔ Real-time monitoring
✔ Low-cost implementation
✔ No internet connectivity required
✔ Early fault detection
✔ User-friendly OLED display
✔ Suitable for stationary vehicle inspection

## Results
The developed system successfully identifies:
- Normal wheel alignment conditions
- Wheel misalignment conditions
- Steering-related deviations
- Low tire pressure
- High tire pressure
- Normal tire pressure

Experimental testing under multiple operating conditions demonstrated reliable detection of alignment and pressure abnormalities.

## Applications
- Automobile maintenance workshops
- Vehicle inspection centers
- Educational and research laboratories
- Automotive diagnostic systems
- Preventive vehicle maintenance

## Future Enhancements
- Dynamic monitoring for moving vehicles
- Mobile application integration
- Data logging and maintenance history
- Vehicle-specific calibration profiles
- Advanced fault prediction techniques
- Enhanced diagnostic analytics

## Conclusion
The Smart Wheel Alignment and Tire Pressure Detection System provides an effective and economical approach for monitoring vehicle wheel condition. By integrating alignment estimation and tire pressure measurement within a wireless embedded framework, the system enables early detection of faults without requiring expensive diagnostic infrastructure. Its portability, simplicity, and real-time monitoring capability make it a practical solution for automotive maintenance and safety applications.

## Authors
**Tejashwini N M** | **Arshiya Fathima** | **Harshithabai R** | **Nisha S K**

Electronics and Communication Engineering

**Project Domain:** Embedded Systems | IoT | Automotive Diagnostics | Wireless Sensor Networks
