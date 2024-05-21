# math-applied-in-python

# Project Description
his project demonstrates the application of mathematical functions using Python. It includes examples of linear functions with one, two, and three inputs, as well as plotting these functions using `matplotlib`.


## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Examples](#examples)
  - [1D Linear Function](#1d-linear-function)
  - [2D Linear Function](#2d-linear-function)
  - [3D Linear Function](#3d-linear-function)
  - [Exponential Function](#exponential-function)
  - [Logarithm Function](#logarithm-function)
- [License](#license)

 # Installation
  To run this project, you need to have Python installed along with the following libraries:
- `numpy`
- `matplotlib`

You can install these libraries using pip:
```bash
pip install numpy matplotlib
```
## Usage
To run the project, simply execute the Python script. The script will compute and plot various mathematical functions.

## Project Structure
```python
math-applied-in-python/
├── data/
│   └── example_data.csv                           # Example dataset file (if applicable)
├── notebooks/
    └── math_applied_in_python.ipynb               # Jupyter notebook with the code
    ├── linear_functions                           # Linear functions scripts
    ├── exponential_function                       # Exponential function script
    ├── logarithm_function                         # Logarithm function script
    └── plotting.py                                # Plotting utility scripts                       
├── README.md                                      # Project README file
└── requirements.txt                               # List of dependencies
```

## Examples

1. 1D Linear Function
This section defines a linear function with one input and plots it.
```python
def linear_function_1D(x, beta, omega):
    y = beta + omega * x
    return y

x = np.arange(0.0, 10.0, 0.01)
beta = 2.0
omega = 1.0
y = linear_function_1D(x, beta, omega)

fig, ax = plt.subplots()
ax.plot(x, y, 'r-')
ax.set_ylim([10])
ax.set_xlim([5])
ax.set_xlabel('x')
ax.set_ylabel('y')
plt.show()
```

2. 2D Linear Function
```python
def linear_function_2D(x1, x2, beta, omega1, omega2):
    y = beta * (omega1 * x1 + omega2 * x2)
    return y

x1_values = np.linspace(-10, 10, 100)
x2_values = np.linspace(-10, 10, 100)
X1, X2 = np.meshgrid(x1_values, x2_values)
Y = linear_function_2D(X1, X2, beta, omega1, omega2)

plt.figure(figsize=(10, 6))
cp = plt.contourf(X1, X2, Y, cmap='viridis')
plt.colorbar(cp)
plt.title('2D Linear Function Contour Plot')
plt.xlabel('x1')
plt.ylabel('x2')
plt.show()
```

3. 3D Linear Function
```python
def linear_function_3D(x1, x2, x3, beta, omega1, omega2, omega3):
    y = beta * (omega1 * x1 + omega2 * x2 + omega3 * x3)
    return y

x1 = 2
x2 = 3
x3 = 4
beta = 1.5
omega1 = 0.5
omega2 = 0.8
omega3 = 1.2

result = linear_function_3D(x1, x2, x3, beta, omega1, omega2, omega3)
print("The result of the linear function is:", result)
```

4. Exponential Function
This section plots the exponential function.
```python
x = np.arange(-5.0, 5.0, 0.01)
y = np.exp(x)

fig, ax = plt.subplots()
ax.plot(x, y, 'r-')
ax.set_ylim([0, 100])
ax.set_xlim([-5, 5])
ax.set_xlabel('x')
ax.set_ylabel('exp[x]')
plt.show()
```

5. Logarithm Function
This section plots the logarithm function.
```python
x = np.arange(0.01, 5.0, 0.01)
y = np.log(x)

fig, ax = plt.subplots()
ax.plot(x, y, 'r-')
ax.set_ylim([-5, 5])
ax.set_xlim([5])
ax.set_xlabel('x')
ax.set_ylabel('$\log[x]$')
plt.show()
```
## License
This README file provides a comprehensive overview of the project, including installation instructions, usage, project structure, and examples of the different mathematical functions implemented in the project.
