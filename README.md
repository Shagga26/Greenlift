# 🌱 GREENLIFT: Smart Solar Agri-Carousel Base Station

GreenLift is a space-saving vertical farming carousel designed for tight urban environments, reducing required floor space by over 80%. This system reimagines the traditional plant shelf as a rotating, solar-powered Ferris wheel that allows caretakers to manage crops from a single, confined space.

This repository contains the Arduino C++ codebase and architecture documentation for the smart caretaking base station.

---

## 🏗️ Hardware & Mechanical Build
*   **Structural Chassis:** Constructed using heavy-duty industrial T-Slot aluminum struts for a rigid base and grey PVC pipes for the central rotating cross-hub.
*   **Gravity-Leveling Baskets:** Plant pots are suspended from the outer arms on free-spinning pivot pins. As the wheel spins, gravity ensures every single pot remains perfectly upright to prevent soil and water spillage.
*   **Accessible Maintenance:** The Ferris wheel design eliminates the need for tall ladders; the user simply rotates the desired plant basket down to the bottom base station for inspection, trimming, and watering.

---

## ⚡ Dual-System Architecture
To maximize energy efficiency and integrate renewable power, the GreenLift electrical architecture is divided into two separate circuits:

### System A: Direct-Drive Rotation (Power Circuit)
The spinning mechanism operates independently from the Arduino to handle heavy physical loads.
*   **Power Source:** 100% powered by a sleek renewable solar panel array.
*   **Mechanism:** A high-torque DC gear motor is wired directly to the solar power source.
*   **Control:** The user operates a manual ON/OFF switch to spin the carousel on command and bring the exact plant basket they want down to the base level.

### System B: Smart Base Station (Arduino Control Circuit)
The stationary hub at the bottom acts as the automated caretaking station, powered and controlled by an **Arduino Uno microcontroller**.
*   **Interval Alarm Monitor:** An internal timer tracks the duration between care cycles. Once the specific time interval is reached, the Arduino triggers a digital buzzer sequence to remind the user to spin the carousel and tend to the plants.
*   **Automated Rainwater Dispensing:** The base houses a dedicated rainwater collection reservoir equipped with a 12V micro-submersible pump. When the user presses the control box's push-button, the Arduino activates a relay module, dispensing the harvested rainwater directly into the lowest plant pot for exactly 2 seconds.

---

## 🌍 UN Sustainable Development Goals (SDGs) Alignment
GreenLift was developed under the WSDG theme *"Where Young Minds Meet AI"* and directly supports two primary United Nations SDGs:
*   **SDG 11 (Sustainable Cities & Communities):** Maximizes vertical space to make fresh food production accessible in crowded urban apartments and balconies without taking up valuable floor space.
*   **SDG 2 (Zero Hunger):** Encourages localized, year-round urban agriculture, while utilizing smart tech to conserve water and resources.
