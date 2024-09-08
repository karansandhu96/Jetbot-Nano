# JetBot Nano: Path Following and Collision Avoidance

## Overview

JetBot Nano is a powerful AI-driven robot built on NVIDIA’s Jetson Nano platform, designed for educational purposes and robotics enthusiasts. The JetBot Nano combines the power of AI with practical robotics applications, allowing it to autonomously follow paths and avoid collisions using deep learning and computer vision techniques.

## Components

1. **Jetson Nano**: The core of JetBot, a compact, low-power computer capable of running multiple neural networks in parallel for AI tasks such as object detection, image classification, and speech processing.

2. **Camera Module**: A standard camera module provides real-time visual input, enabling the JetBot to "see" its environment. This input is crucial for path following and collision avoidance.

3. **Motor Driver and Wheels**: The motor driver controls the wheels based on the commands received from the Jetson Nano, allowing the JetBot to navigate its environment.

4. **Ultrasonic Sensors**: These sensors detect objects in the vicinity of the JetBot, providing an additional layer of safety for collision avoidance.

## Path Following

Path following is a fundamental capability of JetBot Nano. It involves the robot moving along a pre-defined path, which can be represented by a colored line or a series of waypoints.

### How It Works

1. **Visual Detection**: The JetBot's camera continuously captures images of the environment. A convolutional neural network (CNN) processes these images to detect the path.

2. **Line Detection**: The path is usually a distinct color or pattern, making it easily detectable by the vision system. The CNN identifies the line and calculates the required adjustments to keep the JetBot centered on the path.

3. **Control Algorithm**: Based on the detected line's position relative to the center of the camera's view, the control algorithm sends commands to the motor driver, adjusting the speed and direction of the wheels to follow the path accurately.

### Applications

- **Autonomous Navigation**: JetBot can navigate complex environments without human intervention, making it ideal for autonomous delivery robots or self-driving cars.
- **Education**: Provides a hands-on experience for students learning about robotics, AI, and computer vision.

## Collision Avoidance

Collision avoidance ensures that the JetBot can navigate safely by detecting and avoiding obstacles in its path.

### How It Works

1. **Obstacle Detection**: The ultrasonic sensors and the camera work together to detect obstacles. The ultrasonic sensors provide distance measurements, while the camera detects obstacles visually.

2. **Obstacle Classification**: Using deep learning, JetBot classifies objects detected by the camera to determine whether they are static or dynamic obstacles, and how they should be avoided.

3. **Real-Time Decision Making**: When an obstacle is detected, the control algorithm evaluates the situation. It can decide to stop, slow down, or steer away from the obstacle based on the distance and speed of approach.

4. **Safe Navigation**: The JetBot continuously updates its path in real-time to avoid obstacles, ensuring smooth and safe navigation.

### Applications

- **Robotics Research**: Serves as a platform for developing and testing new algorithms in robotics and AI.
- **Safety in Automation**: Demonstrates the principles of safety-critical systems used in industrial robots and autonomous vehicles.

## Implementation

To implement path following and collision avoidance on the JetBot Nano, follow these steps:

1. **Set Up Jetson Nano**: Install the Jetson Nano Developer Kit and flash the SD card with the appropriate JetPack image. Connect the camera module and motor driver.

2. **Install Required Libraries**: Install Python libraries such as OpenCV, PyTorch, and JetBot’s software stack. These libraries provide tools for image processing, machine learning, and control.

3. **Train the Model**: Use labeled datasets to train a CNN for path detection. You can use transfer learning with a pre-trained model like ResNet to speed up the process.

4. **Deploy the Model**: Once trained, deploy the model onto the JetBot. The model will process images from the camera in real-time to detect the path.

5. **Implement Control Logic**: Write control logic to interpret the output of the CNN and send appropriate commands to the motor driver for path following.

6. **Collision Avoidance Setup**: Implement obstacle detection by integrating ultrasonic sensors. Write code to process sensor data and combine it with camera input for collision avoidance.

7. **Test and Tune**: Conduct field tests, tuning the parameters to ensure smooth path following and effective collision avoidance.


https://github.com/user-attachments/assets/8b09a648-a370-4e30-8626-e854477e463f


https://github.com/user-attachments/assets/3a454da0-ea54-42a6-950f-bb2c331d1a5c


https://github.com/user-attachments/assets/1acfee96-5233-4add-a4e7-d25d15b4f27a

![Camera pohoto](https://github.com/user-attachments/assets/6e3f6366-1955-47d8-affd-2459674d93c9)


## Conclusion

The JetBot Nano is an excellent platform for learning and experimenting with AI-driven robotics. Its capabilities in path following and collision avoidance demonstrate fundamental principles that are applicable to a wide range of robotics applications, from simple educational projects to advanced research and industrial automation. By integrating deep learning with real-time control, the JetBot Nano brings cutting-edge AI to the world of autonomous robotics.
