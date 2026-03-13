# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file HTML application called "随机点名转盘" (Random Name Drawing Wheel). It's an educational tool that creates an interactive spinning wheel to randomly select names from a list of students.

The application is entirely contained in a single HTML file with embedded CSS and JavaScript, making it portable and easy to run without any build process or dependencies.

## Architecture & Structure

The application follows a classic single-page application (SPA) pattern:

- **HTML Structure**: Contains the UI elements including the control panel (student count input), wheel container with pointer indicator, spin button, and result display
- **CSS Styling**: Responsive styling with flexbox layout, wheel segmentation styles, animations, and responsive design
- **JavaScript Logic**: Handles the core functionality:
  - Dynamic generation of wheel segments based on student count
  - Mathematical calculations for positioning segments and text
  - Spin animation using CSS transitions with cubic-bezier timing
  - Random selection algorithm with rotation calculation

## Core Features

- **Dynamic Wheel Generation**: Creates wheel segments dynamically based on specified student count (3-60)
- **Visual Design**: Colorful segments with radial text positioning for optimal readability
- **Smooth Animation**: 4-second spin animation with custom easing function
- **Interactive Controls**: Input for student count with update functionality
- **Result Display**: Shows the selected name after spinning completes

## Technical Details

- The wheel segments are created using CSS clip-path polygons calculated with trigonometric functions
- Text is positioned radially and rotated to ensure readability
- The spin animation calculates precise rotation angles to ensure the selected segment stops at the pointer
- Includes protection against text appearing upside-down by adjusting rotation in lower quadrants

## Development Commands

To run this application:

```bash
# Simply open the index.html file in any modern browser
open index.html
# or
python -m http.server 8000  # if you prefer serving via HTTP
```

There are no build steps or dependencies required for this project.