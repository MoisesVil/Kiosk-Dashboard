# Kiosk-Dashboard

## Overview

This project transforms a low-spec laptop (HP Stream 11) into a **dual-purpose Linux machine**:

1. A **power-user workstation** optimized for speed, keyboard-driven workflows, and low resource usage.
2. A **fullscreen kiosk dashboard** built with React that displays modular, draggable, and resizable widgets.

The system is designed to boot quickly, consume minimal resources, and launch directly into a customizable dashboard while still allowing full power-user access when needed.

---

## Motivation

Low-end hardware often feels slow due to heavyweight operating systems and background services. This project explores how:

* Minimal Linux setups improve performance
* Keyboard-first workflows increase productivity
* Web technologies (React) can be used to build system-level dashboards

The goal is to create a **responsive, appliance-like system** that feels intentional rather than limited by hardware.

---

## Key Features

### Power-User Environment

* Lightweight Linux distribution (Lubuntu)
* Minimal window manager (i3 or Openbox)
* Keyboard-driven navigation
* Fast boot and low memory usage

### Kiosk Dashboard

* React-based frontend
* Fullscreen Chromium kiosk mode
* Modular widget system
* Draggable and resizable widgets
* Persistent layouts across reboots

### System Integration

* Local Node.js backend
* Linux system data exposed via REST APIs
* Automatic startup using systemd or autostart scripts

---

## Planned Widgets

* Clock / Date
* CPU & Memory Monitor
* Disk Usage
* Notes / Todo List
* Media or Spotify controller (optional)

Widgets are independent React components and can be enabled, disabled, moved, or resized dynamically.

---

## Tech Stack

### Frontend

* React
* Gridstack.js (widget layout and resizing)
* CSS or Tailwind CSS

### Backend

* Node.js
* Express.js
* Linux system utilities (e.g., `free`, `uptime`, `df`)

### Storage

* LocalStorage (initial)
* SQLite (planned upgrade)

### System

* Lubuntu Linux
* Chromium (kiosk mode)
* systemd / autostart scripts

---

## Architecture Overview

```
[ React Dashboard ]
        |
        | HTTP / JSON
        v
[ Node.js Backend ]
        |
        | Linux Commands
        v
[ Operating System ]
```

The frontend never accesses system data directly. All system information is fetched through the backend for security and separation of concerns.

---

## Project Phases

### Phase 1 — Power-User Setup

* Install Lubuntu
* Configure lightweight window manager
* Set up keyboard shortcuts

### Phase 2 — Dashboard Prototype

* Create React app
* Add widget layout system
* Implement basic widgets

### Phase 3 — Persistence & Automation

* Save widget layouts
* Autostart backend and dashboard
* Enable kiosk mode

### Phase 4 — Enhancements

* Real-time updates
* Additional widgets
* Admin / edit mode

---

## Performance Goals

* Idle memory usage under 1GB
* Dashboard launch time under 3 seconds
* Responsive UI on low-end hardware

---

## Future Ideas

* Multiple dashboard profiles
* Touchscreen support
* Plugin-based widget loading
* Remote dashboard access

---

## Resume Description

Built a Linux-based power-user workstation and kiosk dashboard using React and Node.js, featuring a modular, draggable widget system, lightweight OS configuration, and automated startup optimized for low-resource hardware.

---

## Status

🚧 In Progress — Phase 1 (Power-User Setup)
