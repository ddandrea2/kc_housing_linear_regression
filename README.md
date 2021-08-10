# Linear Regression Analysis of KC Housing Data

Using OLS regression, the best performing model consisted of the following features:

* sqft_living
* waterfront
* lat
* grade*sqft_living15

The final r-squared score for the train data was approximately 0.717, while the r-squared score for the test data was 0.712, meaning the model can explain the variation in home prices ~71.2% of the time. The model produces a RSE of $211,724, which is the average amount the selling price differs from what the model predicts. While there is no set standard by which to judge RSE, it's fair to say that producing an error this large may be problematic. The RSE is about 39.4% of the average selling price of $537,861, to put it into perspective.

Looking at the regression diagnostics, it can be concluded that all three assumptions for the residuals of a linear regression model have most likely been violated. The distribution of the residuals is leptokurtic, they exhibit heterskedasticity, and the model variables may not have a linear relationship with the target.
![heteroskedasticity](/Graphs/download-1.png)


Taking all of this information into account, a linear model may not be the best model to use for this dataset, but a decent linear model was nevertheless created. For the realtor, it does give an idea of the important factors contributing to the sale price of a home out of a pool of features. Some of the features, such as liveable square footage, waterfront properties and renovations may not be surprising as being important. Other features, such as latitude and grade*sqft_living15 are more interesting.

This model should be used in conjunction with realtor experience and intuition in the formulation of an appropriate asking and/or selling price for a client's home. If they are available, adding more features to include in the model as well as more year's worth of data may improve the accuracy of the model. Other predictive models should also be considered; the goal would be to find a predictive model that would increase accuracy while decreasing or maintaining model complexity. This linear model is a great starting point because it is relatively easy to understand and interpret.

## Next Steps
Going back to the histograms of the features prior to log transformation, some of the features, such as sqft_lot, had data points that were significantly larger than the other data points, skewing the distribution. It may be worthwhile to go through each of these features and look for outliers. Taking these outliers into account and potentially adjusting for them may make some the features that were insignificat, significant. This in turn could lead to a better model.
