# Install sympy for symbolic mathematics
!pip install sympy

import sympy as sp

def bisection_method(f, a, b, tol=1e-4, max_iterations=100):
    iterations = 0
    
    while (b - a) / 2 > tol and iterations < max_iterations:
        c = (a + b) / 2
        fa = f(a)
        fc = f(c)
        
        if fa * fc < 0:
            b = c
        else:
            a = c
        
        iterations += 1
    
    root = (a + b) / 2
    return root, iterations

# Define the equation
x = sp.symbols('x')
equation = x**3 + 4*x**2 - 10
f = sp.lambdify(x, equation)

# Perform bisection method
root, iterations = bisection_method(f, 1, 2, tol=1e-4)

print("Root:", root)
print("Iterations:", iterations)
