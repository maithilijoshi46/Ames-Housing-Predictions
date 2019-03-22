The Data Science Process - Maithili Joshi

**Problem Statement**

What features given the Aimes housing dataset


**Data Cleaning and EDA**
There is a lot of missing data. To being cleaning, I filtered and indexed all
columns that had at least 10% of the data missing from the data frame.

I created a list of the missing data:
Pool QC, Misc Feature, Alley, Fence, Fireplace Qu, Lot Frontage

I felt comfortable doing this because with that much missing data,
there wouldn't be a significant level of detail to perform any type of
feature engineering. I recognize that by doing so, I am making several
assumptions about the missing data, as well.


From there, I dropped the rest of the null values from my data frame, so that I
could begin EDA.

**Why I chose specific factors for the regression:


From the correlation matrix, I picked 15 factors that had a 0.45 and greater
correlation with sales price. These were:

Variable| Description| Type
----------------------------
'Garage Yr Blt' | Year the garage was built| Discrete
'TotRms AbvGrd' | Total rooms above ground| Discrete
'Mas Vnr Area' | Masonry Veneer Type | Nominal
'Full Bath' | Number of full baths | Discrete
"Year Remod/Add" | Year the home was remodeled| Discrete
'Year Built' | Year the House was built | Discrete
'1st Flr SF' | Square footage of the first floor | Continuous
'Total Bsmt SF' | Square footage of the basement | Continuous
'Fireplaces' | Number of basements | Discrete
'Garage Cars' | Size of garage in car capacity| Discrete
'Garage Area' | Size of Garage in Square Feet | Continuous
'Gr Liv Area' | Above ground living area square feet | Continuous
'Total Sqft' | Overall square foot of house | Continuous
'Overall Qual' | Overall quality of house | Ordinal
'BsmtFin SF 1' | Type 1 finished Square Feet| Continuous

**Modeling**

I chose to use a linear regression with Lasso.
My cross val score before scaling was 83%
My cross val score after scaling was 85%.

This indicates to me that my model is pretty accurate, with 85% of the variance being modeled properly.

Outside Research:
(https://www.opendoor.com/w/blog/factors-that-influence-home-value)

Based on outside research, there are 8 factors that indicate higher sales prices
for a house. From this, I looked at economic indicators nationally and in the US to make a conclusion! 
