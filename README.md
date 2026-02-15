# Cart-Pole Controller Shootout

## Overview
This project builds and compares three different control strategies—two-loop PD (“PID-style”), pole placement, and LQR—to balance an inverted pendulum on a moving cart using MATLAB. It starts from a nonlinear physics model of the cart-pole system (with gravity, inertia, and friction), then numerically linearizes the dynamics around the unstable upright equilibrium to obtain a state-space model used for controller design. Each controller computes a force command to keep the pendulum angle near 0° while limiting cart motion, and the force is realistically constrained with actuator saturation. The script simulates the full nonlinear closed-loop system from an initial tilt, generates plots of angle, cart position, and control effort, computes quantitative performance metrics (max angle, settling time, max cart travel, and control energy ∫ u² dt), flags failures when the pendulum falls beyond a threshold, and includes an animation to visually verify stability and compare how robust each controller is.

## What’s Included
- Nonlinear cart-pole dynamics model
- Numerical linearization around the upright equilibrium
- Controllers:
  - Two-loop PD (“PID-style”)
  - Pole placement
  - LQR
- Actuator saturation (force limiting)
- Performance metrics + comparison table
- Plots of:
  - Pendulum angle vs time
  - Cart position vs time
  - Control force vs time
- Simple cart-pole animation

## Requirements
- MATLAB
- **Control System Toolbox** (for `lqr` and `place`)
