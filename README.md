# MacThrottle

A macOS menu bar app that monitors thermal pressure and alerts you when your Mac is being throttled.

## Features

- Displays thermal pressure state in the menu bar using different thermometer icons
- Notifies you when thermal throttling begins
- Lightweight background monitoring via a launch daemon

## Thermal States

| Icon | State | Description |
|------|-------|-------------|
| `thermometer.low` | Nominal | Normal operation |
| `thermometer.medium` | Moderate | Elevated thermal pressure |
| `thermometer.high` | Heavy | Active throttling |
| `thermometer.sun.fill` | Trapping/Sleeping | Severe throttling |

## Installation

1. Build and run the app in Xcode
2. Click "Install Helper..." in the menu bar dropdown
3. Enter your admin password to install the monitoring daemon

The helper runs `powermetrics` to read thermal data and writes the current state to `/tmp/mac-throttle-thermal-state`.

## Requirements

- macOS 14.0+
- Admin privileges (for helper installation)

## Uninstalling

Click "Uninstall Helper..." in the menu to remove the launch daemon and helper script.
