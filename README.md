[![GitHub Release](https://img.shields.io/github/v/release/espressif/esp-ui)](https://github.com/espressif/esp-ui/releases) [![Espressif Release](https://components.espressif.com/components/espressif/esp-ui/badge.svg)](https://components.espressif.com/components/espressif/esp-ui)

[![Arduino Lint](https://github.com/espressif/esp-ui/actions/workflows/arduino_lint.yml/badge.svg)](https://github.com/espressif/esp-ui/actions/workflows/arduino_lint.yml) [![Version Consistency](https://github.com/espressif/esp-ui/actions/workflows/check_lib_versions.yml/badge.svg)](https://github.com/espressif/esp-ui/actions/workflows/check_lib_versions.yml)

# ESP-UI

* [中文版本](./README_CN.md)

## Overview

esp-ui is a UI runtime framework based on [LVGL](https://github.com/lvgl/lvgl), designed to provide a consistent UI development experience for screens of various sizes and shapes. The framework integrates a range of standardized system UIs and application management mechanisms, allowing users to flexibly modify styles, add or remove application UIs, significantly improving the development efficiency of HMI products, and accelerating product development and time-to-market.

Key features include:

- Developed in C++, it can be compiled for `PC` or `ESP SoCs` platforms and supports `VSCode`, `ESP-IDF`, and `Arduino` development environments.
- Offers a rich set of standardized system UIs with support for dynamic UI style adjustments.
- Implements an app-based application management approach, ensuring UI isolation and coexistence across multiple apps, enabling users to focus on UI implementation within their target app.
- Application UIs are compatible with "[Squareline](https://squareline.io/) exported code" development methods.

The system UI functionality demonstration is as follows:

<div align="center"><img src="https://dl.espressif.com/AE/esp-dev-kits/esp_ui_phone_demo_2.gif" alt="phone_demo" width="600"></div>
<p align="center">
<a href="./docs/system_ui_phone.md"> System UI - Phone </a>
</p>
<br>

The functional block diagram of esp-ui is as follows, mainly consisting of the following components:

<div align="center"><img src="docs/_static/readme/block_diagram.png" alt="block_diagram" width="600"></div>
<br>

- **System UI Core**: Implements the unified core logic of all system UIs, including app management, stylesheet management, event management, etc.
- **System UI Widgets**: Encapsulates common widgets for system UIs, including status bar, navigation bar, gesture, etc.
- **System UIs**: Implements various types of system UIs based on "System UI Core" and "System UI Widgets".
- **Squareline**: Contains multiple versions of *ui_helpers* files exported from "Squareline Studio" to avoid function name conflicts when used across multiple apps.
- **Fonts**: Contains the default fonts used by the system UIs.

## Usage

Please refer to the documentation - [How to Use](./docs/how_to_use.md).

## System UIs

Currently, esp-ui offers the following system UIs:

- [Phone](./docs/system_ui_phone.md)

## System UI Widgets

Please refer to the documentation - [System UI Widgets](./docs/system_ui_widgets.md).
