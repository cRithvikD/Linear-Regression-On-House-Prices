# Linear-Regression-On-House-Prices

Project link on Kaggle: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview

Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this project challenges us to predict the final price of each home.

# Summary of results using Linear Regression

Our final model is: 

SalePrice ~ LotArea + BsmtFinSF1 + SaleCondition + TotalBsmtSF + GarageCars + GrLivArea + Neighborhood + C(OverallQual) + OverallCond + YearBuilt 

This is a combination of predictors that comprehensively cover key dimensions across size, location, condition/amenity, and transaction to predict the sale price of real estate. 

Additionally, we are confident that this is the best model because Adjusted R2 increased from 0.853 to 0.927. Additionally, we
1. Removed predictors with t-test p-values for all levels < 0.05
2. Conducted EDA to confirm that there is no high correlation between numerical predictors and removed predictors with a high proportion of NULL values 
3. Conducted data structure validation to remove predictors with high multicollinearity (VIF, autocorrelation plot), and removed outlier data points (External studentized residuals, Cook’s Distance) 
4. Conducted model assumption checks around heteroskedasticity (Breush-Pagan Test) , normality (KS Test, JB Test, Histogram and scatter plot of residuals, QQ plot) , and linear relationship between chosen predictors and the response variable (scatter plot of predictors versus response variable) 
5. Selected the model based on the optimal order of predictors (ANOVA Type=1) and also from the pool of all possible combinations of predictors (Adjusted R2, Mallow’s Cp, AIC, BIC)


# Acknowledgments

1. The Ames Housing dataset was compiled by Dean De Cock for use in data science education. It's an incredible alternative for data scientists looking for a modernized and expanded version of the often cited Boston Housing dataset.
2. Anna Montoya, DataCanary. (2016). House Prices - Advanced Regression Techniques. Kaggle. https://kaggle.com/competitions/house-prices-advanced-regression-techniques
3. Thanks to Dr. Shan Wang for organizing this competition as part of the 'MSDS 601: Linear Regression Analysis' course at USFCA!
4. Thanks to Belinda Ong and Ronel Solomon for being brilliant teammates!

