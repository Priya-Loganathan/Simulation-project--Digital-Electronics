# TITLE
Minimise the function using K map F(A,B,C)=A'B+BAC'+A'B'C' and simulate the logic diagram using verilog.

# THEORY
K-MAP
The K-map or Karnaugh map is a graphical tool to minimize a boolean function.
## Truth Table for 3-Variable Map
It is a well-known fact that K-map is nothing but a different representation of truth table; therefore, a truth table for 3 variables will contain 2^3 = 8 rows. This also means that the K-map would contain total of 8 cells, each for a row in the truth table.
## Characteristics of a 3-variable K-map
The truth table has total of 8 rows which corresponds to 8 cells of the 3-variable K-map.
Each cell differs in only one variable to its neighbor, both horizontally and vertically.
To minimize the terms in a boolean function, mark a cell as 1 if its output is 1 in the truth table and leave the rest as it is.
To minimize the variables within each term of a cell that has 1 in K-map, start making groups of 2, 4, and 8.
Grouping of 1s includes neighboring cells, corners and sides even though they overlap each other.
Make larger groups if possible.
Once all 1s are covered then you can stop.

![image](https://github.com/Priya-Loganathan/Simulation-project--Digital-Electronics/assets/121166075/22523d8c-26bb-47d6-8ed0-c399f6483e08)


# PROCEDURE
1.Simplify and Minimise the given function.

2.Draw the K-map for the same.

3.Obtain the minimised function.

4.Open the Quartus software and create a new file.

5.Feed and run the program .

6.The RTL viewer and the timing diagram will be displayed.
# PROGRAM
```
module simu(a,b,c,f);
input a,b,c;
output f;
wire abar,cbar,x,y;
not(abar,a);
not(cbar,c);
and(x,abar,b);
and(y,b,cbar);
or(f,x,y);
endmodule 
```

# NETLIST DIAGRAM
![simurtl](https://github.com/Priya-Loganathan/Simulation-project--Digital-Electronics/assets/121166075/0c795f0e-6b87-4fdd-bd4b-752dd9fbf659)

# TIMING DIAGRAM
![simutimer](https://github.com/Priya-Loganathan/Simulation-project--Digital-Electronics/assets/121166075/3c81f3c5-73f7-4fcc-9387-693acdfa381e)

# RESULT
Thus the program to minimise the function using K map is implemented and executed successfully.
