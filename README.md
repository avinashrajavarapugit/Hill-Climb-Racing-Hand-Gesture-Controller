# Hill Climb Racing Hand Gesture Controller 🎮🖐️

A computer vision-based controller for the popular Hill Climb Racing game, allowing players to use hand gestures for real-time controls, such as accelerating and braking, instead of traditional keyboard input.

## Overview
This project uses OpenCV and MediaPipe to detect hand gestures and track fingertip movements to control in-game actions. By recognizing whether the hand is on the left or right side of the screen, the program simulates gas and brake controls to create an interactive, gesture-driven gaming experience.

## Demo
![Demo Video](DemoLink)

## Features
- **Gesture Recognition**: Achieves 90% accuracy in detecting hand gestures.
- **Real-Time Performance**: Processes video at 20 FPS for smooth gameplay.
- **Controls**:
  - **Gas**: Move the hand to the right side of the screen.
  - **Brake**: Move the hand to the left side of the screen.
  
## Technologies Used
- **Python**: Main programming language.
- **OpenCV**: For real-time video processing and image manipulation.
- **MediaPipe**: For accurate hand landmark detection.
- **pyautogui**: To simulate keyboard actions based on hand position.

## Setup and Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/YourUsername/HillClimbRacing-HandGestureController.git
    cd HillClimbRacing-HandGestureController
    ```

2. **Install Required Libraries**:
    ```bash
    pip install opencv-python mediapipe pyautogui
    ```

3. **Run the Program**:
    ```bash
    python hill_climb_controller.py
    ```

## How It Works
1. The program captures video input from the webcam and flips it horizontally for a mirror view.
2. MediaPipe’s hand detection model identifies hand landmarks and tracks the fingertip.
3. Based on the fingertip’s x-coordinate:
   - **Gas**: Right half of the screen.
   - **Brake**: Left half of the screen.
4. `pyautogui` simulates pressing the right and left arrow keys accordingly.

## Customization
- Adjust the sensitivity or change hand gestures by modifying conditions for the x-coordinate in the code.

## Requirements
- Python 3.x
- Webcam

