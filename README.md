# Brushless DC Motor Design Project

## Overview

This project presents the design, CAD modelling, 3D printing, winding, assembly, and testing of a small brushless DC motor (BLDC). The motor was designed as a radial flux, three phase, six slot/eight pole outrunner BLDC motor using SOLIDWORKS, 3D printed parts, permanent magnets, copper windings, and an electronic speed controller.

The goal of the project was to complete the full motor design workflow from theory to physical implementation. This included selecting motor specifications, performing design calculations, modelling the stator and rotor in SOLIDWORKS, exporting STL files, assembling the motor, winding the stator, and testing the final prototype.

## Final Technical Report

The full technical report is available here:

[Brushless DC Motor Design Project Report](report/BLDC_Motor_Project_Report.pdf)

## Project Motivation

Brushless DC motors are widely used in electric vehicles, drones, robotics, fans, pumps, and other electromechanical systems because they offer high efficiency, low maintenance, and reliable operation compared with brushed DC motors.

This project was built to answer one main question:

**Can a small custom BLDC motor be designed, fabricated, wound, assembled, and tested using 3D printed components and available lab materials?**

The project demonstrates the complete workflow:

Motor specifications
→ analytical calculations
→ SOLIDWORKS CAD modelling
→ STL export
→ 3D printing
→ stator winding
→ physical assembly
→ ESC testing
→ performance evaluation

## Tools and Technologies

* SOLIDWORKS
* 3D printing
* STL modelling
* BLDC motor design
* Electronic speed controller testing
* Copper winding
* Neodymium magnets
  
## Repository Structure

```text
bldc-motor-design-project/
│
├── assembly/
│   └── full motor assembly files and screenshots
│
├── images/
│   └── project images used for the README and report
│
├── parts/
│   └── SOLIDWORKS part files
│
├── report/
│   ├── main.tex
│   ├── BLDC_Motor_Project_Report.pdf
│   └── figures/
│
├── stl_exports/
│   ├── Rotor.STL
│   ├── StatorBottom.STL
│   └── StatorTop.STL
│
└── README.md
```

## Design Objectives

The main design objectives were:

* Design a small BLDC motor within the required size constraint.
* Use a six slot/eight pole electromagnetic layout.
* Create a radial flux outrunner motor design.
* Model the stator and rotor in SOLIDWORKS.
* Export the rotor and stator parts as STL files for 3D printing.
* Wind the stator using a three phase ABC winding scheme.
* Assemble the motor using the shaft, bearings, magnets, rotor, stator, and test base.
* Test the motor using an electronic speed controller.

## Motor Specifications

| Parameter                  | Value                      |
| -------------------------- | -------------------------- |
| Motor type                 | Radial flux outrunner BLDC |
| Number of phases           | 3                          |
| Stator teeth               | 6                          |
| Rotor poles / magnets      | 8                          |
| Winding scheme             | ABC                        |
| Connection type            | Wye / Star                 |
| Rated torque               | 0.075 N·m                  |
| Rated speed                | 2000 RPM                   |
| Rated voltage              | 12 V                       |
| Estimated rated current    | 1.31 A                     |
| Target air gap             | 2 mm                       |
| Stator outer diameter      | 61 mm                      |
| Rotor inner diameter       | 65 mm                      |
| Rotor outer diameter       | 71 mm                      |
| Axial stack length         | 30 mm                      |
| Calculated turns per tooth | 17 turns                   |
| Actual turns per tooth     | 8 turns                    |

## CAD Design

The motor was modelled in SOLIDWORKS using separate stator and rotor parts. The design focused on motor geometry, shaft alignment, bearing support, magnet placement, 3D printability, and assembly fit.

### Stator Design

The stator was designed with six teeth for a three phase winding layout. The stator includes a central shaft hole, bearing pockets, and a square mounting boss to fit the course test stand.

![Stator CAD Model](report/figures/stator_isometric.png)

### Rotor Design

The rotor was designed as an outrunner can with eight internal magnet pockets. The rotor surrounds the stator, allowing the permanent magnets to rotate around the wound stator teeth.

![Rotor Magnet Pockets](report/figures/rotor_magnet_pockets.png)

### Full Assembly

The full assembly was created in SOLIDWORKS to verify that the rotor and stator were aligned correctly and that the final geometry matched the intended outrunner BLDC design.

![Full BLDC Motor Assembly](report/figures/full_assembly_isometric.png)

## 3D Printing and Fabrication

The stator and rotor parts were exported as STL files and 3D printed. The exported files included:

* `Rotor.STL`
* `StatorBottom.STL`
* `StatorTop.STL`

The stator was split into top and bottom printed sections to improve manufacturability and simplify assembly around the shaft and bearing features. After printing, the parts were checked for fit, clearance, and alignment.

![Assembled 3D Printed Motor](report/figures/assembled_printed_motor.png)

## Winding and Assembly

The stator was wound using an ABC three phase winding arrangement with a wye connection. The calculated design required approximately 17 turns per tooth, but the final physical motor used 8 turns per tooth because the available wire gauge and slot space limited the number of turns that could be physically wound.

Eight N52 neodymium magnets were inserted into the rotor pockets to create the eight pole rotor field. The printed stator, rotor, shaft, bearings, magnets, and test base were then assembled into the final motor prototype.

![Wound Stator Assembly](report/figures/wound_stator_test_base.png)

## Design Calculations

The main design calculations included:

* Angular velocity
* Mechanical output power
* Estimated rated current
* Flux density at the stator surface
* Number of teeth per phase
* Required winding turns per tooth

The rated speed was selected as 2000 RPM. The angular velocity was calculated as:

```text
ω = 2πN / 60
ω = 209.4 rad/s
```

The mechanical power was calculated using:

```text
P = τω
P = 0.075 × 209.4
P = 15.7 W
```

The estimated rated current was calculated using:

```text
I = P / V
I = 15.7 / 12
I = 1.31 A
```

The calculated number of turns per tooth was approximately 17 turns. The final motor used 8 turns per tooth due to physical slot space and wire gauge constraints.

## Testing Methodology

The motor was tested using an electronic speed controller, power supply, and control input. Before testing, the following checks were performed:

* Rotor clearance around the stator
* Shaft and bearing alignment
* Magnet placement
* Winding condition
* Phase wire connections
* Supply voltage limit

The motor response was evaluated based on whether it could start, whether it could sustain rotation, whether the rotor rubbed against the stator, and whether the ESC appeared to drive the motor phases correctly.

## Results

The final motor fit within the required size constraint and was successfully assembled using the 3D printed rotor and stator components. The motor responded to the electronic speed controller and produced slight rotational motion, but it did not sustain continuous independent rotation.

The main successful outcomes were:

* Completed BLDC motor design calculations
* Created stator and rotor CAD models in SOLIDWORKS
* Exported printable STL files
* 3D printed the motor components
* Wound the stator using a three phase winding layout
* Assembled the motor with shaft, bearings, rotor, stator, and magnets
* Tested the motor with an ESC

## Key Findings

The main findings were:

* The six slot/eight pole outrunner layout was appropriate for the project requirements.
* The motor geometry was successfully modelled and assembled.
* The physical prototype fit within the required size envelope.
* The actual air gap was larger than the design target, reducing magnetic coupling.
* The final winding count was lower than the calculated value because of slot space and wire gauge limitations.
* Mechanical friction and alignment issues reduced the available starting torque.
* Correct calculations alone do not guarantee strong physical performance because manufacturing tolerances and assembly quality strongly affect motor behaviour.

## Limitations

This project had several limitations:

* The stator and rotor were 3D printed using plastic rather than laminated ferromagnetic steel.
* The actual air gap was larger than the target design value.
* The motor used 8 turns per tooth instead of the calculated 17 turns per tooth.
* Magnet placement and winding were completed manually.
* Testing was mainly observational.
* The project did not include quantitative measurements of torque, no load speed, phase current, back EMF, or efficiency.

## Future Work

Future improvements could include:

* Reducing the rotor stator air gap.
* Redesigning the stator slots to allow more copper turns.
* Using thinner magnet wire to reach the calculated winding count.
* Improving magnet pocket tolerances and magnet retention.
* Improving shaft and bearing alignment.
* Reducing mechanical friction.
* Measuring phase resistance, current, no load speed, back EMF, torque, and efficiency.
* Comparing the 3D printed prototype with a design using laminated steel stator material.

## Lessons Learned

This project showed that BLDC motor design is not only a calculation problem. Physical performance depends heavily on manufacturing tolerance, winding feasibility, air gap control, magnet placement, bearing alignment, and assembly quality.

The project was successful as a full engineering design exercise because it connected theory, CAD modelling, fabrication, winding, assembly, testing, and performance analysis into one complete electromechanical system.
