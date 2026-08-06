# Interactive Art Project

## Eavesdrop Bunny

An interactive Arduino-based robotic bunny that responds to movement, sound, temperature, and touch through sensors, servo motors, NeoPixel LEDs, and audio feedback.

---

## Overview

Eavesdrop Bunny is an interactive mixed-media embedded systems project that combines electronics, programming, and mechanical design to create an expressive desktop companion.

The bunny continuously monitors its environment using multiple sensors and reacts in different ways depending on user interaction:

- Raises its ears when someone approaches
- Changes LED lighting based on ambient sound levels
- Displays "emotional warmth" using temperature-responsive necklace lighting
- Encourages or discourages petting using capacitive touch sensors and sound effects

Although originally created for an interactive art course, the project demonstrates integration of multiple sensors, actuators, LED control, and embedded programming on an Arduino platform.

---

## Features

- **Distance Detection**
  - HC-SR04 ultrasonic sensor detects nearby movement.
  - Two servo motors lift the bunny's ears when someone approaches.

- **Sound Visualization**
  - MAX4466 microphone measures ambient sound levels.
  - NeoPixel strip dynamically changes its illumination based on microphone input.
  - LEDs progressively illuminate as sound intensity increases.

- **Temperature Visualization**
  - Temperature sensor placed inside an interactive egg.
  - A NeoPixel necklace smoothly transitions:
    - Yellow → Orange → Red
  - Represents increasing warmth during conversation.

- **Capacitive Touch Interaction**
  - Conductive fabric hidden beneath the bunny's head and paws creates touch-sensitive zones.
  - Petting the head plays a melody.
  - Touching the feet plays a low-frequency warning buzz.

---

## Hardware

### Microcontroller

- Arduino Uno R3
- Arduino Proto Shield

### Sensors

- HC-SR04 Ultrasonic Distance Sensor
- MAX4466 Electret Microphone Amplifier
- Temperature Sensor
- Capacitive Touch Sensors (conductive fabric)

### Outputs

- 2× Servo Motors
- WS2812 NeoPixel LED Strip
- Single WS2812 NeoPixel LED (necklace)
- Speaker + Amplifier

### Power

- 5V 4A External Power Supply
- 100 μF Capacitor

### Construction Materials

- Plush bunny
- Wooden base and supports
- Drawer handle (thread guide)
- Thread-based ear lifting mechanism
- Plastic Easter eggs
- Felt
- Craft wood
- Various adhesives and soldering materials

---

## Software

- Arduino IDE
- C++
- FastLED library
- tone() library for sound generation

---

## Mechanical Design

A custom lifting mechanism was designed using two servo motors and a thread-and-pulley style system.

Each ear is attached to thread routed over a metal support bar before connecting to a servo horn. When the servos rotate downward, the thread is pulled, lifting the bunny's ears in a smooth and repeatable motion.

---

## Electronics

The project integrates several independent embedded subsystems:

- Distance sensing
- Audio level detection
- Temperature sensing
- Capacitive touch sensing
- Servo motor control
- Individually addressable RGB LEDs
- Audio playback

Power for the servos, LEDs, and ultrasonic sensor is supplied from an external 5V power supply, while sensor data is processed by the Arduino Uno. A shared ground rail and decoupling capacitor were used to improve system stability.

---

