# OpenHAB Home Automation

A collection of custom **OpenHAB** configurations, scripts and automations developed for my personal smart home.

> **Disclaimer**
>
> This repository contains configurations designed specifically for my own installation. It is **not** intended to be a plug-and-play solution, but it may serve as a useful reference for other OpenHAB users looking for similar integrations.

---

## About this project

Most of the work collected here has been developed by combining my own ideas with information, examples and discussions found across the OpenHAB community, GitHub repositories, forums, blog posts and other online resources.

Whenever possible, I will try to properly credit the original sources within the relevant sections of the repository.

This project is my way of giving something back to the community. I have learned a great deal from the work shared by others over the years, and I hope these configurations and scripts can save someone else time or provide inspiration for solving similar problems.

If this repository helps even one person, then it has achieved its goal.

---

## Features

This repository mainly focuses on three custom integrations:

---

## ⚡ Solis S5 Hybrid Inverter (Modbus TCP)

A custom integration for the **Solis S5 Hybrid Inverter** using an external Modbus server.

### Main features

- Read inverter operating data
- Battery monitoring
- PV production monitoring
- Grid import/export monitoring
- Dynamic inverter control
- **Automatic management of export power according to CEI 0-21 limits**
- OpenHAB rules for advanced energy management

The export limiting logic continuously adjusts the inverter active power output to prevent exported power from exceeding the configured threshold.

The goal is to maximize photovoltaic export while respecting grid connection limitations.

---

## ❄️ Viessmann / Gree Air Conditioner Integration

Custom integration for Viessmann air conditioners based on the Gree platform.

### Features

- Power control
- Operating mode selection
- Fan speed control
- Target temperature adjustment
- Swing control
- Temperature monitoring
- OpenHAB automation support

The goal here is to control air conditioners through a better and more customizable interface, since the original vendor applications do not always provide the flexibility and user experience I was looking for.

Unfortunately, the cloud connection used by these split units is still not very reliable, so occasional downtime and communication issues may remain.

---

## 🔥 Smart Water Heater Control

Automatic management of a domestic electric water heater using:

- **Shelly** relay
- **Solis S5 Hybrid Inverter**
- OpenHAB automation rules

The system intelligently activates the heating element when photovoltaic surplus energy is available, increasing self-consumption and reducing unnecessary energy export or grid consumption.

---

# Repository Structure

```text
.
├── things/
├── items/
├── rules/
├── scripts/
├── transformations/
├── persistence/
├── mainui/
└── misc/
```

The structure may evolve over time as new integrations and automations are added.

---

# Requirements

The examples in this repository assume familiarity with:

- OpenHAB 4.x
- Modbus Binding
- Shelly devices
- Solis Hybrid Inverter
- Viessmann/Gree air conditioners

Some configurations may require adaptation to match your own:

- Thing UIDs
- Item names
- Network configuration
- Hardware devices
- Local requirements

---

# Contributions, Feedback & Credits

Suggestions, improvements and corrections are always welcome.

If you notice:

- bugs or mistakes;
- inaccurate information;
- missing attributions or credits;
- code that should not be published;
- licensing issues;
- or anything else that deserves attention,

please feel free to open an issue or contact me.

The purpose of this repository is to share knowledge while respecting the work of everyone who has contributed to the OpenHAB ecosystem.

If I have unintentionally omitted a credit or included something that should not be here, please let me know and I will be happy to correct it.

---

# Purpose

This repository serves as:

- A backup of my OpenHAB configuration
- A collection of reusable automation examples
- Documentation of custom integrations
- A source of ideas for other OpenHAB users

---

# License

This repository is released under the following custom license:

```
Copyright (c) 2026

Permission is granted to use, copy, modify and redistribute the contents of this repository for personal, educational and non-commercial purposes.

Commercial use, redistribution as part of a commercial product or service, or resale of this work requires prior written permission from the author.

This software is provided "AS IS", without warranty of any kind, express or implied.
The author shall not be held responsible for any damages or issues arising from its use.
```

By using any content from this repository, you agree to respect the terms above.

---

If you find this repository useful, feel free to leave a ⭐.

Sharing knowledge is the best way to improve the OpenHAB community.
