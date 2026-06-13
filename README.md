# 8086 Assembly Bitwise Rotate Right (ROR)

A basic 8086 Assembly Language program written in MASM/TASM syntax that demonstrates bitwise circular right-shifting using the **`ROR` (Rotate Right)** instruction and DOS interrupts (`INT 21H`).

## 🚀 Project Overview

This program captures a single-digit number input from the user, converts it from ASCII to its actual numeric decimal value, applies a bitwise right-rotation by 1 position, and converts the result back to ASCII format to display it on the console screen.

## 🛠️ How It Works & Bitwise Logic

Unlike a logical right shift (`SHR`), where the bits falling off the right edge are lost and replaced by zeros on the left, **Rotation Right (`ROR`)** wraps the bits around in a circular fashion.

### The Rotation Logic ($ROR$):
When you execute `ROR BL, 1`, every bit inside the 8-bit `BL` register shifts right by one slot. The **Least Significant Bit (LSB)** or the rightmost bit that leaves the register is moved into the **Most Significant Bit (MSB)** or leftmost slot, as well as copied into the Carry Flag (CF).

#### Bitwise Example (Inputting the number `2`):
1. **ASCII Conversion:** Input `'2'` (ASCII 50) $\rightarrow 50 - 48 =$ numeric value **`2`**.
2. **Binary Representation:** Decimal `2` in an 8-bit register is `0000 0010`.
3. **Execution of `ROR BL, 1`:**
   * Before: `0 0 0 0  0 0 1 0` (The rightmost bit is `0`)
   * After:  `0 0 0 0  0 0 0 1` (The rightmost `0` wrapped around to the leftmost spot, and everything shifted right).
4. **Result:** Binary `0000 0001` is decimal **`1`**.
