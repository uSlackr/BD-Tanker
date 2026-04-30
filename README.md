BD-Tanker
=========
ESPHome-based fermentation temperature monitoring/control for a brewery. This repository houses the BD-Tanker configuration files that were moved from the esphome-lxc workspace for clarity and versioning.

Files included (in this repo):
- brew-control.yaml
- bd-remote-a.yaml
- bd-remote-b.yaml
- bd-remote-c.yaml
- bd-probe-base.yaml

Directory layout:
- BD-Tanker/
  - brew-control.yaml
  - bd-remote-a.yaml
  - bd-remote-b.yaml
  - bd-remote-c.yaml
  - bd-probe-base.yaml
- README.md (this file)
- .gitignore (to ignore secrets)

What this is:
- A distributed ESPHome setup for a brewery fermentation controller (the TD-Controller) with three remote probe boards providing up to 20 temperature probes, and a central brew-control unit with a local enclosure temp sensor, display, inputs, and valve controls.
- The remotes publish sensor data over encrypted UDP; the brew-control consolidates data and provides control logic for fermentation equipment.

Secrets handling:
- Secrets (encryption keys, OTA passwords, etc.) are not tracked in this repo. They should be supplied via ESPHome secrets or a separate secure secrets store. See instructions below for configuring secrets locally.

Usage notes:
- This repo is intended for collaboration and audit purposes. Do not expose secrets or keys publicly.
