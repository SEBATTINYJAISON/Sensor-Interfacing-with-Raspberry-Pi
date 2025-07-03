# Sensor-Interfacing-with-Raspberry-Pi

## 1. Introduction:
This lab introduces the basics of embedded sensor interfacing using the Raspberry Pi 5 and the Sense HAT. The main goal is to demonstrate how to read environmental data (temperature, humidity, and pressure) and display messages on the LED matrix. It provides hands-on experience in Python-based embedded programming, particularly useful in IoT and smart system applications.

##  2. Methodology
The Raspberry Pi was set up in headless mode to enable SSH access. The Sense HAT library was installed via the apt package manager. Two Python programs were developed: one for displaying text on the LED matrix and another for reading and displaying sensor data in the terminal.

## 2.1 Software and Hardware Used
- Programming Language: Python 3
- Libraries: sense-hat, time
- Hardware: Raspberry Pi 5, Sense HAT, WiFi-Router, Main PC

## 2.2 Algorithm Setup
Initial Configuration of Raspberry Pi 5 and Sense HAT
1. Use the Raspberry Pi Imager to download and flash the Raspberry Pi OS onto the
SD card.
2. In the Imager settings, configure the hostname, enable SSH, and set the username
and Wi-Fi credentials.
3. Insert the prepared SD card into the Raspberry Pi and power up the device.
4. Establish an SSH connection from a terminal (for example : ssh pi@192.168.0.10).
5. Update the system packages and install the Sense HAT library by executing:<br>
```sudo apt update```  
```sudo apt install sense-hat```

Part 1: Displaying Messages on the LED Matrix
1. Import the required Python modules ```(sense_hat and time)```
2. Instantiate a ```SenseHat``` object to interface with the hardware.
3. Use the ```show_message()``` method to scroll a text string across the LED matrix.
4. Adjust parameters such as ```text_colour``` and ```scroll_speed``` to customize the message appearance.

Part 2: Reading Environmental Sensor Data
1. Import the necessary modules ```(sense_hat and time)```.
2. Create a ```SenseHat object``` for sensor access.
3. Implement an infinite loop (while True) to continuously read data.
4. Retrieve environmental parameters using:
- ```get_temperature()``` for ambient temperature
- ```get_humidity()``` for relative humidity
- ```get_pressure()``` for barometric pressure
5. Format the sensor values into readable strings.
6. Output the data to the terminal with the ```print()``` function.
7. Introduce a delay between readings using ```time.sleep(2)``` to control the update
frequency.

## Result
Real-time environmental data were captured and printed to the terminal at two-second
intervals. The LED matrix reliably displayed the specified message.
