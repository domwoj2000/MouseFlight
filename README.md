# MouseFlight (Rust)

**MouseFlight** is a Windows utility that converts raw mouse movement into 2-axis virtual joystick signals via vJoy, designed specifically for flight simulators and space combat games that require smooth, continuous pitch and roll joystick inputs.

MouseFlight is a flight-control-focused fork of [MouseDrive](https://github.com/Toxpox/MouseDrive), adapted for mouse-based flight stick emulation.

---

## Features

- **2-Axis Flight Control** — Maps relative mouse movement directly to virtual joystick axes (typically X for Roll / Z for Pitch, with Y and Rz available for throttle and brake).
- **Raw Input Capture** — Captures mouse movement seamlessly, even when the game window isn't explicitly focused (Toggle with `F8`).
- **Lock-free Architecture** — Utilizes atomic globals between the raw input thread and GUI thread for zero-stutter performance.
- **Configurable Curves & Sensitivity** — Fine-tune deadzones, response curves, and scaling so your plane doesn't twitch uncontrollably.
- **Lightweight GUI** — Built with Rust and `eframe/egui` for a clean, low-overhead configuration interface.

---

## Quick Start

1. **Install vJoy** and configure a device with **X, Y, Z and Rz axes** enabled (Device 1 recommended).
2. Ensure `vJoyInterface.dll` is available (place it next to `MouseFlight.exe`, in your Program Files, or inside your system PATH).
3. Run **MouseFlight**.
4. Bind your flight simulator's controls to your vJoy device axes (Pitch & Roll).
5. Press **F8** to toggle mouse capture and take flight!

---

## Configuration

Settings are automatically saved in TOML format:
- Portable mode: `./config.toml`
- Standard mode: `%APPDATA%\MouseFlight\config.toml`

---

## License

Copyright (c) 2025-2026 Toxpox. 
Licensed under the MIT License.
