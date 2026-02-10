# Data Generation using Modelling and Simulation for Machine Learning

## Introduction
In many machine learning applications, collecting real-world data can be costly or impractical. Simulation-based data generation provides an efficient alternative by producing synthetic data using mathematical and physical models. This project demonstrates how modelling and simulation can be used to generate data for training and evaluating machine learning models.

---

## Simulation Tool
The CartPole environment from the Gymnasium library is used as the simulation tool. CartPole is a physics-based simulator that models a pole attached to a cart moving along a frictionless track. The system dynamics are governed by classical mechanics equations.

---

## Simulation Parameters and Bounds

| Parameter | Description | Lower Bound | Upper Bound |
|----------|-------------|-------------|-------------|
| Cart Position | Horizontal position of the cart | -2.4 | 2.4 |
| Cart Velocity | Velocity of the cart | -3.0 | 3.0 |
| Pole Angle | Angle of the pole (radians) | -0.2 | 0.2 |
| Pole Angular Velocity | Angular velocity of the pole | -3.0 | 3.0 |

---

## Data Generation Methodology
1. Random initial values are generated for each simulation parameter within predefined bounds.
2. These parameters are passed to the CartPole simulator as the initial state.
3. The simulator runs for a maximum of 200 steps using random actions.
4. The total reward obtained from the simulation is recorded.
5. This process is repeated 1000 times to generate a synthetic dataset.

---

## Dataset Description
The generated dataset consists of the following attributes:

- cart_position
- cart_velocity
- pole_angle
- pole_angular_velocity
- reward

The first four attributes are input features, and the reward is the target variable.

---

## Machine Learning Models Used
The following regression models are trained and evaluated using the generated dataset:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Support Vector Regression (SVR)
- K-Nearest Neighbors (KNN) Regressor

---

## Evaluation Metrics
The models are evaluated using:
- Mean Squared Error (MSE)
- R² Score

---

## Results
A comparison table is generated to evaluate the performance of all models. A bar graph is also plotted to visualize the R² scores of the models. The Random Forest Regressor achieves the best performance among all evaluated models.

<img width="485" height="319" alt="image" src="https://github.com/user-attachments/assets/9ff11c0d-95da-475c-8f8e-7e5e05e34622" />
---

## Conclusion
This project demonstrates that simulation-based data generation can be effectively used for machine learning tasks. The results show that ensemble models such as Random Forest perform better on simulation-generated data compared to simpler models.


---

## Tools and Libraries
- Python
- Google Colab
- Gymnasium
- NumPy
- Pandas
- Scikit-learn
- Matplotlib



## Repository Structure
