# Project 01.01 - Flashing LED Project

# Materials you'll need
- Raspberry Pi (any model with GPIO pins)
- LED (any color)
- 220-330Ω resistor
- Jumper wires
- Breadboard (optional)
- Power supply for the Raspberry Pi

# Step 1: Gather your materials 
Make sure you have all the required components and tools ready


# Step 2: Connect the LED and Resistor 
- 1. Connect the longer leg of the LED (anode) to one leg of the resistor.
- 2. Connect the other leg of the resistor to one of the GPIO pins on the Raspberry Pi (e.g., GPIO 17).
- 3. Connect the shorter leg of the LED (cathode) directly to a Ground (GND) pin on the Raspberry Pi.
 
# Step 3: Set up the Rasberry Pi
- 1. Power up your Raspberry Pi using a suitable power supply.
- 2. Make sure your Raspberry Pi is running Raspbian or a similar Linux-based OS.
 
# Step 4: Open the terminal
- Open the Terminal on your Raspberry Pi.

# Step 5: Access the GPIO Pins
- In the Terminal, enter the command to access the GPIO pins:
- "gpio -g mode 17 out"

# Step 6: Create a python script
- You can use any text editor to create a Python script. For example, to use the built-in Nano text editor, you can enter:
- "nano_blink_led.py

# Step 7: Write the python script 
- In the Nano editor, write the following Python script to make the LED blink:
-  ```python
 import RPi.GPIO as GPIO
 import time

 GPIO.setmode(GPIO.BCM)
 GPIO.setup(17, GPIO.OUT)

 try:
     while True:
         GPIO.output(17, GPIO.HIGH)
         time.sleep(1)
         GPIO.output(17, GPIO.LOW)
         time.sleep(1)

 except KeyboardInterrupt:
     GPIO.cleanup()
 



# Step 8: Save and exit the text editor
- Save the Python script and exit the Nano text editor (for Nano, press `Ctrl + X`, then `Y` to confirm, and `Enter`).

# Step 9: Run the Python script
-In the terminal, run the Python script you created:
python_blink_led.py


# Your LED should start flashing with a 1-second interval. To stop the script, press `Ctrl + C`.





