# **PLC-Based Spindle Control System: Auto and Manual Modes with Safety Interlocks**

## **Project Overview**

This project features a PLC-based control system for managing a spindle, coolant, and lamp using Simatic Manager. The system operates in two modes- auto and manual , providing flexibility in machine control. It also includes an emergency button for safety.

https://github.com/user-attachments/assets/b2da2250-ebee-4219-b5e0-d330d094e275


![Spindle   Coolant - converted_page-0001](https://github.com/user-attachments/assets/3072509c-01d8-413f-a33b-5d44c9dd341c) 

## **Features**

- **Dual Mode Operation**: Switch between Auto and Manual modes. Modes are mutually exclusive; enabling one disables the other.
- **Manual Mode**: 
  - **Coolant**: Only turns on when the spindle is running.
  - **Lamp**: Only turns on when the spindle is running.
- **Auto Mode**:
  - **Spindle Activation**: Turns on the lamp immediately.
  - **Coolant Activation**: Delays coolant activation by 5 seconds after the spindle turns on.
- **Emergency Button**: Immediately turns off the spindle, coolant, and lamp when activated.

## **Control Logic**

1. **Mode Selection**:
   - **Manual Mode**: 
     - The coolant and lamp depend on spindle operation.
     - Cannot switch to Auto Mode while Manual Mode is active.
   - **Auto Mode**: 
     - The lamp turns on with spindle activation.
     - The coolant activates 5 seconds after spindle activation.
     - Cannot switch to Manual Mode while Auto Mode is active.

2. **Emergency Stop**:
   - Activates a system-wide shutdown of the spindle, coolant, and lamp.

## **PLC Programming Tools**

- **PLC Model**: Siemens S7-1200
- **Programming Software**: Simatic Manager
- **Languages**: Ladder Logic (LAD), Function Block Diagram (FBD)

## **Installation & Usage**

1. **Load** the PLC program into Simatic Manager.
2. **Connect** I/O devices (spindle, coolant pump, lamps, and emergency button).
3. **Select** the mode (Auto or Manual) using the mode selector.
4. **Activate** the spindle to start the process according to the selected mode.
5. **Use** the emergency button to shut down the system in case of emergency.

## **Future Enhancements**

- Integration of additional safety features or alarms.
- Advanced control options for more precise coolant management.

---
