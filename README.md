# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

With the Mecha Car dataset, I performed a multiple linear regression to predict the impact that vehicle length, vehicle weight, spoiler angle, ground clearance, and all wheel drive have on a car's mpg. After using the lm() function to perform the linear regression, I used the summary() function to see the full summary from the linear regression. 

In the summary, I looked at the p-value for each of the independent variables to see which one had a non-random amount of variance in the mpg values in our datasets. In general, a p-value above .05 shows a non-random amount of variance. As can be seen in our summary, vehicle weight, spoiler angle, and AWD all show a p-value higher than .05, implying that those variables show a non-random amount of variance to our mpg values. Our other independent variables have a p-value below the .05 threshold, indicating that they are not significantly impacting a vehicles mpg. 

![Multiple Linear Regression](https://github.com/nicole-tough/MechaCar_Statistical_Analysis/blob/main/MPG_Linear_Regression.PNG)

The slope of the linear model is not considered to be zero. We have several indpendent variables with significant coefficients that result in formula for our linear model. In our formula for linear regression, each of these coefficients would be multiplied by their respective data points to find our slope. 

This linear model does predict mpg of MechaCar prototypes effectively for two reasons. First, it highlights several independent variables that are demonstrating a non-random influence on the MechaCar's mpg. Secondly, the p-value of the intercept is showing random variance. If the intercept was showing non-random variance, that may demonstrate that our data would need to be transformed that there may be other variables outside of our model that are influencing the mpg. However, this is not the case as our p-value for the intercept in this model was below .05.

## Summary Statistics on Suspension Coils

In the next section of my analysis, I used data from MechaCar regarding their suspension coil production. It is important for MechaCar that each lot is producing suspension coils with the same standards and specifications. In order to check this across 3 separate lots, I performed an analysis to obtain the mean, median, variance and standard deviation from each lot. 

The design specifications for MechaCar dictate that the variance of suspension coils must not exceed 100lbs per square inch. Across all lots, we found that they are within these specifications with a variance of 62.29. 

![Total Summary](https://github.com/nicole-tough/MechaCar_Statistical_Analysis/blob/main/total_summary.PNG)

In order to see if the variance of the suspension coils was within the specifications for each lot, I also created a lot summary to show the details of each Lot. I found that one lot in particular was outside of the specifications. As can be seen in the Lot Summary below, Lot 3 has a variance of 170.29, which is above MechaCar's specifications.

![Lot Summary](https://github.com/nicole-tough/MechaCar_Statistical_Analysis/blob/main/lot_summary.PNG)

## T-Tests on Suspension Coils

In the third section of my analysis, I conducted a t-test for each lot to compare the mean of the PSI from each Lot to the expected mean of 1500 pounds/square inch. Upon conducting the t-test, I found that the means from Lot 1 and Lot 2 are statistically similar to 1500, but the mean from Lot 3 is not. 

In my t-test from Lot 1, you can see that the p-value is equal to 1. The p-value being above .05 percent demonstrates that we do not have significant evidence to reject the null hypothesis, and we can conclude that means are statistically similar. 
![Lot 1](https://github.com/nicole-tough/MechaCar_Statistical_Analysis/blob/main/t.test_lot1.PNG)

My t-test from Lot 2 shows a p-value of 0.61, demonstrating that we will again reject the null hypothesis and conclude that the means are statistically similar.

![Lot 2](https://github.com/nicole-tough/MechaCar_Statistical_Analysis/blob/main/t.test_lot2.PNG)

However, my t-test from Lot 3 shows a p-value of .04, which is below our significance level of .05. Therefor, we can must reject the null hypothesis because these results are demonstrating that the means are not statistically similar. 
![Lot 3](https://github.com/nicole-tough/MechaCar_Statistical_Analysis/blob/main/t.test_lot3.PNG)

## Study Design: MechaCar vs Competition

In order to compare MechaCar's performance with its competition, I recommend using a two-sample t-test to compare the mean maintenance cost of MechaCar vehicles with competing brand vehicles.

Our alternative hypothesis would be "The mean cost of maintenance for MechaCar vehicles differs from the mean cost of maintenance for competing brands."

To do this, I would use the metrics of maintenance cost. We would need data points from across the lifespan of cars from MechaCar and other brands that show how much money was spent throughout the lifetime of the car to maintain the vehicle. With these data points, we can calculate the mean maintainence cost for each brand and then run a two sample t test to see if there is a significant difference between the two means. 





