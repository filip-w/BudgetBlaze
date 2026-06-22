# Budget Blaze 🔥
An ultra-budget DIY CNC plasma table built by adapting a laser cutter XY table with a Parkside (Lidl) plasma cutter. 

---

## 📌 Project Overview
The goal of this project was to build a functional CNC plasma cutting table for a fraction of the cost of commercial units. By leveraging the existing mechanics of a cheap/broken laser cutter and the affordability of Parkside tools, **Budget Blaze** proves you don't need thousands of dollars to get into CNC metal cutting.

> ⚠️ **Disclaimer:** Plasma cutters involve high voltages, intense UV light, compressed air, and molten metal. Build and operate at your own risk!

---
<img width="1500" alt="20260524_144556" src="https://github.com/user-attachments/assets/f53a8915-d30b-428c-b888-21884a9161b1" />

## 🛠️ Hardware & Components

### 1. The Motion System (XY Table)
* **Source:** [Insert Laser Cutter model, e.g., K40, cheap diode laser frame, etc.]
* **Modifications:** [Mention if you had to extend the axes, shield the belts from sparks, or beef up the stepper motors].

### 2. The Plasma Cutter
* **Model:** Parkside (Lidl) [Insert model number, e.g., PPS 40 B2]
* **Torch Trigger Modification:** [Explain how you spliced into the torch trigger switch to allow the CNC board to fire the plasma. Did you use a relay?]

### 3. Electronics & Control
* **Controller Board:** [e.g., Arduino Uno with CNC Shield, GRBL, Mach3 board]
* **Firmware:** [e.g., GRBL, FluidNC]
* **Relay Module:** Used to isolate and trigger the plasma torch.

📊 Bill of Materials (BOM)

|Component|Description|Source|
|-------|-----|----------|
|XY Laser Frame|The foundational mechanical chassis and motion system|[AliExpress Link](https://s.click.aliexpress.com/e/_c3vjAaQ1)|
|CNC Torch|Straight-head plasma torch upgrade for easier CNC mounting|[AliExpress Link](https://s.click.aliexpress.com/e/_c3OPOTJf)|
|Relay Board|5V relay module used to safely isolate and trigger the torch circuit|[AliExpress Link](https://s.click.aliexpress.com/e/_c4W0Wmgd)|
|Plasma Cutter|Parkside (Lidl) inverter plasma cutter|Lidl / Local Hardware|
|Controller|Microcontroller running GRBL|Included with the XY laser frame|
---

## 📐 How It Was Built (The Process)

### Step 1: Preparing the Frame
* Assemble the laser cutter frame.
* Designed a custom mount to hold the heavy plasma torch instead of the lightweight laser head.
  <img width="878" height="1027" alt="image" src="https://github.com/user-attachments/assets/7eb1e03c-1b62-436a-8c2b-9cd08e56eca7" />


### Step 2: Wiring the Torch Trigger
* Open the plasma torch handle (or the machine casing) to locate the two trigger wires.
* Wired these into a **5V Relay Module** connected to the CNC controller's spindle/laser pin. When the software commands "Laser ON" (or Spindle ON), the relay closes the circuit and fires the plasma.

### Step 3: Software & Calibration
* **CAD/CAM Software:** [e.g., Inkscape, Fusion 360, SheetCAM]
* **G-Code Sender:** [e.g., Universal Gcode Sender (UGS), Candle, OpenBuilds CONTROL]

---

## 💡 Lessons Learned & Tips
* **Spark/Slag Protection:** Laser cutters aren't built for flying sparks. I had to add [shielding/a water table] to protect the linear rails and belts.
* **EMF Interference:** Plasma cutters produce massive High-Frequency (HF) or blowback interference that can crash the controller.

---

## 📸 Media & Demos
<img width="1500" alt="20260524_144711" src="https://github.com/user-attachments/assets/dcb32bb1-4430-4828-93bf-b2dffa5573a9" />

---

## 📄 License
This project is open-source under the MIT License. Feel free to clone, modify, and build your own!
