# Fusuma Configuration README

## Overview

This README explains the configuration file for Fusuma, a multitouch gesture recognizer for Linux. The configuration defines various gestures and their associated actions for controlling system functions like brightness, media playback, volume, and window management.

## Gesture Types

The configuration supports two main types of gestures:

1. Rotate
2. Swipe

### Rotate Gestures

#### 3-Finger Rotate

- **Clockwise**: Increases screen brightness
  - Default: Increases by 500 units
  - With CTRL (left or right): Increases by 250 units
  - With LEFT SHIFT: Increases by 2500 units

- **Counterclockwise**: Decreases screen brightness
  - Default: Decreases by 500 units
  - With CTRL (left or right): Decreases by 250 units
  - With LEFT SHIFT: Decreases by 2500 units

#### 4-Finger Rotate

- Both **clockwise** and **counterclockwise**: Toggles media play/pause

### Swipe Gestures

#### 3-Finger Swipe

- **Left**: Activates alt-tab (window switching)
  - Subsequent left swipes: Move to the next window
  - Subsequent right swipes: Move to the previous window
  - Up/Down swipes: Navigate through windows

- **Right**: Performs alt-tab and releases alt key

- **End of swipe**: Releases the alt key

#### 4-Finger Swipe

- **Down**: Decreases volume
  - With LEFT SHIFT: Faster decrease
  - With LEFT CTRL: Slower decrease

- **Up**: Increases volume
  - With LEFT SHIFT: Faster increase
  - With LEFT CTRL: Slower increase

- **Right**: Toggles mute

- **Left**: Toggles microphone mute

## Dependencies

This configuration relies on the following:

- KDE Plasma desktop environment
- `qdbus` for interacting with KDE's D-Bus interface
- [ydotool](https://github.com/ReimuNotMoe/ydotool): ydotool should be installed and running, to emulate keypresses

## Notes

- The configuration uses KDE's power management and global shortcuts for brightness and volume control.
- Window switching functionality creates a temporary file to track state.
- Adjust the paths and commands if your system setup differs.

## Customization

You can modify the gesture actions, key combinations, and command intervals to suit your preferences. Be cautious when changing system commands to ensure they're compatible with your setup.
