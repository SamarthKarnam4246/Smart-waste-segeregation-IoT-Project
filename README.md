🗑️ Smart Dustbin (Arduino Based)

This project is an Arduino-powered Smart Dustbin that uses sensors, a servo, and a stepper motor to automate waste disposal.
It detects objects, opens/closes the lid, and provides alerts, making waste disposal hands-free and hygienic.

✨ Features

👋 Automatic Lid Opening

Proximity sensor detects a hand/object → servo motor opens/closes dustbin lid.

🚪 Smart Stepper Mechanism

Stepper motor rotates a flap/container for waste segregation or movement.

🔦 IR Sensor Trigger

Additional IR sensor to control operations.

🌱 Soil Sensor (Repurposed as weight/threshold demo)

Used as an analog input to simulate capacity sensing of dustbin.

🔊 Buzzer Alerts

Beeps when dustbin is full or when sensors are triggered.

🛠 Hardware Requirements

Arduino Uno / Nano / Mega

Servo Motor (SG90/MG90s) – controls dustbin lid

Stepper Motor (28BYJ-48 + ULN2003 driver) – rotates inner mechanism

IR Sensor – detects trash insertion

Proximity Sensor – detects hand/object near lid

Buzzer – for alerts

Soil/Analog Sensor – simulates bin fill level

Breadboard, jumper wires, external power supply

📂 Pin Connections
Component	Pin (Arduino)
IR Sensor	5
Proximity Sensor	6
Buzzer	12
Servo Motor	7
Stepper Motor	8, 9, 10, 11
Analog Sensor	A0
💻 Libraries Used

CheapStepper

Servo

⚙️ How It Works

Idle State:

Servo lid stays closed.

Stepper in neutral position.

Proximity Trigger:

When a person approaches, proximity sensor detects → buzzer alert → stepper rotates → servo opens/closes lid.

IR + Fill Level:

IR sensor detects insertion.

Soil/analog sensor reads value to estimate fill level.

If bin > 20% → rotates stepper for waste handling.

Else → buzzer alert + lid cycles.

📊 Example Serial Monitor Output
Proximity Detected: 0
Lid Opening...
Soil Sensor Reading: 35%
Bin Capacity: OK

Proximity Detected: 0
Soil Sensor Reading: 80%
Bin Full → Buzzer Alert




