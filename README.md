🤖 Robotic Arm Project with AnkerMake M5
📄 Project Description
This project focuses on designing, 3D printing, and assembling a robotic arm using the AnkerMake M5 3D printer. The goal is to create a functional arm that can be used for basic tasks such as object picking, servo motion control, or automation experiments.

The robotic arm parts are fully 3D printed and assembled using servo motors and an Arduino microcontroller for control. This project is ideal for learning about mechanical design, 3D printing, electronics, and programming.

🧰 Materials Used
🖨️ 3D Printer: AnkerMake M5

🦾 3D Printed Parts: Robotic arm segments, base, joints (STL files provided)

⚙️ Electronics:

4–6× SG90 or MG90S servo motors

Arduino Uno or Nano

Breadboard and jumper wires

Power supply (5V – 6V recommended)

Push-buttons or joystick module (optional)

📦 Files Included
Arm_Base.stl

Arm_Joint1.stl

Arm_Joint2.stl

Gripper.stl

Arduino_Code.ino

Wiring_Diagram.png

🖨️ 3D Printing Instructions
Printer: AnkerMake M5

Material: PLA or PETG

Layer Height: 0.2 mm

Infill: 20% – 40%

Supports: Enabled (where necessary)

Bed Adhesion: Brim recommended for larger parts

💻 Arduino Code Overview
The included code controls multiple servo motors using basic angles. You can modify it to respond to sensors, buttons, or even Bluetooth.

cpp
Copy
Edit
#include <Servo.h>

Servo baseServo;
Servo joint1;
Servo joint2;
Servo gripper;

void setup() {
  baseServo.attach(3);
  joint1.attach(5);
  joint2.attach(6);
  gripper.attach(9);
}

void loop() {
  baseServo.write(90);
  joint1.write(45);
  joint2.write(135);
  gripper.write(10); // Closed

  delay(2000);

  gripper.write(90); // Open
  delay(2000);
}
🛠️ Assembly Guide
Print all STL parts using the AnkerMake M5.

Insert servo motors into designated slots.

Connect servos to Arduino following the wiring diagram.

Upload the Arduino sketch.

Power up the system and test motion.

🧠 Learning Objectives
3D model slicing and optimization for the AnkerMake M5

Servo motor control using PWM via Arduino

Mechanical design with moving parts and tolerances

Building functional robotic mechanisms

🚀 Future Improvements
Add Bluetooth or Wi-Fi control (ESP32 or HC-05)

Use joystick for real-time control

Add sensors for object detection (ultrasonic or IR)

Upgrade to MG996R servos for stronger load capacity

# anker-make-m5-arm
