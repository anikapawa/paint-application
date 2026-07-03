# OCaml Paint Application

A fully interactive paint application built in OCaml using a custom GUI toolkit. This project demonstrates functional programming applied to graphics, event-driven UI design, and modular widget-based architecture.

---

## Overview

This application is a lightweight drawing tool that allows users to create and manipulate shapes on a canvas. It is built using OCaml’s Graphics library along with a custom widget system that supports composable user interface components and event handling.

The project focuses on implementing a complete GUI stack from low-level drawing primitives to a structured interactive application.

---

## Features

### Drawing Tools
- Line drawing using click-and-drag interaction
- Free-form point drawing via mouse dragging
- Ellipse drawing using bounding-box drag gestures
- Live preview of shapes while drawing before finalizing

---

### User Interface
- Mode switching between line, point, and ellipse tools
- Color selection toolbar
- Undo functionality for removing the most recent shape
- Clean layout using custom horizontal and vertical widget composition

---

### Line Thickness Control
- Slider-based control for adjusting line thickness
- Applies thickness only to newly created shapes
- Preserves consistency of previously drawn shapes
- Integrated into the widget system as a reusable UI component

---

## Architecture

The application is structured into three main layers:

### Graphics Context Layer (Gctx)
- Abstraction over OCaml’s Graphics module
- Handles coordinate transformations and drawing operations
- Provides primitives for lines, points, and ellipses

### Widget System
- Custom GUI framework built from scratch
- Supports composable layout primitives such as horizontal and vertical stacking
- Event handling for mouse and interaction events
- Reusable UI components including buttons, sliders, and checkboxes

### Application Layer (paint.ml)
- Maintains global application state (mode, color, shapes, preview state)
- Translates user input into drawing operations
- Manages shape history for undo functionality
- Controls rendering pipeline

---

## Key Concepts

- Functional programming applied to GUI development
- Event-driven architecture (mouse down, drag, release)
- Mutable application state with persistent shape history
- Custom widget composition system
- Coordinate system conversion between logical and screen space
- Efficient undo implementation using a deque structure

---

## How It Works

1. The user selects a drawing mode (line, point, or ellipse)
2. Mouse events drive interaction:
   - MouseDown starts a shape
   - MouseDrag updates a live preview
   - MouseUp finalizes and stores the shape
3. Shapes are stored in a history structure (deque)
4. The canvas is re-rendered by iterating over stored shapes in order

---

## Custom Enhancements

This implementation extends the base paint system with:

- Slider-based line thickness control
- Improved UI layout system using reusable composition functions
- Real-time preview rendering for shapes
- Extended widget system for reusable UI components

---

## Technologies Used

- OCaml
- OCaml Graphics library
- Custom widget and GUI system
- Functional programming architecture
- Event-driven design

---

## Running the Project

In a local or Codio environment:

```bash
make build
make paint
```

Then open the paint application in the provided GUI window.

---

## Author
Anika Pawa
GitHub: https://github.com/anikapawa
