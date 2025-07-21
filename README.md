# FPGA Capstone Project – Module II  
### Mixed-Signal System Design with PWM and ADC using Altera MAX10  

**Author:** Abhijit Rai  
**Institution:** Army Institute of Technology, Pune  
**Course:** University of Colorado Boulder – FPGA Specialization (Coursera)  
**Module:** Course 4 – Capstone Project: Module II  
**Date:** Nov 2024  

---

## Project Overview

This project implements a **mixed-signal system** using Intel’s MAX10 FPGA on the DE10-Lite board. It integrates analog voltage sensing via the on-chip ADC and digital control through a Pulse Width Modulation (PWM) circuit. Designed as part of CU Boulder’s FPGA Capstone sequence, the system demonstrates analog input acquisition, signal processing, and LED-based feedback.

---

## Learning Outcomes

Through this project, the following skills were developed:

- Using Quartus Prime Lite Edition for complete FPGA design flow.
- Designing and simulating a PWM control system.
- Integrating on-chip ADC blocks and reading analog voltage levels.
- Creating custom hardware subsystems with Qsys (Platform Designer).
- Performing timing analysis and waveform simulation with ModelSim.
- Documenting all development steps and observations in a formal lab notebook.

---

## Development Environment

| Component       | Details                                  |
|----------------|-------------------------------------------|
| **FPGA Device** | Intel MAX10 FPGA (Flash-based, 55nm)     |
| **Board**       | DE10-Lite by Terasic                     |
| **Toolchain**   | Quartus Prime Lite v16.1, ModelSim, USB Blaster |
| **Design Tools**| Qsys (Platform Designer), Schematic Capture |
| **Reference Files** | `pwm_led_top.bdf`, `debouncer.v`, ADC modules |

---

## Implementation Phases

### A. PWM Subsystem – Digital Output Control

1. **Environment Setup**
   - Installed Quartus Prime v16.1 Lite and drivers.
   - Created working directory: `C:\AlteraPrj\DE10litePWM`.
   - Imported PWM reference design files from provided `.zip`.

2. **Circuit Design**
   - Built the PWM circuit using schematic entry (`.bdf`) and Verilog modules.
   - Defined input switches and LED-based visual output.

3. **Simulation**
   - Used ModelSim to simulate PWM timing and validate duty cycle behavior.

4. **Synthesis and Fitting**
   - Analyzed synthesis reports: Fmax, logic utilization, and flip-flop count.
   - Resolved logic warnings and unconstrained paths.

5. **Programming and Testing**
   - Programmed board using `.sof` file via USB Blaster.
   - Verified LED blinking patterns and PWM modulation under switch control.

---

### B. ADC Subsystem – Analog Input Monitoring

1. **Preparation**
   - Extracted ADC design components and integrated them into the existing project.

2. **System Creation in Qsys**
   - Instantiated and configured the on-chip ADC core.
   - Connected ADC read logic through schematic and HDL modules.

3. **Compilation**
   - Completed routing and compilation stages.
   - Debugged path constraints and simulation mismatches.

4. **Functional Validation**
   - Applied varying voltages to analog input.
   - Verified dynamic 7-segment display output reflecting voltage magnitude.

5. **Performance Metrics**
   - Captured Fmax, logic usage, and flip-flop count from final reports.
   - Compared display readings to expected voltmeter outputs.

---

## Project Deliverables

- `DE10litePWM` project folder containing:
  - Quartus source files: `.qpf`, `.bdf`, `.v`, `.sof`
  - System configuration and simulation data
- Structured **engineering lab notebook** (PDF), including:
  - Design decisions and simulation snapshots
  - Compilation and resource usage logs
  - Board-level testing results for PWM and ADC systems

---

## Evaluation Criteria

| Component             | Description                                |
|----------------------|--------------------------------------------|
| **Design Functionality** | Working PWM and ADC subsystems          |
| **Simulation Accuracy** | Verified behavior through ModelSim       |
| **Documentation Quality** | Clear and complete engineering records |
| **Board Validation**     | Correct and responsive hardware outputs |
| **Submission Format**    | Zipped project folder + lab notebook PDF|

---

## References

- [CU Boulder Coursera – FPGA Capstone: Module II](https://www.coursera.org/learn/fpga-capstone)  
- [Intel Quartus Prime Lite v16.1 Documentation](https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html)  
- [Terasic DE10-Lite SystemCD and User Guide](https://www.terasic.com.tw/)  
- [ModelSim Simulation Tool Documentation](https://eda.sw.siemens.com/en-US/ic/modelsim/)  

---

## Acknowledgements

This project was completed under the **University of Colorado Boulder’s FPGA Specialization** on Coursera. Educational licenses were used for all tools and reference materials.

Special thanks to:

- **Intel Corporation** – FPGA devices and software  
- **Terasic Technologies** – DE10-Lite hardware support  
- **Professor Timothy Scherr** and CU Boulder faculty – For structured guidance and real-world hardware insight

---

## Summary

This module delivered a practical and verified implementation of a **mixed-signal voltmeter system** on the DE10-Lite FPGA platform. The project successfully integrated PWM output logic with analog input acquisition via ADC, providing both simulation-based and physical board-level confirmation of expected functionality.
