# Implementation of the batch Least Squares Method 
Least squares estimation aims to find the parameters of a mathematical model that minimize the sum of the squared differences between the observed data (measurements) and the model's predictions. 
# Determining Resistance of an Electrical Component using Ohm's Law

In this code, we aim to determine the resistance of an electrical component using Ohm's law, which relates voltage (V) and current (I) through the formula V = RI. We have collected data on the voltage and current values for the component and wish to fit a line through the origin to find the best estimate of the resistance (R) in ohms.

## Prerequisites
To run this code, these Python libraries must be installed:

numpy
matplotlib

## Data
We have collected the following data for the electrical component:

Current (I) values: [0.2, 0.3, 0.4, 0.5, 0.6] amperes
Voltage (V) values: [1.23, 1.38, 2.06, 2.47, 3.17] volts

## Code Description
It begins by importing the necessary libraries: numpy for numerical computations and matplotlib for plotting.

The current (I) and voltage (V) data are stored as column vectors.

We plot the current (I) against voltage (V) data points using a scatter plot to visualize the relationship.

To fit a line through the origin (y = αx), we use the Jacobian matrix (H) with only one column representing the current (I) values.

The estimation of the resistance parameter (α) is done using the least-squares method. We compute the transpose of the Jacobian matrix (H_transpose), the product of the transpose and the Jacobian (H_squared), the inverse of the product (H_inverse), and the product of the transpose and voltage (V) (H_product).

The estimated resistance (R) is then obtained by multiplying the inverse of H_squared with H_product.

We display the slope parameter of the best-fit line, which represents the estimated resistance (R) in ohms.

We plot the best-fit line along with the data points to visualize the linear relationship between voltage (V) and current (I).

## Results
The code outputs the slope parameter of the best-fit line, which represents the estimated resistance (R) in ohms. Additionally, it displays a scatter plot of the data points and the best-fit line.

## Note
This code assumes that all measurements have equal importance and fits a line through the origin (y = αx) to estimate the resistance (R) using the least-squares method.

It is important to ensure that the collected data is accurate and representative of the electrical component's behavior.

For more accurate results, additional data points and a more robust regression analysis may be required.

If the current (I) values are close to zero or too small, there might be errors in the estimation, and the data points may need to be scaled or transformed accordingly.

