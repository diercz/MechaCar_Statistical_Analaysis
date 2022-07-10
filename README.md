# MechaCar_Statistical_Analaysis

## Overview

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. The purpose of this analysis is to review the production data for instights that may help avoid manufacturing risks.  

## Linear Regression to Predict MPG

First we took a look at the correlation Coefficient Matrix to identify variables of interest.  There are no variables that share what is considered a strong correlation (1>= absolute value "r">= 0.7), as revealed in the matrix.

![webpage](cor coeff)

### Correlation Coefficient Matrix

- "MPG" and "Vehicle Length" share a moderate correlation of 0.61, which is the strongest of the variables provided.  "MPG" and "Ground Clearance" cam in sencond at a weaker correlation level of 0.33.
- When we square the Vehicle Length coefficient, we get a R-squared of approximately 0.37, which indicates that Vehicle Length will only predict about 37% of MPG observations.  

![webpage](mult lin reg)

### Multiple Linear Regression

- Analyzing our results, vehicle length and ground clearance are statistially unlikely to provide random amounts of variance to the linear model. Meaning they have a significant impact on MPG.
- In addition, the p-value of our linear regression is 5.35e-11, which is much smaller than our assumed significance level of 0.05%.  Therefore, we can state that there is sufficient evidence to reject the null hypothesis, meaning the slope of our linear model is not zero.
- R-squared of approximately 0.71.  This indicates that the multiple linear regression will predict 71% of mpg observations. 

## Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 lbs per square inch (PSI).  We are looking to determine that the manufacturing data meets the design specs for all manufacturing lots in total and each lot individually.  

The dataset is comprised of the PSI Metric for 150 vehicles produced in three lots.

#### Total Summary Table

![webpage](total sum DF)

#### Lot Summary Table

![webpage](lot sum DF)

#### PSI Summary

- Per the Total Summary Table, PSI variance for all lots combines is 62.29 lbs per square inch, which satisfies the design spec requirements.
- Per the Lot summary above, PSI variance in Lots 1-3 yield 0.98, 7.47, 170.29 lbs per square inch.

At first thought it was to be believed that lot three was doing something incorrect as it exceeded the 100lb weight capacity, but after reviewing the Median and Mean for the Lot we determined that the data is skewed left.  This indicates that there is a higher probability that the lower weights exist at this location than others.  

We would recommend that the manufacturing team review its approach with vehicle allocation to these lots in order to normalize distribution so they each meet the design specs.  

## T-Tests on Suspension Coils

We are determining if all lots and each individual lot are statistically different from the population meant of 1,500 pounds per square inch.  We performed T-tests to calculate the p-value and compared it against the significance value of 0.05.

#### All Manufacturing Lots

![webpage](all man lots)

P-Value, 0.06 is above the common level of 0.05.  This means we do not have sufficienct evidence to reject that there is a statistical difference between all lots and the population mean.  The two means are statistically similar.  

#### Lot One

![webpage](lot 1)

P-Value, 1 is above the significance level.  This means we do not have sufficent evidence to reject that there is a statistical difference between Lot 1 and the population mean.  The two means are statistically similar.

#### Lot Two

![webpage](Lot 2)

P-Value, 0.61 is above the significance level.  This means we do not have sufficent evidence to reject that there is a statistical difference between Lot 2 and the population mean.  The two means are statistically similar.


#### Lot Three

![webpage](Lot 3)

P-Value, .042 is below the significance level.  This means there is sufficient evidence to reject that there is a statistical difference between Lot 3 and the population mean.  The two means are statistically different.  

## Study Design: MechaCar vs. Competition

To ensure the MechaCar prototype is a success, we should evaluate how it stands up to the competition.  A potential study will provide a statistical insight to how MechaCar compares to its competition.

### Metrics

Metrics to test are both city and highway fuel efficiency.

### Hypothesis

Null: MechaCar has the same fuel efficiency for each cylinder class.  Alternative: MechaCar does not have the same fuel efficiency for each cylinder class.

### Statistical Test

Use Linear regression and Sample T-tests to test the hypothesis against the population mean for each metric.

### Data

Data needed to perform our tests we would want the following variables: Manufacturer, Engine Size, Highway Fuel Efficiency, City Fuel Efficiency, Model, Year, and Cost.  