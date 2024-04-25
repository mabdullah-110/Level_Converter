# Bi-Directional Logic Level Converter Repository :electric_plug:


[![License](https://img.shields.io/github/license/hiibrarahmad/Level_Converter?style=for-the-badge)](LICENSE)
[![Latest Release](https://img.shields.io/github/v/release/hiibrarahmad/Level_Converter?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/releases)
[![Contributors](https://img.shields.io/github/contributors/hiibrarahmad/Level_Converter?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/graphs/contributors)
[![Documentation](https://img.shields.io/badge/documentation-yes-brightgreen?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/wiki)
[![Open Issues](https://img.shields.io/github/issues/hiibrarahmad/Level_Converter?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/issues)
[![Stars](https://img.shields.io/github/stars/hiibrarahmad/Level_Converter?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/stargazers)
[![Forks](https://img.shields.io/github/forks/hiibrarahmad/Level_Converter?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/network/members)
[![Last Commit](https://img.shields.io/github/last-commit/hiibrarahmad/Level_Converter?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/commits/main)
[![Release Date](https://img.shields.io/github/release-date/hiibrarahmad/Level_Converter?style=for-the-badge)](https://github.com/hiibrarahmad/Level_Converter/releases)



## Overview :mag_right:
When bridging the gap between 3.3V and 5V systems, the **Bi-Directional Logic Level Converter** offers a seamless solution. This compact device not only steps down 5V signals to 3.3V but also steps up 3.3V to 5V simultaneously. It's versatile, accommodating 2.8V and 1.8V devices as well, making it an asset for various electronic projects.

What distinguishes this level converter is its capability to set high and low voltages and safely step up and down between them on the same channel. Each converter supports up to 5 pins on both the high and low sides, with three inputs and three outputs provided for each side.
![Detail View](https://github.com/hiibrarahmad/Level_Converter/blob/main/pic/Screenshot%202024-04-25%20233035.png)

## Features :sparkles:
- **Bi-directional voltage conversion** between 5V, 3.3V, 2.8V, and 1.8V.
- Convert up to 3 pins from the high side to 3 pins on the low side.
- Safely step up and down between different voltages on the same channel.
- Easy integration into projects requiring different logic levels.

## How to Use :wrench:
To start using the level converter, follow these steps:
- **High Voltage (HV)**: Connect the high voltage (e.g., 5V) to the 'HV' pin.
- **Low Voltage (LV)**: Connect the low voltage (e.g., 3.3V) to the 'LV' pin.
- **Ground (GND)**: Connect the ground from your system to the 'GND' pin.
- **Low Voltage (LV1/LV2/LV3)**: Connect the low voltage (e.g., 3.3V) to be converted to high voltages to the respective pins.
- **High Voltage (HV1/HV2/HV3)**: Connect the high voltage (e.g., 5V) to be converted to low voltages to the respective pins.

Ensure that both high and low voltage sources are powering the board for proper operation.

## Applications :bulb:
This level converter finds utility in:
- Safely connecting low voltage devices to higher voltage systems.
- Enabling IoT devices with secure logic level conversion.
- Compatibility in multi-voltage environments.

## Contributing :handshake:
Feel free to fork this repository, make enhancements, and submit pull requests. We welcome improvements and value your contributions!

## License :memo:
Distributed under the MIT License. See `LICENSE` for more information.

## Contact :phone:
For further details and support, please reach out to us via [GitHub Issues](https://github.com/hiibrarahmad/Level_Converter/issues) or email.

---

Thank you for exploring our bi-directional logic level converter. Happy building! :hammer_and_wrench:

## Board Overview
The board's schematic reveals a simple yet effective design for bi-directional logic level conversion. Each channel employs a level-shifting circuit, comprising a single N-channel MOSFET and pull-up resistors, replicated three times across the board.

Through semiconductor wizardry, this circuit seamlessly shifts signals between different voltage levels, ensuring that a 0V signal on one end remains 0V on the other.

### Pinout
The board features a total of 10 pins across two parallel rows of five headers. One row is dedicated to high voltage inputs and outputs, while the other handles low voltage.

The pins are labeled on both sides of the board and organized into groups. Here's a closer look at some key pin groups:

#### Voltage Inputs
Pins labeled HV, LV, and two GNDs serve as references for high and low voltages. Supplying regulated voltages to these inputs is essential for proper functionality.

The voltage at HV and GND inputs should exceed that at LV. For instance, when interfacing from 5V to 3.3V, HV should be 5V, and LV should be 3.3V.

#### Data Channels
The board features three independent data channels capable of bidirectional shifting between high and low voltages. Pins HV1, LV1, HV2, LV2, HV3, and LV3 denote these channels, with the number indicating the channel and HV/LV indicating the voltage side.

For example, a low-voltage signal input at LV1 will be shifted up to a higher voltage and outputted from HV1. Conversely, a signal input at HV3 will be shifted down and outputted from LV3. Utilize as many channels as your project necessitates.

Note that these level shifters operate exclusively in the digital domain and cannot convert analog voltages.

