# hello-world
Just another repository

Changes from new branch

# Calculating Fatigue Crack Growth Rate

## ASTM E647 methods
The following methods are described in depth in ASTM E647

### Secant Method 
This method is a direct calculation of the local slope and is succeptible to data noise at small crack growths. 

da/dN = (a<sub>i+1</sub> + a<sub>i</sub>) / (N<sub>i+1</sub> + N<sub>i</sub>)

### Incremental Polynomial
This method is preferred because it reduces noise from the data using a regression fit.

Using a second-order polynomial equation of the form to sets of (2n + 1) successive data points, where n is usually 
1, 2, 3, or 4. The form of the equation for the local fit is as follows:

&acirc;<sub>i</sub> = b<sub>0</sub> + b<sub>1</sub>x + b<sub>2</sub>x<sup>2</sup>

where:

x = (N<sub>i</sub> - C<sub>1</sub>) / C<sub>2</sub> , and -1 &le; x &le; 1

The parameters C<sub>1</sub> and C<sub>2</sub> are used to the scale the input data, thus avoiding numerical 
difficulties in determining regression parameters.

C<sub>1</sub> = (N<sub>i</sub> + N<sub>i+1</sub>)/2

C<sub>2</sub> = (N<sub>i</sub> - N<sub>i+1</sub>)/2

The rate of crack growth at N<sub>i</sub> is obtained from the derivative of the polynomial equation:

(da/dN)<sub>&acirc;</sub> = b<sub>1</sub>/C<sub>2</sub> + 2b<sub>2</sub>(N<sub>i</sub> - C<sub>1</sub>) / 
C<sub>2</sub><sup>2</sup>

*__Note: Filtering the crack growth data, based on a change in crack length, can aid in creating a better 
Crack Growth Rate Curve.__*

## Modified Incremental Method - Larsen
This method is often used instead of the Incremental Polynomial Method. The excerpt below 

>The modified incremental method uses regression intervals based on intervals in crack length (Da),
rather than intervals based on a number of points, as in ASTM E647. Each regression interval is separated from the previous
and subsequent intervals by Da and includes a range of data ±3&Delta;a (Fig. 2). All data points within the ±3&Delta;a interval are used
in a regression where the FCGR is calculated at the center based on the slope of a polynomial fitted to the data. If the regression
interval ended up with fewer than seven points, the interval range was incrementally increased by ±&Delta;a until seven
points were included.`




