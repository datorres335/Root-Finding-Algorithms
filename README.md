# Root-Finding Methods: Bisection, Newton-Raphson, Secant, and False-Position

## Overview
This program implements four numerical methods for root-finding:
- **Bisection Method**
- **Newton-Raphson Method**
- **Secant Method**
- **False-Position Method**

The program ensures solutions converge within a given tolerance and detects divergent or slow-converging solutions.

## Implementation Details
This program is implemented in **Java** using a single main file:
1. **Main.java** - Handles user input, applies root-finding methods, and exports results.

## Input Format
The user provides:
1. **Starting values** for each method.
2. **Error tolerance (ea < 1%)**.
3. **Maximum iterations (100 iterations max).**

## Functions Used
The program evaluates roots for two functions:
(a) **f(x) = 2x³ – 11.7x² + 17.7x – 5**  
   - This function has **three positive roots** in the interval **[0,4]**.
(b) **f(x) = x + 10 – x cosh(50/x)**  
   - The root lies in the interval **[120,130]**.

## Program Output
1. **Root estimates for each method at each iteration**.
2. **Approximate relative percent error for each method**.
3. **Final root value once convergence is reached or after 100 iterations**.
4. **Exports error values for plotting**.

## Example Run
### **User Input**
```
Please choose the first starting value for the methods to use on function 1: 0
Please choose the second starting value for the methods to use on function 1: 4
```

The program applies **all four methods** to find the roots.

### **Example Output**
```
Relative error array exported to bisectFunction1_R34.txt
Relative error array exported to falsePosFunction1_R34.txt
Relative error array exported to newtonRaFunction1_R34.txt
Relative error array exported to secantFunction1_R34.txt
```
If the solution **does not converge** within 100 iterations, the program displays:
```
Sorry solution did not converge to desired relative percent error within 100 iterations.
```
### **User Input**
```
Please choose the first starting value for the methods to use on function 2: 1
Please choose the second starting value for the methods to use on function 2: 3
```

The program applies **all four methods** to find the roots.

### **Example Output**
```
Relative error array exported to bisectFunction1.txt
Relative error array exported to falsePosFunction1.txt
Relative error array exported to newtonRaFunction1.txt
Relative error array exported to secantFunction1.txt
```
If the solution **does not converge** within 100 iterations, the program displays:
```
Sorry solution did not converge to desired relative percent error within 100 iterations.
```

## Plotting the Results
The program exports error values to **text files**, which can be plotted using **Google Sheets, Excel, Python, or MATLAB**.

### **Exported Files**
- `bisectFunction1_R34.txt`
- `falsePosFunction1_R34.txt`
- `newtonRaFunction1_R34.txt`
- `secantFunction1_R34.txt`
- `bisectFunction1.txt`
- `falsePosFunction1.txt`
- `newtonRaFunction1.txt`
- `secantFunction1.txt`

Each file contains **iteration vs. relative percent error**, which can be plotted with:
- Logarithmic scale of error values.

## Java Code Structure
### **Main.java**
- **Handles user input** for starting values.
- Implements all **four root-finding methods**.
- **Checks for convergence** and stops if error criteria are met.
- **Exports iteration data** for visualization.

## Usage Instructions
1. **Compile the program**:
   ```bash
   javac Main.java
   ```
2. **Run the program**:
   ```bash
   java Main
   ```
3. **Follow the prompts** to input starting values.
4. **View the step-by-step solution and final computed results.**
5. **Plot the error data** using external software.
