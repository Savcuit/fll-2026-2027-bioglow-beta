# FLL 2026–2027 BIOGLOW — BETA

Working copy of the robot code for the FLL **BIOGLOW** season (LEGO SPIKE Prime / Pybricks).
The tested release lives in [`fll-2026-2027-bioglow`](https://github.com/Savcuit/fll-2026-2027-bioglow).

## What differs from v2.0

| Area | v2.0 | Beta |
|---|---|---|
| Speed variable | implicit per move | `speed = 900` module-level default |
| `reset()` | waits for IMU ready, re-enables gyro | straight reset, no IMU wait |
| `calibrate()` | IMU reset + drive reset | spins both wheels briefly, then resets |
| Pivot ratio | computed from axle track and wheel size | fixed `1.92` |
| Program list | 4 programs | same 4 programs |

## Hardware

| Port | Device |
|---|---|
| B | Left drive motor (counter-clockwise) |
| D | Right drive motor (clockwise) |
| A | Attachment motor (clockwise) |
| F | Attachment motor (clockwise) |

Drive base 62.4 mm wheels, 120 mm axle track, `PrimeHub(top_side=Axis.Z, front_side=Axis.X)`.

## Running

Start → hub red → reset → wait 1 s → green. Display shows the program number:
**LEFT/RIGHT** cycle, **CENTER** runs. Any button press during a run aborts via `check()`.

## Status

Beta — expect movement tuning and program edits between runs. Nothing here is
competition-final; promote to the release repository only after testing on the field.
