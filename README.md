
# Micrograd

## Introduction
Micrograd is a minimalistic automatic differentiation and neural network library implemented in Python. It's designed for educational purposes, providing a simple yet powerful tool to understand the fundamentals of neural network operations, automatic differentiation, and gradient-based optimization.

## Features
- Scalar-based automatic differentiation.
- Basic operations (addition, multiplication, power, etc.).
- Implementation of a simple neural network with customizable layers.
- Tanh activation function.
- Backward propagation for gradient calculation.

## Installation
To use Micrograd, simply clone this repository to your local machine using:


## Usage
Here's a quick example of how to use Micrograd:

```python
# Import the library
from micrograd import Value

# Create Value objects
a = Value(2.0)
b = Value(3.0)

# Perform operations
c = a * b + b

# Compute gradients
c.backward()

# Print gradients
print(a.grad)  # Output: Gradient of a with respect to c
print(b.grad)  # Output: Gradient of b with respect to c

from micrograd.nn import MLP

# Create a multilayer perceptron
model = MLP(nin=3, nouts=[4, 4, 1])

# Forward pass
x = [2.0, 3.0, -1.0]
output = model(x)

# Compute loss (assuming you have a loss function defined)
loss = loss_function(output, target)

# Backward pass
loss.backward()
