# Bluetooth-Controlled Floor Cleaning Robot

This repository contains the code and documentation for a Bluetooth-controlled floor cleaning robot. The robot is designed to move and clean floors using various cleaning tools attached to a Bluetooth-controlled car. The cleaning system is built around an Arduino UNO, and its movement is controlled via a mobile device using Bluetooth communication.

## Features

- **Remote Control**: Operates using Bluetooth, allowing control via a mobile device.
- **Cleaning Mechanism**: Equipped with cleaning tools like sponges, brushes, and detergents that move with the robot to clean the floor.
- **Motor Control**: Supports movement in multiple directions (forward, backward, left, right) and can stop based on commands.
- **Speed Control**: Adjustable speed through commands ranging from slow to fast.
- **Electronic Braking System**: Equipped with an optional electronic braking system for more precise stopping.
- **Light Control**: LED indicator for operation status.

## Components

- **Arduino UNO**: The central control unit for the robot.
- **Motors & Motor Drivers (L298N)**: Responsible for the movement of the robot.
- **Bluetooth Module**: Facilitates wireless communication between the robot and the mobile device.
- **Cleaning Materials**: Sponges, brushes, and detergents are mounted on the car for cleaning operations.

## How It Works

- The robot receives movement commands via Bluetooth (e.g., move forward, backward, left, right).
- Cleaning tools attached to the robot move along with the car, cleaning the floor as it navigates.
- Speed adjustments and turning radius can be controlled remotely using specific commands.
- An electronic braking system can be enabled or disabled for stopping the robot precisely.

## Control Commands

- `'F'`: Move Forward
- `'B'`: Move Backward
- `'L'`: Turn Left
- `'R'`: Turn Right
- `'G'`: Forward-Left Diagonal
- `'I'`: Forward-Right Diagonal
- `'H'`: Backward-Left Diagonal
- `'J'`: Backward-Right Diagonal
- `'0'` to `'9'`, `'q'`: Speed control (from slow to fast)
- `'S'`: Activate the electronic braking system

## Code Overview

The code defines the control logic for the robot, with the following key sections:

- **Setup**: Initializes the motor control pins, LED, and Bluetooth communication.
- **Loop**: Continuously checks for incoming Bluetooth commands and adjusts the robot's movement or speed based on the input.
- **Motor Control Functions**: Functions like `forward()`, `back()`, `left()`, and `right()` to handle directional movement.
- **Brake System**: An optional electronic braking system activated by the `'S'` command for precision stopping.

## Requirements

- Arduino IDE
- Arduino UNO
- L298N Motor Driver
- DC Motors
- Bluetooth Module (e.g., HC-05)
- Cleaning Materials (sponges, brushes, etc.)

## Usage

1. Upload the Arduino code from this repository to your Arduino UNO.
2. Connect your Bluetooth module to the Arduino and pair it with a mobile device.
3. Use a Bluetooth terminal app to send commands (e.g., `'F'` for forward) to control the robot.
4. Attach cleaning tools to the robot, and it will clean the floor as it moves.
