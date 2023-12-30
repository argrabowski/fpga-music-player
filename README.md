# FPGA Music Player

## Overview
This project utilizes a Xilinx Zynq FPGA, incorporating a MicroBlaze soft processor and various peripherals on the Basys3 board. The primary functionalities include reading inputs from switches and buttons, updating LEDs, generating musical notes, displaying notes on a seven-segment display, and playing a tune on startup or after a reset.

## Implementation
The project is organized into several files, with the main logic implemented in the `main.c` file. Key functionalities are encapsulated in separate functions, such as reading inputs (`check_switches` and `check_buttons`), calculating note parameters (`calc_note`), and updating outputs (`update_LEDs`, `update_cathode`, `update_anode`, `update_amp2`). The code structure is modular, making it easy to understand and extend.

## Hardware Components
- **FPGA Device:** Xilinx Zynq FPGA
- **Development Board:** Basys3
- **Peripherals:** GPIO modules, Timer (XTmrCtr), and AMP2 Audio Amplifier

## Setup and Configuration
1. **Vivado Project:**
   - Load the provided Vivado project file in the Vivado environment.
   - Configure the MicroBlaze soft processor and necessary IP blocks.

2. **Code Compilation:**
   - Compile the C code using the Xilinx SDK.

3. **FPGA Programming:**
   - Program the FPGA with the generated bitstream.

4. **Run the Application:**
   - Upon startup or reset, the application will play a wake-up tune and perform various musical functionalities based on switch and button inputs.

## File Structure
- **main.c:** Main application logic.
- **xparameters.h:** Definitions of hardware parameters.
- **xgpio.h, xil_types.h, xil_printf.h, xstatus.h, sleep.h, xtmrctr.h:** Header files for necessary libraries.

## Note Frequencies
- The code defines note frequencies for several musical notes (e.g., C3, D3, E3) using constants.
