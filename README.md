# PCB Design Class — Semester Projects

This repository contains all the PCB design projects completed throughout my PCB Design course, created using **KiCad**. The projects progressively build on each other, covering fundamental circuit concepts from simple switching circuits to microcontroller-based systems, culminating in a full AC to DC power converter as the final project.

---

## Project 01 — Mini Inverter

A half-bridge DC inverter circuit built around the **IR2153 self-oscillating half-bridge driver** and two **N-Channel Power MOSFETs (17A, 60V, TO-220)**. The circuit drives a transformer to produce an AC-like output from a DC battery source. LEDs are used for status indication. This was the introductory project, covering basic switching topologies, MOSFET gate driving, and transformer-coupled power circuits.

**Key components:** IR2153, N-Channel MOSFETs, transformer, LED, battery

---

## Project 02 — Arduino Nano + LCD Display

A microcontroller-based project integrating an **Arduino Nano v3.x** with an **NHD-0420E2Z LCD display** (4×20 character). The board routes power, data lines, and passive components between the module and the display. This project introduced working with microcontroller modules in KiCad, footprint assignment for through-hole and SMD packages, and multi-component PCB layout.

**Key components:** Arduino Nano v3.x, NHD-0420E2Z LCD, resistors, capacitors, battery

---

## Project 03 — 4-Digit 7-Segment LED Display Driver

A display driver circuit built around the **CC56-12SRWA** — a 4-digit, 7-segment super bright red LED display (common cathode). The schematic routes the segment and digit control lines from a battery-powered source. This project focused on understanding multi-digit display multiplexing, current-limiting resistors for each segment, and organizing a moderately complex schematic cleanly.

**Key components:** CC56-12SRWA (4-digit 7-segment display), resistors, single-cell battery

---

## Project 05 — LED Sequencer (CD4017 + NE555 Timer)

A classic LED chaser/sequencer circuit using the **CD4017 Johnson Counter** (10 decoded outputs) driven by the **NE555 timer IC** configured in astable mode. The 555 generates a clock signal that steps the 4017 through its outputs sequentially, lighting one LED at a time in a running pattern. This project explored timer circuits, clocking logic ICs, and the fundamentals of sequential logic on a PCB.

**Key components:** CD4017B, NE555 (SOIC-8), LEDs, resistors, capacitors, single-cell battery

---

## Project 06 — Sound-Activated Relay (Clap Switch)

A sound-triggered switching circuit that uses an **ECM microphone (AOM-6545P-R)** to pick up audio signals, amplified by the **OPA27GP precision op-amp**. The amplified signal is processed by a **74LS109 Dual JK Flip-Flop** to toggle a **PR12 5V relay (SPDT)** via a **TIP122 NPN Darlington transistor**. A trimmer potentiometer sets the sensitivity threshold. This project brought together analog signal conditioning, digital logic, and electromechanical output on one board.

**Key components:** AOM-6545P-R ECM mic, OPA27GP op-amp, 74LS109 JK flip-flop, TIP122 Darlington transistor, PR12-5V-360-1C relay, 1N4001 flyback diode, trimmer potentiometer

---

## Project 07 — USB-C Powered LED Dimmer

A variable LED brightness circuit powered through a **USB Type-C receptacle (6-pin, power-only)**. The circuit uses a **BD140 PNP power transistor** as the main switch, a **TL431D shunt voltage regulator** for reference, and a **potentiometer (RK163)** to allow manual dimming control. A fast-switching diode (1N4148WT) handles transient protection. This project introduced USB-C power input integration and analog control of LED brightness through transistor biasing.

**Key components:** USB_C_Receptacle_PowerOnly_6P, BD140 PNP transistor, TL431D shunt regulator, RK163 potentiometer, 1N4148WT diode, LED, resistors

---

## Project 08 — Stereo Audio Amplifier (LA4440)

A two-channel stereo audio amplifier board built around the **LA4440-E**, a Class AB 2-channel amplifier IC in a 14-pin SIP package (by onsemi). The board includes the necessary input/output coupling capacitors and resistor network as specified in the datasheet. This project covered audio amplifier PCB layout considerations such as ground planes, decoupling, and heat dissipation for power ICs.

**Key components:** LA4440-E stereo amplifier IC (14-SIP), capacitors, resistors

---

## Final Project — AC to DC Power Supply Converter

The semester capstone project: a full **AC to DC rectifier and filter circuit** designed from scratch. The circuit takes an AC input through screw terminals, passes it through a **bridge rectifier built with four 1N4007 diodes** (1000V, 1A, DO-41), and smooths the output using **polarized electrolytic capacitors**. An LED with a current-limiting resistor serves as a power indicator. 

This project brought together everything learned in the course — schematic design, footprint assignment, PCB layout, design rule checks, Gerber file export, and board revision management.

**Key components:** 1N4007 rectifier diodes ×4 (bridge configuration), polarized electrolytic capacitors, resistor, LED, screw terminals (AC input / DC output)

---

## Tools Used

- **KiCad** — Schematic capture, PCB layout, Gerber export
- **Git** — Version control and project history

---

## Repository Structure

```
├── Project 01/           # Mini Inverter
├── Project_02/           # Arduino Nano + LCD Display
├── Project_03/           # 4-Digit 7-Segment Display
├── Project 05/           # LED Sequencer (4017 + 555)
├── PROJECT_06/           # Sound-Activated Relay
├── PROJECT_07/           # USB-C LED Dimmer
├── Project_08/           # Stereo Audio Amplifier
└── FINAL_PROJECT- AC to DC Converter/   # Full-Wave Rectifier Power Supply
```

Each folder contains the KiCad project files (`.kicad_sch`, `.kicad_pcb`, `.kicad_pro`), Gerber outputs where applicable, and automated KiCad backup archives.