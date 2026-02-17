# CSE5280_assignment_floor_plan_animation

## Summary

This is the code for running floor plans using different gradient decent functions. This code uses multiple maps to compare cost functions and compare between them. The SRC code contains the entire code list. 

**/src/Floor_Plan_Assignment.ipynb** contains all code and compiled visual images

## Parameters Functions

*the ipynb file includes multiple paramters and functions to choose from*

### Wall_cost Parameters
**R** - Range to calculate wall cost

**wall_cost_factor** - the factor strengthen the wall cost versus the distance cost

**pts_distance()** - selects the function to cacluate the point distance to the wall
* dot - calculates euclidean distance
* vectorize - calculate distance by the highest value (square distances)

**wall_penalty_function()** - selects the function to calculate the penalty cost for teh walls
* Quad - square function (parabola)
* Quartic - power 4 function
* LN - natural log function
* Linear - linear function (degenerate case)

### Gradient
**gradient_step** - calculating the next h step for the derivative

**gradient_function()** - selectes the type of method to calculate the gradient
* simple - f'(x) = f(x+h)-f(x)/h
* avg - f'(x) = ( f(x+h)-f(x) ) + ( f(x) -f(x-h) ) / (2*h)

### Gradient Vector Map
**steps** - the distance between each position to calculate the gradient

### Movement animation
**Step_Max_Limit** - the maximum number of steps before the calculation stops

**distance_per_step** - the distance the position moves per step

### Floor Plan selection

**floor_plan** - 
* baseline
* zigzag
* deadended
* symmetric

**use_gradient** - show Gradient Vector Map

**create_movelist** - allows to cacluate the movement anmation of object from start to finish

## Parameters for each wall cost function

these are the best parameters to use for each function

> Step_Max_Limit = 1000

> distance_per_step = 0.1
### quad

| Variable         | Value        |
| -------------    | ------------ |
| R                | 1            |
| gradient_step    | 0.4          |
| pts_distance     | dot          |
| wall_cost_factor | 2            |
| gradient_fuction | avg          |

### quartic
| Variable         | Value        |
| -------------    | ------------ |
| R                | 1            |
| gradient_step    | 0.3          |
| pts_distance     | vectorize    |
| wall_cost_factor | 2            |
| gradient_fuction | avg          |

### LN

| Variable         | Value        |
| -------------    | ------------ |
| R                | 1            |
| gradient_step    | 0.4          |
| pts_distance     | vectorize    |
| wall_cost_factor | 0.5          |
| gradient_fuction | avg          |

### Linear

| Variable         | Value        |
| -------------    | ------------ |
| R                | 1            |
| gradient_step    | 0.2          |
| pts_distance     | vectorize    |
| wall_cost_factor | 2            |
| gradient_fuction | avg          |

### Analysis

Analysis of the code is in the CSE5280_FLoor_Plan_Analysis.docx document