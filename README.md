## Gradient Descent and OLS Example for Linear Regression
While taking the Machine Learning course on Coursera by Andrew Ng, I decided to try to implement some of the things I learnt inside Unity. This exmple was adapted from [The Coding Train video](https://www.youtube.com/watch?v=L-Lsfu4ab74).

The example demonstrates how the [gradient descent](http://en.wikipedia.org/wiki/Gradient_descent) algorithm can be implemented in C# to solve a liniar equation problem. 
I've made all the equations visible in the inspector:

<img src="https://github.com/eman-insilico/Unity-ML-gradient-descent-OLS-liniar-regression/blob/master/Gradient%20Descent%20inspector.JPG" width="220">

### Code Requirements
The example code is in Python ([version 2.6](https://www.python.org/doc/versions/) or higher will work). The only other requirement is [NumPy](http://www.numpy.org/).

### Description
This code demonstrates how a gradient descent search may be used to solve the linear regression problem of fitting a line to a set of points. In this problem, we wish to model a set of points using a line. The line model is defined by two parameters - the line's slope `m`, and y-intercept `b`. Gradient descent attemps to find the best values for these parameters, subject to an error function.

The code contains a main function called `run`. This function defines a set of parameters used in the gradient descent algorithm including an initial guess of the line slope and y-intercept, the learning rate to use, and the number of iterations to run gradient descent for. 

```python
initial_b = 0 # initial y-intercept guess
initial_m = 0 # initial slope guess
num_iterations = 1000
``` 

Using these parameters a gradient descent search is executed on a sample data set of 100 ponts. Here is a visualization of the search running for 200 iterations using an initial guess of `m = 0`, `b = 0`, and a learning rate of `0.000005`.

<img src="https://github.com/eman-insilico/Unity-ML-gradient-descent-OLS-liniar-regression/blob/master/OLS.gif" width="450">

<img src="https://github.com/eman-insilico/Unity-ML-gradient-descent-OLS-liniar-regression/blob/master/Gradient%20Descent.gif" width="450">

### Execution
To run the example, simply run the `gradient_descent_example.py` file using Python

```
python gradient_descent_example.py
```

The output will look like this

```
Starting gradient descent at b = 0, m = 0, error = 5565.10783448
Running...
After 1000 iterations b = 0.0889365199374, m = 1.47774408519, error = 112.614810116
```

