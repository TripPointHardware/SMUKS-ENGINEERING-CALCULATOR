# EE Calc

An offline Android scientific calculator for electrical engineers: units carried through every calculation, complex numbers and phasors, dB, a formula library that solves, plots, and checked symbolic calculus.

Part of Trip Point Software · by Trip Point Hardware

Android 8.0 or newer · Free · No internet access

## Why

I kept forgetting and losing my scientific TI calculator, and got so fed up that I chose to make one I will never forget about; because it's on my phone.

## Features

### The calculator
- **Units carried through every calculation**, with cancellation and dimension checks. `5 V / 2.2 kΩ` = `2.27273 mA`; `1 m + 1 s` is an error that says why.
- **Engineering notation** by default — results pick the right prefix (`0.00047 F` → `470 µF`) — plus scientific and plain, with adjustable precision (3–12 significant figures) or decimal places.
- **Correct or error, never quietly wrong**: `sin(π)` shows `0`, `-2^2` is `-4`, and every ambiguous input raises an error with a hint (`1/2π` → "add parentheses: 1/(2π) or (1/2)π").
- **34-digit exact decimals** in the core, so `0.1 + 0.2` = `0.3` — no floating-point drift.
- Temperature done right: absolute vs difference (`30 °C − 20 °C` = `10 K`), and below 0 K is an error.
- `ans` keeps the previous result at full precision, with its units, even after a restart.

### Complex numbers, phasors & dB
- `j` for the imaginary unit; rectangular, polar and exponential forms, converted with `→` like units: `(50 + j30) Ω → polar`.
- Polar input with `∠`: `10∠30°`. Phasor functions `abs`, `arg`, `re`, `im`, `conj`, `polar()`, `rect()`.
- **dB done properly**: `dBm`, `dBW`, `dBV`, `dBµV`. `10 dBm + 3 dB` = `13 dBm`, while `dBm + dBm` errors and points you to `psum()`.
- `∥` for parallel combination (`4.7 kΩ ∥ 10 kΩ` = `3.19728 kΩ`), and EE constants ready to type: `e`, `π`, `q_e`, `c`, `h_P`, `k_B`, `N_A`, `ε0`, `µ0`, `k_e`, `F_c`.

### Formula library
- ~40 built-in formulas across electrostatics, DC circuits, magnetism, transients, AC and signals, each with its equation in 2D math and example values.
- **Leave one variable blank and it solves for it** — numeric root-finding on the unit engine, no CAS needed. Each variable keeps its units, and a wrong dimension is caught before solving.
- **Your own formulas**: type an equation, the variables are detected with their units, and the units must balance before it saves. They solve like the built-ins, can be starred for the widget, and are stored locally.
- **E-series lookup**: `nearest(E24, 3.19728 kΩ)` → `3.3 kΩ (+3.21 %)`.

### Plots
- **Function plots** `y = f(x)` with units on the axes, up to four traces, pinch-zoom and pan, and a crosshair readout evaluated exactly.
- **Bode plots** from a transfer function `H(s)` — magnitude and unwrapped phase, with **gain and phase margins** found and marked on the charts.
- **FFT** of pasted or CSV data, with window, dB and log-frequency options, and the peak frequency refined between bins.

### Numeric tools
- **Linear systems**: `solve(A, b)` and `det(A)` for up to 10 unknowns, with unit-aware entries — mesh analysis (Ω, V) gives currents, nodal (S, A) gives voltages.
- **Polynomial roots** with exact multiplicity: `roots(1, 6, 15, 20, 12)` gives −2 (double) and −1 ± j1.41421 — never −2 ± j10⁻¹⁷.
- **Special functions**: `erf`, `erfc`, `qfunc` and both branches of `lambertw`, accurate to 34 digits.

### Symbolic calculus — and every answer is checked
- Derivatives, integrals, ODEs, Laplace and inverse Laplace transforms, Fourier and inverse Fourier transforms, Fourier series, and the matrix exponential `e^(At)`.
- **Every symbolic answer is verified numerically before it's shown** — a wrong or questionable result becomes an error, never an answer. A Simplify button and Evaluate-at-a-point round it out.
- Runs offline, off the main thread, with a timeout and cancel — no expression can freeze the screen.

### Backup & history
- **Export / Import** your formulas, favorites and history as one text file. Import merges, so importing the same file twice adds nothing.
- **Automatic backup**: once a day, saved to a folder you pick; the newest 14 are kept.
- History keeps your last 500 calculations; tap one to edit it again.

### Also
- Home screen widget with your favorite formulas, one tap to open.
- Warm monochrome theme with a magenta accent (plus cyan, yellow and green), light and dark mode.

## Install

1. Download the APK on your phone and tap it.
2. Allow **Install unknown apps** for your browser or file manager when asked. If Play Protect warns about an unknown developer, choose **Install anyway**.
3. Open EE Calc and start typing. Set your angle mode, precision, notation and accent in Settings, or **Restore a backup**.

## Your data

- Everything stays on your phone. The app has no internet permission, no account, no ads and no analytics.
- **Export / Import** in Settings: one text file with your formulas, favorites and history. Import merges, so importing the same file twice adds nothing.
- Automatic backup can save a daily copy to a folder of your choice, which survives uninstalling.

## Permissions

None. EE Calc requests no Android permissions. Backup and restore use the system file picker, so the app never asks to see your files, and it never touches the network.

## Requirements

- Android 8.0 or newer. Tested on a Samsung Galaxy A55 (One UI 8, Android 16).

## Version history

| Version | Changes |
|---|---|
| 1.0.0 | First release |

## Credits
**Symja (Java Symbolic Math Library)** — symbolic calculus and algebra powered by [Symja](https://github.com/axkr/symja_android_library), developed by Axel Kramer.
Licensed under the GNU Lesser General Public License v3.0 (LGPL-3.0).
Source code available at: https://github.com/axkr/symja_android_library

## License

Source code is private; this repository hosts the releases. Well, I don't mind sharing the source code, but if you are like me, I just download scripts and programs I see on GitHub. I could give a rat's ass how it works.
