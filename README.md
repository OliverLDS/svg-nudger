# SVG Nudger v3

A very small browser-only SVG editing helper for human alignment work.

It is designed for this workflow:

```text
Codex generates SVG -> open in SVG Nudger -> manually align/resize -> copy or download final SVG
```

## Features

- Load any local `.svg` file in the browser
- Click to select one SVG object
- Shift-click to select multiple objects
- Drag selected objects together
- Resize one or many selected objects using the bounding-box handles
- Hold Shift while dragging a corner handle to keep proportions
- Move selected objects with arrow keys
- Grid snapping: off, 1px, 5px, 10px, 20px
- Undo / redo
- View selected tag, id, class, and transform
- Auto-locate the selected single object in **Current SVG code**
- Edit the SVG source directly in **Current SVG code** and apply it with blur or `Ctrl`/`Cmd` + `Enter`
- Modify selected SVG text object font family and font size
- Copy edited SVG code
- Download edited SVG

## How to use

1. Open `index.html` in Chrome, Edge, or another modern browser.
2. Click **Choose File** and load your SVG.
3. Click an object to select it.
4. Shift-click more objects if needed.
5. Drag selected objects to move them together.
6. Drag the red handles around the selection box to resize.
7. If you select a single object, **Current SVG code** automatically scrolls to that element.
8. Edit the SVG source directly in **Current SVG code**, then blur the field or press `Ctrl`/`Cmd` + `Enter` to apply it.
9. If you select a `<text>` or `<tspan>` element, edit its font family or font size from **Text style**.
10. Click **Copy SVG Code** or **Download Edited SVG**.

## Notes

- This is intentionally not a full SVG editor.
- It edits placement and size mainly through `transform="matrix(...)"`.
- Text style changes are written as `font-family` and `font-size` attributes.
- The SVG code box is editable and replaces the current SVG when applied.
- The red selection box and handles are temporary UI only. They are removed from copied/downloaded SVG output.
- For best results, select the visible object or group that you want to align, not hidden elements inside `defs`.
