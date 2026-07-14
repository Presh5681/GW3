California Housing: Digging into the Data 🏡

This repository is a clean, straightforward dive into the classic California Housing dataset. Before jumping headfirst into machine learning models, I wanted to get my hands dirty inspecting the data, hunting down outliers, and seeing how the features actually interact with one another.

🛠️ The Toolkit

Nothing overly fancy here—just the trusty Python scientific stack doing what it does best:
Pandas & NumPy for data wrangling and numerical operations.Scikit-Learn to fetch the dataset.
Matplotlib & Seaborn to make the visualizations look clean and readable.

📋 What I Did

I broke the analysis down into three main steps:Data Check: Loaded up the 20,640 rows, verified there weren't any missing values (spoiler: it's perfectly clean!), and made sure the data types were correct
The Outlier Hunt: Used the Interquartile Range (IQR) method to flag extreme values across the variables.Visualizing Relationships: Plotted the distribution of home values and whipped up a correlation heatmap to see what actually drives housing prices.

💡 The Cool Stuff I Found
1. The Outliers are Telling a StoryUsing the standard $1.5 \times \text{IQR}$ rule, a few variables really stood out:Average Bedrooms (AveBedrms - 1,424 outliers):
There is massive variation here. Some blocks have massive homes, while others are much more modest.Population (Population - 1,196 outliers): This highlights the contrast between California's highly dense urban pockets and its sprawling rural areas.The Price Cap (MedHouseVal - 1,071 outliers): Heads up—the median house value is capped at $5.0$ (which represents $500,000). You'll see a big, artificial spike right at the edge of the distribution plot because of this capping.
2. Key Correlations
3. Income is King: Unsurprisingly, median income (MedInc) has a massive positive correlation of ~0.69 with house values. If the neighborhood makes more, the houses cost more
4. .Geography Rules: Latitude and longitude have a strong negative correlation of -0.92. This simply traces the natural diagonal slope of California's coastline.Room to Bedroom Ratio: The number of total rooms and bedrooms are super tightly coupled (0.85 correlation), which makes complete sense structurally.
