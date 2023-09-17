# Automatidata_project
# Project Goal
This project represents that the New York City Taxi and Limousine Commission (TLC) has approached the data consulting firm Automatidata to develop an app that enables TLC riders to estimate the taxi fares in advance of their ride.

# Automatidata - Google Data Analytics Project
Table of Contents
-----------------
1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Project Structure](#project-structure)
4. [Project Goals](#project-goals)
5. [Data Used](#data-used)
6. [Methods and Tools](#methods-and-tools)
7. [Data Analysis Steps](#data-analysis-steps)
8. [Results and Insights](#results-and-insights)
9. [Data Visualizations](#data-visualizations)
10. [Challenges Faced](#challenges-faced)
11. [Future Work](#future-work)
12. [Installation](#installation)
13. [Usage](#usage)
14. [Contributing](#contributing)
15. [License](#license)
16. [Acknowledgments](#acknowledgments)
17. [Contact Information](#contact-information)
18. [References](#references)

## Introduction
# Background on the Automatidata scenario
Automatidata works with its clients to transform their unused and stored data into useful solutions, such as performance dashboards, customer-facing tools, strategic business insights, and more. They specialize in identifying a client’s business needs and utilizing their data to meet those business needs. 

Automatidata is consulting for the New York City Taxi and Limousine Commission (TLC). New York City TLC is an agency responsible for licensing and regulating New York City's taxi cabs and for-hire vehicles. The agency has partnered with Automatidata to develop a regression model that helps estimate taxi fares before the ride, based on data that TLC has gathered. 

The TLC data comes from over 200,000 taxi and limousine licensees, making approximately one million combined trips per day. 

## Project Overview

The New York City Taxi and Limousine Commission seeks a way to utilize the data collected
from the New York City area to predict the length of rides and fares.


## Project Structure

[Explain the structure of your project, including directories and files.]

## Project Goals
# Project Goal
This project represents that the New York City Taxi and Limousine Commission (TLC) has approached the data consulting firm Automatidata to develop an app that enables TLC riders to estimate the taxi fares in advance of their ride.

## Data Used

This project uses a dataset called 2017_Yellow_Taxi_Trip_Data.
**Data Source:**
You can access the dataset used in this project [here](https://www.nyc.gov/site/tlc/about/data.page#).
The data consisted of approximately 408k unique trips and 18 features. The features included information on trip duration and destination, vendor used, toll information, and payment type.

## Methods and Tools

This project contains the 2017_Yellow_Taxi_Trip_Data set, Python notebook, PACE framework, Tableau and input from stakeholders.


## Data Analysis Steps

## Data Analysis Steps

1. **Data Collection**: Gathered relevant datasets provided in the Google Data Analytics course.

2. **Data Preprocessing**: Cleaned and standardized the data, handling missing values and outliers.

3. **Exploratory Data Analysis (EDA)**: Explored data, generated visualizations, and identified patterns.

4. **Data Transformation**: Engineered features and applied necessary transformations.

5. **Modeling**: Built machine learning and statistical models.

6. **Model Evaluation**: Assessed model performance using cross-validation and metrics.

7. **Data Visualization**: Created informative charts and graphs.

8. **Interpretation**: Extracted insights and conclusions from the analysis.

9. **Reporting**: Documented the process and results for reference.

These steps summarize the data analysis workflow in the "Automatidata" project.


## Results and Insights

At the end of this project we get these insights from our model.
1. **Would you recommend using this model? Why or why not?**  
Yes, this is model performs acceptably. Its F<sub>1</sub> score was 0.7235 and it had an overall accuracy of 0.6865. It correctly identified ~78% of the actual responders in the test set, which is 48% better than a random guess. It may be worthwhile to test the model with a select group of taxi drivers to get feedback.

2. **What was your highest scoring model doing? Can you explain how it was making predictions?**   
Unfortunately, random forest is not the most transparent machine learning algorithm. We know that `VendorID`, `predicted_fare`, `mean_duration`, and `mean_distance` are the most important features, but we don't know how they influence tipping. This would require further exploration. It is interesting that `VendorID` is the most predictive feature. This seems to indicate that one of the two vendors tends to attract more generous customers. It may be worth performing statistical tests on the different vendors to examine this further.

3. **Are there new features that you can engineer that might improve model performance?**   
There are almost always additional features that can be engineered, but hopefully the most obvious ones were generated during the first round of modeling. In our case, we could try creating three new columns that indicate if the trip distance is short, medium, or far. We could also engineer a column that gives a ratio that represents (the amount of money from the fare amount to the nearest higher multiple of $5) / fare amount. For example, if the fare were \\$12, the value in this column would be 0.25, because \\$12 to the nearest higher multiple of \\$5 (\\$15) is \\$3, and \\$3 divided by \\$12 is 0.25. The intuition for this feature is that people might be likely to simply round up their tip, so journeys with fares with values just under a multiple of \\$5 may have lower tip percentages than those with fare values just over a multiple of \\$5. We could also do the same thing for fares to the nearest \\$10.


## Data Visualizations

[Include any data visualizations you created.]

## Challenges Faced

[Discuss any challenges or obstacles you encountered during the project.]

## Future Work

As a next step, the Automatidata data team can consult the New York City Taxi and Limousine commission to share the model results and recommend that the model could be used as an indicator of tip amount. However, additional data would be needed to realize significant improvement to the model.


## Installation

[Explain any setup or installation requirements.]

## Usage

[Provide instructions on how to use your project.]

## Contributing

[Encourage contributions and provide guidelines for contributors.]

## License

[Specify the license under which your project is shared.]

## Acknowledgments

[Give credit to sources that contributed to your project.]

## Contact Information

[Provide contact information for inquiries.]

## References

[Include references or citations to external sources.]
