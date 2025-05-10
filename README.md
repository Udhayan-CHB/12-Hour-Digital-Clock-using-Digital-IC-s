# 12-Hour Digital Clock Using CD4026 ICs & Crystal Oscillator ⏱️

A fully hardware-based 12-hour digital clock project using CD4026 decade counter/7-segment driver ICs and a crystal oscillator for precise timekeeping. This build runs independently of microcontrollers or software, showcasing pure digital logic with real-time second, minute, and hour counting.

---

# Project Overview

This project implements a HH:MM:SS digital clock using six 7-segment displays, driven directly by CD4026 ICs. Timing is maintained through a crystal oscillator circuit, ensuring accurate 1 Hz pulses that increment the second counter. The design resets automatically at 12:59:59 and loops back to 01:00:00. A manual reset button allows for resetting the clock to 12:00:00.

---

# Components Used

| Component                           | Quantity |
|-------------------------------------|----------|
| CD4026 (Decade Counter + Driver)    | 6        |
| 7-Segment Display (Common Cathode)  | 6        |
| 32.768 kHz Crystal Oscillator       | 1        |
| CD4060 or similar frequency divider | 1        |
| Logic Gates (CD4011/CD4081 etc.)    | As needed|
| Capacitors, Resistors               | Varies   |
| Push Button (Reset)                 | 1        |
| Breadboard or PCB                   | 1        |
| 5V Power Supply                     | 1        |

---

# How It Works

1. Clock Signal Generation:
   - A 32.768 kHz crystal oscillator is used with a frequency divider (e.g., CD4060) to produce an accurate 1 Hz signal.
   
2. Counting Mechanism:
   - Each CD4026 counts from 0 to 9 and drives a 7-segment display directly.
   - The counters are cascaded for seconds, minutes, and hours using carry-out logic.
   - Custom logic ensures the hour resets after reaching 12.

3. Display Output:
   - 6-digit 7-segment display shows time in HH:MM:SS format.
   - No additional display driver is required, as CD4026 outputs directly control the displays.

4. Manual Reset:
   - A push-button wired to the reset pins on the CD4026s resets the clock to 12:00:00 when pressed.

---

# Features

- 12-hour format display (no AM/PM)
- Accurate timekeeping with a crystal oscillator
- Reset button to set time to 12:00:00
- Fully hardware-based—no microcontrollers
- Simple cascading logic for counter synchronization

---

# Learning Highlights

- Practical use of CD4026 for both counting and display driving
- Frequency division using crystal oscillators
- Hardware-only logic sequencing and design
- Manual reset logic in digital systems

---

# Future Improvements

- Add AM/PM indicator using flip-flop logic
- Include a time-setting mechanism (e.g., set hours/minutes)
- Replace the breadboard with a custom PCB for durability
- Add backup power (battery) for retention during power failure

---

# Contributions

Have a suggestion or improvement? Open a pull request or issue—community collaboration is welcome!

---

## ✍️ Author

Made with logic, LEDs, and a bit of patience by [Your Name].


