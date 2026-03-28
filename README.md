# RollPDF

## Overview
RollPDF is a single-file horizontal PDF viewer with smooth drag-inertia scrolling, designed for reading manga, comics, and multi-page documents.

## Quick Start
https://covao.github.io/RollPDF/RollPDF.html

## Features
- **Drag & drop** — open a PDF by dropping it onto the page or via the Open button
- **Horizontal scroll** — all pages laid out side by side with no gaps; scroll continuously left or right
- **Left / Right binding** — toggle L-bind / R-bind; auto-detected from PDF ViewerPreferences
- **Smooth inertia** — short drag releases with friction decay; long drag (1s+) releases into constant-speed continuous scroll
- **Fit Height** — one-click scale to fill the viewer height; applied automatically on load
- **CSS zoom** — zoom in/out instantly via Ctrl+Wheel or toolbar buttons without re-rendering pages
- **Fullscreen mode** — press F or the fullscreen button; toolbar slides in on mouse hover at top edge
- **Auto-hide overlays** — page numbers and scroll indicator fade out 3 seconds after the last interaction
- **URL parameters** — open a specific PDF, page, binding, and autoscroll state via query string

## Requirements
- A modern web browser (Chrome, Edge, Firefox, Safari)
- No server or installation required — runs entirely as a static HTML file

## Usage
**Open a file**
Drop a PDF onto the viewer or click **Open**.

**Navigate**
Drag horizontally to scroll. Use the mouse wheel (or trackpad) for horizontal scroll. Arrow keys move one step at a time.

**Continuous scroll**
Drag for 1 second or more, then release — the viewer keeps scrolling at the average drag speed. Click or press Escape to stop.

**Zoom**
Use **Ctrl + Wheel** to zoom in/out, or the `+` / `−` toolbar buttons. Click **FIT** to fit the page height to the window.

**Binding direction**
Click **L-bind / R-bind** to toggle page order. Right-to-left PDFs (manga) are detected automatically.

**Fullscreen**
Press **F** or click the fullscreen button. Move the mouse to the top of the screen to reveal the toolbar.

**URL parameters**

| Parameter | Values | Description |
|---|---|---|
| `pdf` | URL | Remote PDF to load on startup |
| `page` | number | Page to scroll to on open |
| `binding` | `R` / `L` | Override binding direction |
| `autoscroll` | `on` / `off` | Start continuous scroll automatically |

Example:
```
RollPDF.html?pdf=https://example.com/book.pdf&page=3&binding=R&autoscroll=on
```
