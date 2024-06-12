# Project Inverse Kinematics with Deep Neural Networks for IRB 120 robot of ABB

### Introduction
This repository hosts a project focused on implementing inverse kinematics for an ABB IRB 120 robot. Inverse kinematics is a fundamental concept in robotics that involves determining the joint parameters of a robot to achieve a desired end-effector position. The project aims to develop a neural network capable of predicting the robot's joint configurations based on given x, y, z coordinates in its workspace.

### Files Overview
1. **Dataset.ipynb**: This Jupyter notebook is dedicated to generating a dataset necessary for training and testing the neural network. It leverages rotation matrices and the Robotic Toolbox, a collection of robotics algorithms in MATLAB, to create simulated data representing various robot configurations.

2. **analysis.ipynb**: This notebook performs a detailed analysis of the generated dataset. Exploratory data analysis techniques are employed to gain insights into the distribution and characteristics of the data, which helps in understanding potential challenges and formulating appropriate strategies for training the neural network.

3. **ik_dnn.ipynb**: In this notebook, the neural network is constructed using TensorFlow's Sequential model, a popular framework for building deep learning models. Deep neural networks (DNNs) are a class of artificial neural networks characterized by multiple layers of interconnected neurons, allowing them to learn complex patterns and representations from data. The Sequential model facilitates the sequential stacking of layers, enabling the creation of sophisticated architectures.

   - The notebook explores various neural network architectures by experimenting with different configurations of layers, activation functions, and regularization techniques. TensorFlow's extensive library of pre-built layers and functions is utilized to construct the model efficiently.
   
   - Multiple loss functions and optimizers are evaluated to find the most suitable combination for minimizing prediction errors and improving model performance. TensorFlow's flexible API allows for easy experimentation and fine-tuning of model parameters.
   
   - Several trained models are saved along with associated metadata, including training history and evaluation metrics. Additionally, CSV files containing preprocessed data used for training are included for reproducibility and transparency.

### Conclusion
Despite diligent efforts, an optimal model capable of accurately predicting the robot's joint configurations from given coordinates could not be attained, as indicated by a suboptimal performance score of under 30%. Further investigation revealed relevant literature discussing similar challenges in robotics and deep learning.

In particular, it was noted that custom loss functions tailored to the specific task of predicting transformation matrices from x, y, z coordinates have shown promise in improving model performance. Future iterations of the project may benefit from incorporating such techniques and exploring novel approaches inspired by recent advancements in the field.

