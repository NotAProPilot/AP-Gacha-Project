# AP-Gacha-Project
## Overview
- The program will be divided into 4 parts
1. Basics about Probability 
2. Conditional probability and Bayes' Theorem
3. Distribution Functions
4. Sampling

## Calculating Z-distribution, T-distribution
### Z-distribution
```java
import java.util.Scanner; // import the Scanner class for user input
import org.apache.commons.math3.distribution.NormalDistribution; // import the NormalDistribution class from the Apache Commons Math library

public class ZScoreCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // create a Scanner object for user input
        System.out.print("Enter the z value: ");
        double zValue = scanner.nextDouble(); // read the z value from user input

        NormalDistribution standardNormal = new NormalDistribution(); // create a NormalDistribution object
        double areaUnderCurve = standardNormal.cumulativeProbability(zValue); // calculate the cumulative distribution function (CDF)
        
        System.out.println("The area under the curve from -infinity to z value " + zValue + " is: " + areaUnderCurve); // print the calculated area under the curve
    }
}
```
or
```python
# import the scipy.stats library for our program
import scipy.stats as st 

# asking user input for z value
z_value = float(input("Enter the z value: "))

# calculating the cumulative distribution function (CDF) for the given z value
# the area under the curve to the point z is essentially the CDF from -infinity to z. 
area_under_curve = st.norm.cdf(z_value)

# printing the calculated area under the curve
print("The area under the curve from -infinity to z value", z_value, "is:", area_under_curve)

```



