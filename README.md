# Fall Detection System

## Overview
The **Fall Detection System** is designed to detect sudden falls using an **ADXL335 3-axis accelerometer** and an **AVR microcontroller (Arduino Mega)**. If a free fall is detected, the system activates a **buzzer alarm** to alert caregivers or emergency responders.

## Components Required
- **Microcontroller**: Arduino Mega (or any AVR-based board with ADC support)
- **Accelerometer**: ADXL335
- **Buzzer**: Connected to Digital Pin 12 (PB4)
- **Power Supply**: 5V DC
- **Connecting Wires**

## Connection Details
| **Device**         | **Pin Name**    | **Connection** |
|--------------------|----------------|----------------|
| **ADXL335**       | VCC             | 3.3V           |
|                   | GND             | GND            |
|                   | X-Axis (X_OUT)  | A0 (ADC0)      |
|                   | Y-Axis (Y_OUT)  | A1 (ADC1)      |
|                   | Z-Axis (Z_OUT)  | A2 (ADC2)      |
| **Buzzer**        | Positive (VCC)  | PB4 (Digital Pin 12) |
|                   | Negative (GND)  | GND            |


## Working Principle
1. **ADC Initialization**  
   - The system initializes the ADC to read analog values from the **X, Y, and Z axes** of the ADXL335 sensor.
2. **Fall Detection Algorithm**  
   - The system continuously monitors **accelerometer data**.
   - If all three axis values fall **below the defined threshold**, the system detects a **free fall** and activates              the buzzer.
3. **Buzzer Activation**  
   - When a fall is detected, the **buzzer turns ON** to alert nearby people.
   - If no fall is detected, the buzzer remains **OFF**.

