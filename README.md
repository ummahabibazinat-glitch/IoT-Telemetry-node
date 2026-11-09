# 4-Bit Binary Click Counter Using Arduino Uno

## 📌 Project Overview

This project implements a 4-bit binary click counter using an Arduino Uno, one push button, and four LEDs.

Each time the push button is pressed, the counter increments by 1 and displays the corresponding 4-bit binary number (0000 to 1111) through the LEDs. After reaching 15, the counter resets to 0. This project demonstrates low-level AVR register manipulation rather than standard high-level Arduino functions.

---

## 🎯 Objectives

- Build a 4-bit binary counter (0–15).
- Display binary values using four LEDs.
- Read button input using the `PINB` register.
- Configure pin directions using the `DDRB` register.
- Control all four LEDs with a single `PORTB` register write.
- Use the internal pull-up resistor for the push button.

---

## 🛠️ Components Required

- Arduino Uno
- 1 × Push Button
- 4 × LEDs
- 4 × 220Ω Resistors
- Jumper Wires
- Breadboard

---

## 🔌 Pin Configuration

| Component | Arduino Pin | Register Bit |
| :--- | :--- | :--- |
| **LED 1** | D8 | PB0 |
| **LED 2** | D9 | PB1 |
| **LED 3** | D10 | PB2 |
| **LED 4** | D11 | PB3 |
| **Push Button** | D12 | PB4 |

---

## ⚙️ Working Principle

1. The four LED pins are configured as OUTPUT using `DDRB`.
2. Pin 12 (`PB4`) is configured as INPUT with the internal pull-up resistor enabled.
3. The button state is read directly using the `PINB` register.
4. Each valid button press increments the counter.
5. The counter value is displayed in binary using a single `PORTB` register write.
6. A 50 ms delay is used for simple button debouncing.
7. The counter automatically resets to 0 after reaching 15.

---

## 📊 Expected Output

| Decimal | Binary |
| :---: | :---: |
| 0 | `0000` |
| 1 | `0001` |
| 2 | `0010` |
| 3 | `0011` |
| 4 | `0100` |
| 5 | `0101` |
| ... | ... |
| 15 | `1111` |

---

## 💻 Code

The Arduino source code can be found in the `sketch.ino` file.

---

## 🔗 Simulation Links

- **Wokwi Simulation:** https://wokwi.com/projects/480223311398248449


---

## 📚 Registers Used

- **`DDRB`** – Data Direction Register B
- **`PORTB`** – Port B Data Register
- **`PINB`** – Port B Input Register

---

## 👩‍💻 Project Information

- **Platform:** Arduino Uno
- **Simulator:** Wokwi
- **Project Type:** Embedded Systems / Register Manipulation
- **Language:** C++
