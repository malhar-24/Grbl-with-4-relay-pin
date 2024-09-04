# GRBL Firmware with Custom Relay Control

## Overview

This is a customized version of the GRBL firmware designed to control four relays using specific commands. The relays are connected to the following Arduino pins:


- **Pin A3**: Relay control with M10 (on) and M11 (off) commands.
- **Pin A4**: Relay control with M20 (on) and M21 (off) commands.
- **Pin 12**: Relay control with M40 (on) and M41 (off) commands.
- **Pin 13**: Relay control with M50 (on) and M51 (off) commands.

**Baud Rate is 115200**(change it if necessary in config.h file) 
  
## Features

- Standard GRBL CNC control.
- Additional relay control through custom M-codes.
- Configurable pin assignments.

## Pin Configuration

The following pins are assigned for relay control:

| Relay | Pin  | Command On | Command Off |
|-------|------|------------|-------------|
| Relay 1 | A3   | M10        | M11         |
| Relay 2 | A4   | M20        | M21         |
| Relay 3 | 12   | M40        | M41         |
| Relay 4 | 13   | M50        | M51         |

## Installation

1. **Download and Extract**: 
   - Download this modified version of GRBL from the provided repository or clone it using git.

2. **Arduino IDE**: 
   - Open the `grbl` folder inside the Arduino IDE.

3. **Modify Configuration (if needed)**: 
   - If you need to change any pin configurations, edit the `config.h` file.
   
4. **Upload to Arduino**:
   - Select your Arduino board from the Tools > Board menu.
   - Upload the GRBL firmware to your Arduino.

## Custom Commands

This modified version of GRBL includes custom M-codes for controlling the relays:

- **Relay 1 (Pin A3)**
  - **M10**: Turn Relay 3 ON
  - **M11**: Turn Relay 3 OFF

- **Relay 2 (Pin A4)**
  - **M20**: Turn Relay 4 ON
  - **M21**: Turn Relay 4 OFF
   
- **Relay 3 (Pin 12)**
  - **M40**: Turn Relay 1 ON
  - **M41**: Turn Relay 1 OFF

- **Relay 4 (Pin 13)**
  - **M50**: Turn Relay 2 ON
  - **M51**: Turn Relay 2 OFF

## Usage

1. **Connect Relays**:
   - Connect your relays to the corresponding pins on the Arduino as listed in the pin configuration table.
   
2. **Control Relays**:
   - Use the custom M-codes listed above in your G-code files to control the relays.

3. **Test**:
   - Send commands manually through your preferred G-code sender software to test the relay control.

## Troubleshooting

- **Relay not responding**: Ensure the correct pin is assigned and that the relay is wired correctly.
- **M-code not recognized**: Verify that you have uploaded the correct firmware version and that the custom M-codes are included in the G-code file.

## Contribution

Feel free to contribute to this project by submitting issues or pull requests on the repository.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---
