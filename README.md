# Autonomous Pesticide Sprayer Robot

Code for the **Autonomous Pesticide Sprayer Robot**.

## Video Showcase

https://github.com/user-attachments/assets/e7281a75-e334-48a4-890e-7f8c3c24ce05

## Description
This repository contains the code I developed for our robotics project.  
The code is written in Python and runs on a Raspberry Pi.  

⚠️ Note: I can showcase the code, but I cannot provide the hardware schematics.

## Usage
Run the main script on the Raspberry Pi:

```bash
python3 pesticidespraybot.py
````

## Features

* **Dual 3-Level Spraying (Height-based)**
  The robot sprays at different heights (low, medium, high) from both sides.

* **Autonomous Navigation via Markers**
  The robot navigates using colored markers:

  * 🔴 Red squares → move left
  * 🔵 Blue squares → move right

* **SMS Alert and Auto-Terminate**
  If pesticide levels are low, the robot sends an SMS via Twilio/WhatsApp and terminates operations safely.

## Project Structure

* `myobjects90percent.py` – Contains classes and imports for all entities in the robot. Every real-world component has a corresponding class (object-oriented approach).
* `pesticidespraybot.py` – Main script for autonomous spraying. Imports `myobjects90percent.py` and runs the system.
* **Unit Tests for Components**

  1. `getHSV.py`
     Get HSV values for detecting the color of the corn plant.
  2. `takepicturecam.py`
     Capture images with the camera.
  3. `testLCD.py`
     Test the LCD display.
  4. `testUS.py`
     Test ultrasonic sensors.
  5. `testcamwindow.py`
     Check connectivity of all 3 cameras.
  6. `testgreencam.py`
     Detect correct green color of the corn plant.
  7. `testmarkercam.py`
     Detect navigation markers (red/blue squares).
  8. `testmotor.py`
     Test robot movement.
