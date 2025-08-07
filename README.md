# Obstacle Avoidance with Ultrasonic Sensor and Servo Motor (Using L293D Shield)

## 📌 Project Overview

This Arduino project demonstrates how to use a **servo motor** connected via the **L293D motor driver shield** along with an **ultrasonic sensor (HC-SR04)** to detect and avoid obstacles.

The ultrasonic sensor is **mounted on top of the servo motor**, allowing it to **rotate and scan a wider area**. When an obstacle is detected within **10 cm**, the motor stops and changes direction.

---

## 🧰 Components Used

- Arduino UNO  
- L293D Motor Driver Shield  
- HC-SR04 Ultrasonic Sensor  
- Servo Motor  
- Jumper Wires  
- Breadboard 
- Mount for sensor  (It was attached to the repository under the name "Mount")
- Power Source  

---

## 🔌 Connections Overview

- **Servo Motor:**  
  Connected to one of the pins via the L293D shield (D9)

- **Ultrasonic Sensor (mounted on servo):**  
  - VCC → 5V  
  - GND → GND  
  - Trig →  Connected to one of the pins via the L293D shield (D10)  
  - Echo →  Connected to one of the pins via the L293D shield (D2)

- **L293D Shield:**  
  Mounted directly on the Arduino UNO to control the motor.

---

## 🔄 Motion and Scanning Logic

- The servo rotates the ultrasonic sensor left and right to **scan the environment**.
- If an object is detected at **≤ 10 cm**, the movement motor:
  - **Stops**
  - **Changes direction** after a delay
- If no object is detected, the robot continues moving forward.

---

## ⚙️ Behavior Summary

| Condition               | Action Taken                |
|-------------------------|-----------------------------|
| No object (< 10 cm)     | Motor moves forward         |
| Object detected ≤ 10 cm | Motor stops, then reverses  |
| Servo Rotation          | Sweeps left and right for wider detection |

---

result:

https://youtube.com/shorts/DChnwZdUl6c?feature=shared
