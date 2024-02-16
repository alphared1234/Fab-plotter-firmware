# Fab-plotter-firmware
This repository contains the SAMD21E17A for a Mini CNC Plotter, designed to draw on surfaces using two stepper motors and a servo-controlled pen. The project uses the AccelStepper and MultiStepper libraries to control the stepper motors and achieve smooth motion.



# HARDWARE REQUIREMENT
 1.SAMD21E17A MCU board
 
 2.Two stepper motors with drivers

 3.Servo motor

 4.Pen

 5.Power supply

 6.CNC frames 

 # Wiring Instructions

 1.Connect stepper motor 1 to pins 2, 4, 3, and 5 on the Arduino.

 2.Connect stepper motor 2 to pins 6, 8, 7, and 9 on the Arduino.

 3.Connect the servo motor to pin 15 on the Arduino.

 4.Ensure the power supply is appropriately connected to power the motors.

 # Configuration

 Adjust the following parameters in the code to match your setup:

 const int penZUp = 40;
const int penZDown = 80;

const int penServoPin = 15;

const int stepsPerRevolution = 2048;

float StepsPerMillimeterX = 18.6;
float StepsPerMillimeterY = 18.6;

float Xmin = 0;
float Xmax = 150;
float Ymin = 0;
float Ymax = 150;
float Zmin = 0;
float Zmax = 1;


# Usage
1.Upload the code to your SAMD21E17A board.

2.Connect the Mini CNC Plotter to your computer via USB.

3.Open the serial monitor in the Arduino IDE or any serial communication software.

4.Send G-code commands to control the plotter. Example commands include moving to specific coordinates, lifting or lowering the pen, and setting the pen's position.


# G-code commands 

1.G00 or G01: Move to a specific position.

2.M03 S123: Lower the pen.

3.M03 S000: Lift the pen.

# Acknowledgments

The code uses the AccelStepper and MultiStepper libraries for smooth stepper motor control.

