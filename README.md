# GooglePlay Apps - Analysis
## Using Panda

As of May 2022, there are more than 3.3 million Android apps on GooglePlay store.  Contrast this with iOS, which has 2.2 million apps on the App Store. There are 2.2 billion android users worldwide and commands 72% Mobile OS marketshare! Currently, about 4000 new apps are getting added to GooglePlay store every day, and the numbers are still moving north!

So let's explore the Apps and Games in GooglePlay store and anazlye the chracterstics of the most popular ones in the list.

> Problem Definition - As the GooglePlay store is crowded with so many Apps and Games, can we study the underlying trends and surcafe out some winning characteristics that makes them successful?


## Step 1: Select dataset: Android Apps from GooglePlay Store and User Reviews

This dataset is obtained from scraping Google Play Store in April 2020.

Source: https://www.kaggle.com/datasets/tungmphung/new-google-play-store-android-apps-dataset

#### Contents: 
2 csv files:
1. app.csv with 53,732 rows and 18 columns.
2. comment.csv with 1,468,173 rows and 4 columns.


#### App: Column description
- id: a unique identifier for each app.
- app_name.
- genre (a.k.a category).
- rating.
- reviews: the number of reviews.
- cost_label: If the app is free, the cost_label value is ‘Install‘. If the app is premium, the cost_label value is the price, e.g. ‘đ23,000 Buy‘, ‘đ69,000 Buy‘. 
    - Note - that the currency is in Vietnam dong. At the current time, đ23,000 \approx 1$.
- rate_5_pc, …, rate_1_pc: the percentage of user ratings that vote 5-stars, …, 1-star.
- updated: The date that the app was last updated on the Play Store.
- size: app size.
- installs: the number of installs (or downloads).
- current_version: the current version of the app.
- requires_android: the Android version required for the app to run.
- content_rating: age restriction.
- in_app_products: cost of items in the app.
- offered_by: the developer or team that designed the app.


#### Comment: Column description
- app_id: the id of the app the comment belongs to.
- content: comment’s content, might be truncated if too long.
    - Note that not all comments are recorded. Comments are sorted by relevance and at most 40 most relevant comments are recorded for each app.
- stars: the user rating that is attached to the comment.
- helpfuls: the number of users who found this comment helpful.


## Step 2: Perform data preparation & cleaning
1. Read the CSV files and convert into dataframe using Pandas
2. Handle missing, incorrect and invalid data
3. Data wrangling


## Step 3: Perform exploratory analysis & visualization
1. Compute the mean, sum, range and other interesting statistics for numeric columns
2. Explore relationship between columns using scatter plots, bar charts etc.
3. Make a note of interesting insights from the exploratory analysis

## Step 4: Ask & answer questions about the data
- Frame some nteresting questions about your dataset
- Answer the questions either by computing the results using Numpy/Pandas or by plotting graphs using Matplotlib/Seaborn/Plotly/Folium
- Create new columns, merge multiple dataset and perform grouping/aggregation wherever necessary
- For each question, summarize the key insight from the analysis or visualization in simple words
