## Executive Summary

This portfolio artifact showcases the design and implementation of a thermostat control system developed for CS-350 Emerging Systems Architecture & Technologies at Southern New Hampshire University. The project demonstrates finite state machine design, embedded-style hardware interaction, and structured control logic implemented in Python.

The system integrates real-time temperature monitoring, hardware input handling, LED output signaling, and multithreaded execution to simulate real-world embedded thermostat behavior. This artifact reflects my ability to design maintainable, reliable systems while working within hardware constraints and debugging complex runtime issues.

# Thermostat State Machine – Embedded Systems Portfolio Artifact

**Course:** CS-350 Emerging Systems Architecture & Technologies  
**Student:** Emireth Castro  
**Institution:** Southern New Hampshire University  

---

## Project Summary and Problem Solved

This project implements a fully functional thermostat control system using a finite state machine (FSM) architecture. The objective was to design an embedded-style application that interfaces with physical hardware components, manages environmental control logic, and maintains predictable, safe operation across multiple system states.

The core problem addressed was how to manage heating and cooling behavior in a controlled, maintainable way while responding to real-time temperature data and user input. The solution required coordinating hardware input, LED output, timing logic, and state transitions in a manner consistent with real-world embedded systems.

This artifact demonstrates my ability to design and implement software that directly interfaces with hardware while maintaining clarity, stability, and correctness.

---

## System Architecture and Design Decisions

The thermostat was designed using a finite state machine (FSM) to enforce structured system behavior. The application operates in one of three mutually exclusive states:

- **OFF** – System idle with no active output  
- **HEAT** – Heating logic enabled  
- **COOL** – Cooling logic enabled  

State transitions occur in a deterministic circular sequence:


This design ensures that the system never enters an undefined or unsafe state. State transitions are triggered exclusively by a dedicated hardware input (red button), while configuration changes (temperature adjustments) are handled independently. This separation of responsibilities improves reliability and mirrors best practices in embedded systems design.

---

## Functional Behavior and Hardware Interaction

The thermostat continuously monitors temperature data and compares it to a user-defined setpoint. Visual feedback is provided through LED indicators to communicate system behavior clearly.

### Heating Logic
- When the temperature is below the setpoint, the red LED pulses to indicate active heating.
- When the temperature meets or exceeds the setpoint, the red LED remains solid, indicating heating is no longer required.

### Cooling Logic
- When the temperature exceeds the setpoint, the blue LED pulses to indicate active cooling.
- When the temperature is at or below the setpoint, the blue LED remains solid.

### OFF State
- All LEDs are disabled, ensuring no unintended system activity occurs.

This behavior accurately reflects real thermostat control logic and demonstrates effective hardware/software integration.

---

## Multithreading and System Stability

A background display management thread was implemented to handle display updates and debugging output independently of the main execution loop. This allowed the system to remain responsive while continuously running.

The use of multithreading reinforced the importance of non-blocking operations in embedded systems and ensured that the system could handle ongoing tasks without performance degradation.

---

## Debugging, Iteration, and Problem Solving

This project involved extensive debugging and iterative refinement. Multiple failed runs occurred due to syntax errors, state logic issues, and hardware timing constraints. Temperature read errors were occasionally encountered due to hardware input limitations.

These challenges were addressed by:

- Adding detailed debug output to trace state transitions and temperature values  
- Isolating and testing individual system components  
- Implementing defensive programming techniques to prevent system crashes  
- Repeatedly validating behavior against expected state machine logic  

Persisting through these challenges strengthened my debugging skills and reinforced the importance of methodical problem-solving in embedded environments.

---

## What I Did Particularly Well

I excelled at implementing and debugging the finite state machine architecture. Clearly defining system states and transitions made the application easier to reason about, test, and maintain. I also successfully integrated hardware input, LED output, and concurrent execution into a cohesive and reliable system.

---

## Areas for Improvement

One area for improvement would be incorporating more structured incremental testing earlier in development. While the final system is stable and complete, earlier isolation of hardware-related issues could have reduced overall debugging time. This insight will inform my approach to future embedded and hardware-integrated projects.

---

## Tools, Technologies, and Resources Used

- Python 3  
- Raspberry Pi GPIO libraries  
- Multithreading concepts  
- Terminal-based debugging  
- Hardware reference documentation  
- Course-provided materials  

These tools strengthened my ability to bridge software design with physical hardware constraints.

---

## Transferable Skills and Professional Value

This project developed several skills that are directly transferable to future coursework and professional roles, including:

- Finite state machine design  
- Embedded systems architecture  
- Hardware/software integration  
- Debugging complex, real-time systems  
- Writing maintainable and adaptable code  

These competencies are applicable to embedded development, automation, IoT systems, and control applications.

---

## Maintainability, Readability, and Adaptability

The codebase was structured to be readable, modular, and maintainable. Responsibilities are clearly separated, and state logic is centralized for clarity. The finite state machine design allows additional features or states to be added with minimal refactoring, making the system adaptable for future enhancements.

---

## Reflection and Portfolio Context

This artifact represents a significant milestone in my development as a computer science student. It demonstrates my ability to design, implement, debug, and refine an embedded-style system while managing real-world constraints. The lessons learned from this project—particularly in persistence, debugging, and system design—will directly inform my future work in emerging systems and related fields.
## Selected Portfolio Artifacts

The following artifacts were selected for inclusion in my CS-350 portfolio submission:

1. **Thermostat Control Program (Thermostat.py)**  
   Demonstrates embedded-style finite state machine logic, hardware input handling, LED output control, multithreading, and real-time system behavior.

2. **Thermostat State Machine Design Documentation**  
   Visual and written documentation illustrating system states, transitions, and control logic used to ensure predictable and safe operation.

These artifacts were chosen because they best represent my technical strengths in emerging systems architecture, embedded design principles, and hardware/software integration.
