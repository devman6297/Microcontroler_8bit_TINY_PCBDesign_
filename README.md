# Microcontroler_8bit_TINY_PCBDesign_
The provided the design of a microcontroller-based system named "TINY," incorporating essential modules for power management, RGB LED control, an accelerometer interface, and user input.


Microcontroller Overview
Microcontroller: PIC16LF1829-I/SS


Features:
     Power Supply: Operates at 3.3V (regulated by the TPS79333 voltage regulator).


     
I/O Ports:
          RA0 to RA5: Configured for digital I/O and debugging (ICSPDAT/ICSPCLK pins).
          RC0 to RC7: Connected to RGB LED control and other outputs.
          RB7 and RB6: Interface with the button and I2C communication lines (SDA, SCL).



Special Functions:
            Supports In-Circuit Serial Programming (ICSP).
            I2C communication interface.
            General-purpose Input/Output pins for LED driving and button interface.



Applications:
     LED color control.
     Sensor data acquisition (accelerometer).
     User input processing.
     Power Management



Battery and USB Power:
     The system can be powered either by a battery or USB.
     The battery voltage (+VBAT) is managed by a BAT54CLT1G Schottky diode to avoid reverse current flow.
     USB 5V input passes through LED1, providing a visual power-on indicator.



Voltage Regulator: TPS79333
          Converts input voltage (+VIN) to a stable 3.3V for the microcontroller and peripherals.
          Uses decoupling capacitors (C1 and C2) for noise reduction.


RGB LED Control
         LED2: MHS110FRGBCT RGB LED



Driving Circuit:
        Controlled via three transistors (Q1, Q2, Q3 - 2N7002).
        Resistors (R1, R2, R3 - 300Ω) limit the current for each color channel (Red, Green, Blue).
        Color brightness and mixing controlled by PWM signals from RC4, RC5, and RC6.
        Accelerometer Interface



Accelerometer: KXTJ3-1057
            Communication: I2C interface (SDA, SCL) connected to the microcontroller.



Power Supply: Operates at 3.3V.
          Interrupt Pin (INT): Provides event notifications to the microcontroller.
          Decoupling Capacitors: C4 and C8 ensure stable operation and noise filtering.
          User Input



Button (SW1):
          A push-button connected to RB7 with a pull-up resistor (R12 - 10kΩ).
          Provides user interaction, e.g., for triggering events or modes.
          Debugging Interface



ICSP Header (H2):
      Provides In-Circuit Serial Programming for firmware updates and debugging.
      Pins include VPP (Programming Voltage), ICSPDAT, ICSPCLK, and GND.
      Connector Headers
 
 
 
 I2C and Button Header (H3):
Exposes I2C lines and button signal for external devices or debugging.



LED Header (H4):
        Provides access to RGB LED control signals and power lines (+VIN, GND).

        








  SChematic--->


![image alt](https://github.com/devman6297/Microcontroler_8bit_TINY_PCBDesign_/blob/d914bda468b8a599d19e3b819bfd3926f88c82dc/Schematic_Node-MCU_2025-01-07.png)









 3D View--->



![image alt](https://github.com/devman6297/Microcontroler_8bit_TINY_PCBDesign_/blob/80d4cca219521ba677ac25446ab46990150bf7ff/Screenshot%202025-01-07%20185422.png)
