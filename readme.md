# **Can Attributes Predict Performance in Pro Cycling?**

---

This is a topic chosen for Project 2 on Regression, for the Metis Data Science Bootcamp - Summer 2020 Cohort.

## Context

Pro cycling is made up of mostly skinny Europeans. Is it possible to use cyclist profile data like age, build, nationality, etc. to predict performance?

## Goal

Predict performance of the world’s top pro cyclists, by category, using linear regression based on cyclist characteristics.

## Findings

In analyzing the top 1000 cyclists of each specialty, each specialty is hard to predict based on just height, weight, age, nationality, continent, and team.
Sprinters have the highest predictability, as they have the lowest variance in age, weight, and height. Climbers and time-trialists are more broad in those metrics and are much more difficult to predict.
Nationality, team, and continent do not suggest greater performance for pro cyclists despite ~80% of the pro cyclists in my data being European.
Every cyclist in the top 1000 pro cyclists is inherently an outlier, so to be able to draw reliable conclusions on the group is difficult.

# Methodology

## Gathering data:

Data on the 2019 top 1,000 male pro cyclists, per category, was scraped using Beautiful Soup from [Pro Cycling Stats](https://www.procyclingstats.com/).

Specific cyclist data was scraped via Beautiful Soup from each cyclist’s profile, using each cyclist’s link-stub found within the html code on the respective rankings pages.
Data frames were made from each cyclist rankings table, and also for each cyclist’s profile. These two data frames were then merged into one single data frame using each cyclist’s link stub.

## Cleaning data:

* Cyclists who had passed away during 2019 were removed from dataframe.
* BMI was calculated using listed height and weight data.
* Metric height and weight data was converted to imperial.
* Continent of origin was added for riders, assigned based on nationality.
* Numerical columns were converted to float and integer types.

## Exploring and modeling data:
R^2 was calculated for each cyclist specialty in tandem. The cyclist specialty that interacted best with my model was focused on for presentation.

# Deliverables

* [Full data and analysis](data_and_analysis)
  * [Part 1 - Data Scraping](data_and_analysis/Attributes_Predict_Performance_Cycling_-_Part_1_-_Data_Scraping.ipynb)
  * [Part 2 - EDA and Modeling](data_and_analysis/Attributes_Predict_Performance_Cycling_-_Part_2_-_EDA_and_Modeling.ipynb)
* Presentation Deck
  * [PDF version](presentation/Joseph_Grovers-Project_2-Attributes_Predict_Performance_Cycling.pdf.zip)
  * [Google Slides version](https://docs.google.com/presentation/d/1_Jh5HvSbAxy09nQUI18o1J3NmNuMYeSKHif12fRED7Y/edit?usp=sharing)
  * [PPT version](presentation/Joseph_Grovers-Project_2-Attributes_Predict_Performance_Cycling.pptx.zip)

### [Joseph Grovers GitHub](https://github.com/josephgrovers)

## Technologies Used

* Jupyter Notebook

* Python

* Pandas

* Matplotlib

* Seaborn

* BeautifulSoup

* SKLearn

* StatsModels

* Numpy

* Google Slides

## Presentation Materials Used

* Slidesgo - Template
* Flaticon - Icons
* Freepik - Infographics & images



