# ScArY - Scientific RPN calculator on ATTINY
Version 1.0 ... (c) 2018 by deetee/zooxo

## What is ScArY?
ScArY is a scientific RPN calculator on an ATTINY85 and a  QYF-TM1638-board (8 digit LED display with 16 buttons controlled with 3 pins). ScArY is capable of familiar functions of RPN calculators (i.e. stack operations) and many mathematical operations (i.e. trigonometic functions) as well as some special functions like calculating annuities or gaussian distributions.
Due to the memory restrictions of the ATTINY85 (8 kilobytes) some compromises were  made to offer so many functions. So the numbers are shown in SCI notation only (see below).

Another compromise is the lack of checking for errors - usually there is no readable display  if an error occurs.

Due to the 8-bit-processor ARC calculates only 5 to 6 digits exactly. This should be enough for most calculations (except you are a bookkeeper who wants to add billion-amounts with cent-accuracy).

## On which hardware does ScArY run?
Compile the attached file "scary_1_0-ino" with your arduino suite and upload the code to your ATTINY85 with some programmer hardware or an Arduino as ISP (like I did). Connect the ATTINY85 pins (5/6/7 resp. data/clock/strobe) with the corresponding pins on the QYF-TM1638-board, power them up (5V Vcc and GND) and you are running.

## Which Commands does ScArY support (COMMANDS and KEYS)?    
### Basic keys:
* 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, ., EE, CHS, ENTER, C/CE, f
### f-keys:
* +, -, *, / (basic operations)
* STO, RCL, SHOW, SWAP, LASTx, ROT+, ROT-, SQRT, PI
* MENU (browse menu)
* BRIGHTNESS (set brightness of display)
* zZZ (toggle screensaver)
### MENU-functions:
* POWER, 1/X, EXP, LN
* SIN, COS, TAN, ASIN, ACOS, ATAN
* SINH, COSH, TANH, ASINH, ACOSH, ATANH
* ANNU (present value for a given interest rate and duration)
* GAUSS PDF/CDF (Propability Density Function and Cumulated Distribution Function)
* FACT (factorial)
* DEG/RAD

## How to Enter a Number?
  1. Enter mantissa (with '.' if applicable)
  2. If applicable: Enter EE to enter exponent (limited to 29)
  3. If applicable: Toggle sign of exponent with EE
  4. If applicable: Toggle sign of number with CHS

## A short Video of a Miniaturized ScArY
https://www.youtube.com/watch?v=q-9j547xWfg

## Some Pictures of a Miniaturized ScArY
![pics](https://user-images.githubusercontent.com/16148023/36966765-be3b98d6-2055-11e8-950e-49108db44dd6.png)

## The Circuit Diagram
![circuit](https://user-images.githubusercontent.com/16148023/36966763-bdd99212-2055-11e8-9185-e1ec609a81a4.png)

## The Keyboard Layout
![keyboard](https://user-images.githubusercontent.com/16148023/36966764-be132be4-2055-11e8-9582-b050a5415ba3.png)
