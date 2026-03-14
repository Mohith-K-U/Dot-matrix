# Arduino MAX7219 8×8 LED Matrix Scrolling Text

This project demonstrates how to display **scrolling text and simple animations** on a **MAX7219 8×8 LED Dot Matrix Display Module** using an **Arduino UNO**.  
The program scrolls a custom text message across the LED matrix and then plays a short arrow animation.

---

## Features

- Scrolls custom text across the LED matrix
- Supports ASCII characters using bitmap fonts
- Displays frame-based LED animations
- Adjustable brightness and scroll speed
- Uses SPI communication for efficient display control
- Simple and beginner-friendly Arduino project

---

## Hardware Required

- Arduino UNO (or compatible Arduino board)
- MAX7219 8×8 LED Dot Matrix Display Module
- Jumper wires
- USB cable for programming and power

---

## Wiring Diagram

Connect the MAX7219 module to the Arduino UNO as shown below.

| MAX7219 Pin | Arduino UNO Pin |
|-------------|-----------------|
| VCC | 5V |
| GND | GND |
| DIN | D11 |
| CS  | D10 |
| CLK | D13 |

### Pin Description

- **VCC** – Power supply for the display (5V)
- **GND** – Ground connection
- **DIN** – Data input (SPI MOSI)
- **CS** – Chip select pin
- **CLK** – Clock pin for SPI communication

---

## Library Required

This project uses the **MD_MAX72XX** library.

### Install using Arduino IDE

1. Open Arduino IDE
2. Go to **Sketch → Include Library → Manage Libraries**
3. Search for **MD_MAX72XX**
4. Click **Install**

---

## How the Program Works

1. The Arduino communicates with the MAX7219 LED driver using **SPI protocol**.
2. The scrolling text is converted into **bitmap columns using an ASCII font table**.
3. These columns are shifted across the display to create the **scrolling text effect**.
4. After the text finishes scrolling, a **bitmap arrow animation** is played.
5. The loop repeats continuously.

---

## Customization

### Change the Scrolling Text

Modify the following line in the code:

```cpp
const char *scrollingText = " TechBots ";
```

Example:

```cpp
const char *scrollingText = " Hello World ";
```

---

### Adjust Scroll Speed

```cpp
uint16_t scrollDelay = 100;
```

- Lower value → Faster scrolling  
- Higher value → Slower scrolling

---

### Adjust Display Brightness

```cpp
int brightnessLevel = 8;
```

Brightness range:

```
0  = Minimum brightness
15 = Maximum brightness
```

---

## Output

When the program runs, the LED matrix will:

1. Scroll the text **"TechBots"** across the display
2. Play a short **arrow animation**
3. Repeat the sequence continuously

---

## Project Structure



## Applications

- LED message displays
- Arduino learning projects
- IoT notification displays
- Name badges
- Embedded display systems

---

## Author

Mohith K U

---

## License

This project is open-source and can be used for educational and personal projects.
