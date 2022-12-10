# Phase_2_Project

Business Case
Model Business for us to look at: https://constructionconsulting.co/

Royal Advisory is a Construction Consulting firm. We help contractors and construction companies identify the most valuable home renovations to invest in.

* Because the housing market is cooling rapidly in Seattle, homeowners are increasingly opting to invest in remodeling their current home instead of buying new properties (https://www.king5.com/article/money/markets/real-estate/seattle-home-renovation-housing-cooldown/281-71cb28a8-1bd5-4187-955f-debad072fe53). The demand for home renovators in Seattle has increased by 25% over the past 6 months.
* A home renovation company, (NAME), is moving into the Seattle area. As a new business in the city, they need to decide what types of services they should offer. They want to be able to provide their clients the most valuable renovations that will maximize their home's future sale value. Therefore, they hired us to share our recommendations on the best renovation services to offer homeowners.
Goal: to identify what types of renovation investments increase the sale value of home, we asked the following questions:
Business Question
Results: Describing the overall model metrics and feature coefficients You need at least one overall model metric (e.g. r-squared or RMSE) and at least two feature coefficients.* For a business audience, make sure you connect any metrics to real-world implications. You do not need to get into the details of how linear regression works. For a data science audience, you don't need to explain what a metric is, but make sure you explain why you chose that particular one.*

Definitions for our reference: https://www.bicconstruction.com.au/what-is-the-difference-between-a-home-renovationextensionaddition-new-build/

What types of home additions contribute to a higher sale price?
Multiple Linear Regression Model
Additions: Bedrooms, Bathrooms, Garage, Patio, Basement


For home expansions/extensions: which room size is most associated with higher sale price? For which room does size contribute the most to increased house sale price? (Increasing the size of which room is associated with higher prices?)

Multiple Linear Regression Model. Iterative model (R2 + 2 feature coefficients).
Start with sqft_living. Add in sqft_garage, sqft_patio, maybe sqft_yard? (sqft_lot - sqft_living)?


BONUS: 0. (Additional) If we have time, we could run a simple linear regression on grade. If significant it's an advertising treat for our clients
Rationale (rubric directions)
Rationale: Explaining why you are using statistical analyses rather than basic data analysis For example, why are you using regression coefficients rather than just a graph? What about the problem or data is suitable for this form of analysis?

Regression coefficients allow us to see how the different parts affect the whole
Each of these factors influence each other and change what their true value is.
This is where regression is useful: regression tells you how much each quality contributes to value– so you know what qualities to prioritize searching for in a potential investment.

Still need to answer: For a data science audience, this includes your reasoning for the changes you applied while iterating between models.

If we iterate through Model 1: gives us the opportunity to see how much each (additional) extension is worth.
Data Cleaning
Continuous Variables by removing outliers based on the z-score rule (z > 3)
Categorical Variables
We want to look at what the typical customer would request. Therefore:
We excluded Bedrooms/Bathrooms < 1 because not relevant to renovators
Filtered out Bedrooms > because:
few datapoints (outliers) and not our target audience (low number of each category = very rare to encounter in King County
Filtered out Bathrooms > 6 because: few datapoints (outliers) and not our target audience (low number of each category = very rare to encounter in King County
