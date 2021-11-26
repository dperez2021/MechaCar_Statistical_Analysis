# MechaCar_Statistical_Analysis

## Overview of Project

A few weeks after Jeremy started his new role, he is approached by upper management about a special project. AutosRUs' newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team's progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, we'll help Jeremy and the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Deliverables:

This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

1. Deliverable 1: Linear Regression to Predict MPG
2. Deliverable 2: Summary Statistics on Suspension Coils
3. Deliverable 3: T-Test on Suspension Coils
4. Deliverable 4: Design a Study Comparing the MechaCar to the Competition

## Resources:

This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

- Data Source: MechaCar_mpg.csv and Suspension_Coil.csv
- Data Tools: tidyverse, dplyr, ggplot2 and MechaCarChallenge.RScript.
- Software: RStudio and R


## Deliverable 1:
### Linear Regression to Predict MPG

![D1](https://user-images.githubusercontent.com/88256967/143614500-aff0edb5-20bd-4824-a85f-153f96f57e22.PNG)


- In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. The vehicle length, and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model. That is to say, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype.

- The p-Value for this model, p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indcates that the slope of this linear model is not zero

- This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, his multiple regression model does predict mpg of MechaCar prototypes effectively.

When we remove less impactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability does decrease, but not drastically: the r-squared value falls from 0.7149 to 0.674.

![D1B](https://user-images.githubusercontent.com/88256967/143614515-b76d5b68-d24b-4601-8b5a-c0749d01cbde.PNG)


## Deliverable 2:

![D2A](https://user-images.githubusercontent.com/88256967/143614529-c63907eb-d22f-404d-bdd2-2de14592df3f.PNG)


All Manufacturing Lots

![D2B MANUFACTUR LOT](https://user-images.githubusercontent.com/88256967/143614540-82eab0a1-9744-4021-98b1-9e75e585f0f1.PNG)


By each manufacturing lot

![D2 PLOT](https://user-images.githubusercontent.com/88256967/143614550-aa88e638-a3d5-4ff0-b939-48edccf1ffb8.PNG)


Plot by each manufacturing lot

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
The design specs are respected for all manufacturing lots in total with a global variance of 62.3 psi.
On the lot level, Lot 1 and Lot 2 are into specs with respectively variances of 0.98 and 7.5 psi. The Lot 3 is out of specs with a variance of 170.3 psi.

## Deliverable 3
### t-Tests on Suspension Coils
### T-Test all manufacturing lots against the population mean



Assuming our significance level is the common 0.05 percent, our p-value of 0.069 is above the significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we can state that the PSI across all manufacturing lots is statiscally similar to the population mean of 1498.78 psi.

### T-Tests each manufacturing lot against the population mean

![D3A](https://user-images.githubusercontent.com/88256967/143614560-9e17c88b-af5d-458b-8fb2-a3d3a8db0684.PNG)

Lot 1

![D3B1](https://user-images.githubusercontent.com/88256967/143614574-46a40b24-d8d5-41a6-8425-993fa80b8d77.PNG)


Here the p-value is below the significance level of 0.05 percent, so we can reject the null hypothesis and conclude that the PSI across the Lot 1 is statistically different from the population mean.

Lot 2 & Lot 3

![D3B2](https://user-images.githubusercontent.com/88256967/143614589-19297583-3802-4c93-afa0-9374655e494e.PNG)
![D3B3](https://user-images.githubusercontent.com/88256967/143614592-f78a51c5-7f48-4ef7-b3c4-38944028bbc3.PNG)


Here both p-values are above the significance level, so we can conclude that the PSI for Lot2 and Lot3 are statistically similar to the population mean.



