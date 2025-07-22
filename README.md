# PIC-Based Car Battery Voltage Monitoring System

## Project Description

This project is a **PIC16F877A-based Car Battery Voltage Monitoring System** designed to measure and display the real-time voltage of a car battery. The aim is to help users monitor their car battery's health and prevent unexpected failures.

The system uses a **voltage divider circuit** to scale down the 12V battery voltage to a safe level for the microcontroller's ADC (Analog-to-Digital Converter). The PIC microcontroller reads this analog voltage, converts it into a digital value, and displays the result on a **16x2 LCD** screen.

---

## System Workflow

1. **Power-On**: Initializes the microcontroller's peripherals (ADC, Timer, LCD).
2. **Input Reading**: Continuously reads the analog voltage through the ADC.
3. **Processing**: Converts the digital value to the actual battery voltage.
4. **Output**: Displays the voltage on the LCD; a buzzer or LED may alert users if the voltage is too low.

---

## Main Components

- **PIC16F877A Microcontroller**
- **Voltage Divider Circuit (Resistors)**
- **16x2 LCD Display**
- **Buzzer or LED** (for warning alerts)
- **12V Car Battery**
- **Power Supply Module (e.g., 7805 Voltage Regulator)**

---

## Interfaces Used

- **GPIO (General Purpose I/O)**:
  - To control the LCD, LED, and buzzer.
  - Can be extended for button interfaces.

- **ADC (Analog-to-Digital Converter)**:
  - Reads analog voltage input from the battery and converts it to digital.

- **Timer0**:
  - Generates delays and triggers periodic updates (like refreshing the display).

---

## Code Highlights

- Runs on the **PIC16F877A** microcontroller.
- Uses **RA0/AN0** analog pin to read the voltage.
- LCD works in **4-bit mode**.
- Screen updates only when the voltage value changes (to avoid flickering).
- Uses software delays instead of hardware timers.

---

## Expected LCD Output

  Voltage (V)     --    LCD Status     
  > 14.8          --    Status: HIGH   
  14.4 – 14.8     --    Status: CHARGING 
  13.8 – 14.3     --    Status: GOOD   
  12.6 – 13.7     --    Status: OK     
  11.5 – 12.5     --    Status: LOW    
  < 11.5          --    Status: CRITICAL 



## Repository

You can find the full source code here:  
[https://github.com/berilmutlu/car-battery-voltage-monitoring-sys]

---

## Conclusion

This project demonstrates the use of **embedded systems** and **microcontroller interfacing** in real-life applications. It's a practical tool for monitoring a car's battery voltage and provides an excellent introduction to ADC, timers, and LCD interfacing in embedded electronics.
