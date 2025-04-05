# Zephyr Atom Wi-Fi Sample

![CI](https://github.com/tamegai-m/zephyr-atom-wifi-sample/actions/workflows/ci.yml/badge.svg)

This repository is a sample Zephyr project for running on **M5Stack ATOM Lite (ESP32)** with **Wi-Fi enabled**, based on Zephyr v4.1.99.

## Features

- Wi-Fi scan, connect and ping from Zephyr shell
- Built with ESP32 toolchain (gcc8_4_0-esp-2021r2-patch5)
- GitHub Actions for CI build (see `.github/workflows/ci.yml`)

## Build locally

```bash
west build -b m5stack_atom_lite/esp32/procpu . \
  -- -DCONFIG_ESP32_USE_UNSUPPORTED_REVISION=y

# 📁 Folder Structure

# This project expects the following layout on your local machine:

# ```
# ~/projects/
# ├── bootloader/              # Optional bootloader (e.g., MCUboot)
# ├── modules/                 # Additional West modules
# ├── zephyr_atom_wifi_sample/ # Application directory (this repository)
# ├── tools/                   # Tools and helper scripts
# └── zephyr/                  # Zephyr RTOS source (west init -l .)
# ```

# Execute `west build` from within `zephyr_atom_wifi_sample/`.
# This setup mirrors the structure described in the accompanying Qiita article.

