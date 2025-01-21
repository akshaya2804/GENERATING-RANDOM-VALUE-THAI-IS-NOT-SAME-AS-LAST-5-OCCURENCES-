# GENERATING-RANDOM-VALUE-THAT-IS-NOT-SAME-AS-LAST-5-OCCURENCES-

Overview

This project implements a Random Number Generator in SystemVerilog that ensures each generated number is unique compared to the last five generated values. The implementation leverages SystemVerilog's randomize() function and constraints to enforce the uniqueness requirement.

Key Components

Class Definition (RandomNumber)

The RandomNumber class contains:

a: A 4-bit random number (values range from 0 to 15).
last_values: An array storing the last 5 generated random values.
unique_constraint: A constraint ensuring that the new random number is not equal to any of the values stored in the last_values array.

Key features:

Constraint Logic: The unique_constraint ensures that the new value of a is not equal to any element in last_values.
randomize_and_update Task: Handles the randomization of a and updates the last_values array with the latest generated value, maintaining only the most recent 5 numbers.
Testbench (testbench)

The testbench creates an instance of the RandomNumber class and generates 10 random values using the randomize_and_update task.
The generated random numbers are displayed using the $display system task.

 It Works
 
Randomization

The randomize() method generates a 4-bit random number (a).
The constraint ensures that the generated number is unique compared to the last 5 numbers.

Array Update

The last_values array stores the last 5 generated numbers.
Each new value is appended to the array while the oldest value is removed, maintaining the array size at 5.

Testbench Execution

The testbench initializes the RandomNumber class.
It runs a loop to generate 10 random numbers while printing each value to the console.

Output

A sample output of the program:

Randomized value: 2
Randomized value: 5
Randomized value: 8
Randomized value: 3
Randomized value: 12
Randomized value: 7
Randomized value: 4
Randomized value: 6
Randomized value: 9
Randomized value: 1
