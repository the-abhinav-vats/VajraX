# VajraX

**A Robust Single-Channel H-Bridge Motor Driver**

VajraX (वज्रX) is a robust single-channel H-Bridge motor driver designed for brushed DC motor applications. Built around the IR2104 high-side/low-side gate driver and IRLZ44N logic-level MOSFETs, the board delivers efficient bidirectional motor control with PWM speed regulation.

The project was designed entirely in KiCad 9 with a focus on reliability, power integrity, clean PCB layout, and ease of integration into embedded systems, robotics, and automation projects.

---

## Features

- Single-channel full H-Bridge architecture
- IR2104 high-side/low-side gate driver
- IRLZ44N logic-level MOSFETs
- PWM speed control
- Bidirectional motor control
- Bootstrap high-side driving circuit
- On-board 5 V and 3.3 V regulated outputs
- AMS1117 voltage regulators
- Wide high-current PCB traces
- Ground plane optimized layout
- Bulk and decoupling capacitors
- Screw terminal connectors
- Test points for debugging
- Power indication LEDs
- Two-layer PCB design

---

## Hardware Specifications

| Parameter | Value |
|----------|------|
| Input Voltage | 12 V DC |
| Logic Supply | 5 V / 3.3 V |
| Gate Driver | IR2104 |
| MOSFET | IRLZ44N |
| Motor Type | Brushed DC |
| Motor Channels | 1 |
| PWM Control | Supported |
| Direction Control | Supported |
| PCB Layers | 2 |
| Designed Using | KiCad 9 |

---

## System Architecture

The board consists of four major sections:

### H-Bridge
A full H-Bridge constructed using four IRLZ44N N-channel MOSFETs provides forward, reverse, braking, and coast modes for a brushed DC motor.

### Gate Driver
Two IR2104 gate driver ICs generate the high-side and low-side gate signals using bootstrap capacitors and bootstrap diodes for reliable switching.

### Power Supply
The power section accepts a 12 V input and generates regulated 5 V and 3.3 V rails using AMS1117 voltage regulators.

### User Interface
Power indication LEDs, test points, and screw terminal connectors simplify debugging and integration with external controllers.

---

## Pin Configuration

### Power Connector

| Pin | Description |
|-----|-------------|
| 1 | 12 V |
| 2 | 5 V |
| 3 | 3.3 V |

### MCU Interface

| Pin | Description |
|-----|-------------|
| 1 | PWM1 |
| 2 | PWM2 |
| 3 | ENABLE |

### Motor Output

| Pin | Description |
|-----|-------------|
| 1 | Motor Terminal A |
| 2 | Motor Terminal B |

---

## PCB Design Highlights

- Ground plane on both PCB layers
- Wide traces for high-current paths
- Short gate drive traces
- Bootstrap components placed adjacent to gate drivers
- Decoupling capacitors positioned close to IC supply pins
- Compact component placement
- Dedicated mounting holes
- Test points for measurement and debugging

---

## Applications

- Robotics
- Embedded Systems
- Industrial Automation
- Educational Projects
- DIY Electronics
- Mechatronics
- Motor Control Experiments

---

## Repository Structure

```
VajraX/
│
├── Hardware/
│   ├── PCB/
│   ├── BOM/
│  
│
├── Images/
│   ├── Schematic.png
│   ├── PCB_Top.png
│   ├── PCB_Bottom.png
│   └── PCB_3D.png
│
├── Datasheets/
│   ├── IR2104.pdf
│   ├── IRLZ44N.pdf
│   └── AMS1117.pdf
└── README.md
```

---

## Bill of Materials

| Component | Quantity |
|-----------|---------:|
| IR2104 Gate Driver | 2 |
| IRLZ44N MOSFET | 4 |
| AMS1117-5.0 | 1 |
| AMS1117-3.3 | 1 |
| 1N4007 Diode | 2 |
| 470 µF Capacitor | 1 |
| 220 µF Capacitor | 4 |
| 10 µF Capacitor | 2 |
| 100 nF Capacitor | Multiple |
| 10 nF Capacitor | 2 |
| LEDs | 2 |
| Gate Resistors | 4 |
| Pull-down Resistors | 4 |
| Screw Terminal Connectors | 2 |

---

## Design Considerations

- Logic-level MOSFETs selected for efficient switching.
- Separate power regulation for 5 V and 3.3 V peripherals.
- Bootstrap circuit enables high-side N-channel MOSFET operation.
- Ground plane implemented to improve power integrity and reduce noise.
- Wide copper traces used for motor current paths.
- Decoupling capacitors placed close to integrated circuits for stable operation.

---

## Future Improvements

- Current sensing
- Overcurrent protection
- Reverse polarity protection
- Thermal shutdown
- TVS surge protection
- Fault indication
- Current feedback
- UART diagnostics
- CAN interface
- PWM frequency selection

---

## Software Used

- KiCad 9
- Git
- GitHub

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Author

[Abhinav Vats](https://www.linkedin.com/in/abhinavvats06/)

B.Tech Electronics and Communication Engineering

Areas of Interest:
- Embedded Systems
- PCB Design
- Power Electronics
- Robotics
- Internet of Things

---

## Contributing

Contributions, suggestions, and improvements are welcome. If you find any issues or have ideas to improve the design, feel free to open an issue or submit a pull request.

---

## Disclaimer

This project is intended for educational, research, and prototyping purposes. Ensure that the PCB is tested with appropriate safety precautions before operating high-current loads.
