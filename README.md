MAT 303 Module Two Problem Set Report
Interaction Terms and Qualitative Predictors
Ahmed Ahmed
[ahmed.ahmed3@snhu.edul]
Southern New Hampshire University
1. Introduction
This analysis explores the relationship between fuel economy and several vehicle characteristics using the mtcars dataset. The dataset contains information on 32 automobiles from the 1974 Motor Trend magazine. The goal is to examine how horsepower, quarter-mile time, the interaction between horsepower and quarter-mile time, and the number of cylinders influence miles per gallon. Results from this analysis could help manufacturers or consumers understand how engine performance and design features affect fuel efficiency. A multiple linear regression model that includes both an interaction term and a categorical predictor will be used.
2. Data Preparation
The important variables in this analysis are miles per gallon (mpg), horsepower (hp), quarter-mile time (qsec), and number of cylinders (cyl). The mpg variable measures fuel economy, hp measures engine power, qsec measures acceleration performance, and cyl is a categorical variable indicating whether the car has 4, 6, or 8 cylinders. The mtcars dataset contains 32 rows (observations) and 11 columns (variables).
3. Model With Interaction Term and Categorical Predictor
Correlation Analysis
The Pearson correlation coefficient between fuel economy (mpg) and horsepower (hp) is approximately –0.776, indicating a strong negative linear relationship. As horsepower increases, miles per gallon tends to decrease. The correlation between mpg and quarter-mile time (qsec) is approximately 0.419, indicating a moderate positive linear relationship. Cars with higher quarter-mile times (slower acceleration) tend to have slightly better fuel economy.
Reporting Results
The general form of the regression model is:
mpg = β₀ + β₁(hp) + β₂(qsec) + β₃(hp × qsec) + β₄C(cyl=6) + β₅C(cyl=8) + ε
Using the output from the regression, the estimated prediction equation is:
mpg ̂= 24.506 + 0.142(hp)+ 0.532(qsec)- 0.0125(hp × qsec)-      
4.408C(cyl=6) - 4.581C(cyl=8)
The R-squared value is 0.833 and the adjusted R-squared is 0.801. This means that approximately 83.3% of the variation in miles per gallon is explained by the predictors in the model. The adjusted R-squared remains high after accounting for the number of predictors, indicating a strong model.
 
 
The Residuals vs Fitted Values plot shows points scattered around the horizontal line at zero with no strong systematic pattern, which supports the assumption of homoscedasticity. The Normal Q-Q plot shows that the residuals generally follow the reference line, with only minor deviations in the tails. Overall, the assumptions of homoscedasticity and normality appear reasonably satisfied.
Evaluating Model Significance
The overall F-test has a p-value of approximately 2.53 × 10⁻⁹, which is much smaller than 0.05. Therefore, we reject the null hypothesis and conclude that the model is statistically significant at the 5% level.
Individual term significance at the 5% level:
• The interaction term (hp × qsec) is significant (p = 0.025).
• The indicator for 6-cylinder cars is significant (p = 0.012).
• The intercept, horsepower, quarter-mile time, and the indicator for 8-cylinder cars are not significant at the 5% level.
Making Predictions Using the Model
For a car with 175 horsepower, a quarter-mile time of 14.2 seconds, and 6 cylinders, the predicted fuel economy is approximately 21.34 mpg.
The 95% prediction interval is approximately (14.88, 27.81). This means we are 95% confident that the fuel economy for an individual car with these characteristics will fall between 14.88 and 27.81 mpg.
The 95% confidence interval for the mean response is approximately (18.00, 24.69). This means we are 95% confident that the average fuel economy for all cars with these characteristics falls between 18.00 and 24.69 mpg.
Prediction intervals are wider than confidence intervals because they account for both the uncertainty in estimating the mean response and the additional variability of individual observations.
4. Conclusion
Based on the analysis, the multiple regression model is statistically significant and explains a large portion of the variation in fuel economy. The interaction between horsepower and quarter-mile time is significant, as is the effect of having 6 cylinders compared to 4 cylinders. Residual diagnostics do not indicate major violations of model assumptions. Assuming the sample size is adequate, this model can reasonably be used to understand the relationships among these variables. Practically, the results suggest that fuel economy depends not only on individual predictors but also on how horsepower and acceleration performance interact, and that the number of cylinders plays a meaningful role.

<img width="468" height="642" alt="image" src="https://github.com/user-attachments/assets/e188ec6a-87e9-4374-8546-0fa28428c4e1" />
