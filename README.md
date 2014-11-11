Improved Euler's method ODE solver
======================

A simple script that outputs a results table based on a given ordinary differential equation.

Inspired by my math homework, which showed me that Euler's Method is a very repetitive process.  I couldn't find a tool that would easily let me solve using this method and I didn't want to enter a few very similar forumlas 10 times with different values, so I wrote one myself. I also prefer coding to doing my math homework so this is a compromise.

##Usage

###Entering the Equation
When prompted for an equation, give it in its full form with all operators. **The equation must be in terms of `x` and `y`.**

```
Enter an ODE (with all operators, incl. *) to be solved: 
>>> 2 * x + 3 / 4 * y - 15
```
NOT

```
Enter an ODE (with all operators, incl. *) to be solved: 
>>> 2sin(x) + 4y
```

###Initial values

Enter initial numerical values for x and y when prompted

```
Enter an initial x: 
>>> 3

Enter an initial y: 
>>> pi
```

**Constants `pi` and `e` are supported.

**Rationals are not currently supported.

###Calculation value

The program will prompt for a calculation value. This is the x value you wish to calculate up to. It will be the last row printed in the table.

```
Enter the value to calculate up to: 
>>> 2.1
```

###Step value

The step value (h) is the increment of x for each value calculated. It determines how many rows will be in the table. Typically this value can be `0.1` or `0.05`. A smaller step value yields more precise results for the whole table.

```
Enter the step value (h) to use for the calculation: 
>>> 0.05
```
###Typical output
```
Enter an ODE (with all operators, incl. *) to be solved: 
>>> y - pow(y, 2)
Enter an initial x: 
>>> 0
Enter an initial y: 
>>> 0.5
Enter the value to calculate up to: 
>>> 0.5
Enter the step value (h) to use for the calculation:
>>> 0.05

---RESULTS---

0.0 	 0.5
0.05 	 0.5125
0.1 	 0.525
0.15 	 0.5375
0.2 	 0.55
0.25 	 0.5625
0.3 	 0.575
0.35 	 0.5875
0.4 	 0.6
0.45 	 0.6125
0.5 	 0.625
0.55 	 0.6375


```

##Supported Functions

The currently supported functions are the following:

- Floor: `floor(x)`
- Ceiling: `ceil(x)`
- Exponential: `exp(x)`
- Logarithm: `ln(x)`, `log(x, base)`, `log10(x)`
- Power: `pow(x, y)`
- Square root: `sqrt(x)`
- Trig functions: `sin(x)`, `cos(x)`, `tan(x)`, `asin(x)`, `acos(x)`, `atan(x)`
- Hyperbolic trig functions: `sinh(x)`, `cosh(x)`, `tanh(x)`, `asinh(x)`, `acosh(x)`, `atanh(x)`

They can be passed any integer or floating-point number, or the varaibles `x` or `y`. You can include them within the entered ODE as you would any number


##Limitations

- [ ] Loss of precision
- [ ] Found some incorrect functions giving incorrect results, definitely still needs work

Basic concept at the moment, more thorough testing is definitely needed. Expansions and improvements that could be made remain to be seen. Suggestions are more than welcome.
