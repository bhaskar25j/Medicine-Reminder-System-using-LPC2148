# Medicine-Reminder-System-using-LPC2148
This embedded system project is a real-time Medicine Reminder System designed using an LPC2148 ARM7 microcontroller. It alerts users to take their medication at scheduled times using a buzzer, LCD, and 4x4 matrix keypad, making it especially useful for the elderly or chronically ill patients.

🎯 Project Objectives

Display real-time clock (RTC) data (date and time) on a 16x2 LCD.
Allow users to set and store multiple medicine schedules via a 4x4 keypad.
Trigger an audible and visual alert when medicine time is reached.
Allow user acknowledgment through a dedicated button to stop the alert.

🔧 Hardware Requirements

Component	Description

LPC2148 MCU	ARM7-based microcontroller
16x2 LCD	For displaying RTC and messages
4x4 Keypad	For inputting medicine timings
RTC (On-chip)	Real-time clock functionality
Buzzer	Audio alert
Switches (SW1, SW2)	For setting schedules and acknowledgment
USB-UART/DB-9	For programming and debugging

💻 Software Requirements

Embedded C (Keil IDE or equivalent)
Flash Magic (for flashing the LPC2148)
Optional: Proteus or simulation tools for testing logic

⚙️ Working Principle

Medicine Time Setup

User presses SW1 to enter medicine times via the keypad.
Schedule is stored in microcontroller memory.
LCD displays current RTC info and scheduled times.
Monitoring & Alert

The system checks RTC time continuously.
If current time matches any stored medicine time:
LCD displays “Take Medicine Now”
Buzzer beeps intermittently to notify user
User Acknowledgment

User presses SW2 to stop the buzzer and confirm intake.
System returns to normal monitoring.

📑 Software Flow Summary

System Initialization (RTC, LCD, Keypad, Buzzer)
Display current date/time
Wait for SW1 to input medicine time
Compare RTC time with saved schedule
If match found, alert user
Wait for SW2 acknowledgment
Return to monitoring loop

📈 Features

Real-time clock based scheduling
Multi-time reminder setup
Simple hardware interface
Low power and cost-effective
Ideal for home and healthcare use

🔮 Future Enhancements

Battery backup for RTC
Voice alert system
Integration with mobile app or SMS module
Long-term history log in EEPROM
