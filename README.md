# Greenhouse Rover Simulation

A ROS-based autonomous mobile robot simulation in a Gazebo greenhouse environment. Implements three operation modes: manual teleoperation, visual target tracking, and coordinate-based autonomous navigation with obstacle detection.

![ROS](https://img.shields.io/badge/ROS-22314E?style=flat&logo=ros&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Gazebo](https://img.shields.io/badge/Gazebo-Simulation-orange?style=flat)

---

## Overview

Simulates an autonomous service rover navigating a greenhouse environment. The rover is built on the [uma_grover](https://github.com/carlos-silvap/uma_grover) robot model and supports multiple control modes for field robot research scenarios.

**Operation modes:**

1. **Manual**: keyboard or joystick teleoperation via `geometry_msgs/Twist`
2. **Target tracking**: visual detection and following of a target using camera input (`sensor_msgs`)
3. **Autonomous navigation**: goal-based navigation to GPS/metric coordinates with obstacle detection and avoidance

---

## Stack

- **ROS (Noetic / catkin)** — middleware, launch system, parameter server
- **Gazebo** — physics simulation and sensor emulation
- **Python** — control scripts and navigation nodes
- **Nav stack** — `geometry_msgs`, `sensor_msgs`, `std_msgs`

---

## Repository Structure

```
├── launch/      # roslaunch files to start simulation and nodes
├── models/      # Gazebo robot and environment models
├── param/       # ROS navigation parameters (costmaps, planners)
├── scripts/     # Python nodes: manual control, target tracking, autonomous nav
├── world/       # Gazebo greenhouse world file
├── CMakeLists.txt
└── package.xml
```

---

## Robot Model

The rover URDF and physical configuration are defined in the companion package [uma_grover](https://github.com/carlos-silvap/uma_grover).

---

## Context

Developed as a first-semester robotics project at [Mid Sweden University](https://www.miun.se/en) as part of the Erasmus Mundus MSc in Computer Science & Engineering.
