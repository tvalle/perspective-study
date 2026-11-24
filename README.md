# Box Rotation and Horizon Study

An interactive perspective study tool for drawing. Place boxes on a ground plane, rotate and tilt them, move the camera, and watch how the horizon line, vanishing points and vanishing lines respond.

It answers two common questions:

- What happens when boxes on the same ground line are rotated? Rotating a box around the vertical axis (yaw) only slides its two vanishing points along the horizon. Boxes with the same rotation share vanishing points, no matter where they sit.
- Which rotation creates a new horizon line? Only tilting a box (pitch or roll). Its faces become inclined planes, and each inclined plane has its own vanishing line. When the tilt is around a horizontal hinge, the hinge's vanishing point stays on the true horizon and the new line pivots around it. Tilting or rolling the camera does not create a new horizon: it moves or rotates the same eye-level horizon inside the frame.

## Running

The app is a single static file with no dependencies and no build step. Open `index.html` in a browser, or serve the folder with any static file server:

```sh
python -m http.server
```

## Features

- Horizon (eye level) line, center of vision, ground grid and sky/ground tint
- Add, duplicate, remove, line up and copy rotation between boxes
- Per-box yaw, pitch, roll, position, elevation and size
- Vanishing points colored by edge direction (x width, y height, z depth), merged when shared, with off-screen and infinite markers
- Construction lines from each edge to its vanishing point
- Vanishing lines for tilted planes, optionally for every face of the selected box
- X-ray mode for hidden edges
- Live explanation panel describing what the camera, the selected box and the scene are doing
- Top view (plan) with draggable boxes and the camera's field of view
- Ten lesson presets: same rotation on one row, different yaws on one row, 1-point vs 2-point, tilting, tumbling, ramps and roofs, looking up, looking down, floating boxes, and camera roll

## Controls

Boxes:

| Input | Action |
| --- | --- |
| Drag | Move on the ground |
| Shift + drag | Yaw |
| Ctrl or Alt + drag | Tilt (vertical drag pitches, horizontal drag rolls) |
| Q / E | Yaw |
| W / S | Pitch |
| A / D | Roll |
| N | New box |
| Delete | Remove selected box |
| Tab | Select next box |

Camera:

| Input | Action |
| --- | --- |
| Right-drag | Look around (turn and tilt) |
| Middle-drag or Shift + right-drag | Orbit the selected box |
| Alt + wheel | Orbit distance |
| Ctrl + wheel | Field of view |
| Arrow keys | Walk |
| R / F | Raise / lower eye height |
| Z / C | Roll |
| L | Level the camera |
| G | Aim at the selected box |

Hold Shift with the keyboard shortcuts for finer steps. The camera pad in the top-right corner offers the same actions plus worm's-eye, eye-level and bird's-eye viewpoints.

View:

| Input | Action |
| --- | --- |
| Wheel | Zoom the picture out to find far vanishing points |
| Drag empty space | Pan |
| Double-click | Re-center |

## License

Released into the public domain under [CC0 1.0 Universal](LICENSE).
