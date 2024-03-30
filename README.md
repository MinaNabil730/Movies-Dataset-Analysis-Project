# Movies Dataset Analysis Project

## Table of Contents

1. [Data Cleaning/Preparation](#data-cleaningpreparation)
2. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
    - [Q1: What genres are used the most?](#q1-what-genres-are-used-the-most)
    - [Q2: Which director made the most movies?](#q2-which-director-made-the-most-movies)
    - [Q3: Is the highest-rated movie of that director the highest-rated overall?](#q3-is-the-highest-rated-movie-of-that-director-the-highest-rated-overall)
    - [Q4: What is the most common year for releasing movies?](#q4-what-is-the-most-common-year-for-releasing-movies)
    - [Q5: Does the year with the most movie releases have the highest revenue?](#q5-does-the-year-with-the-most-movie-releases-have-the-highest-revenue)
    - [Q6: Is there a relationship between movie budget and votes?](#q6-is-there-a-relationship-between-movie-budget-and-votes)
    - [Q7: Is there a relationship between movie budget and revenue?](#q7-is-there-a-relationship-between-movie-budget-and-revenue)
3. [Results/Findings Summary](#resultsfindings-summary)
4. [Recommendations](#recommendations)
5. [Limitations](#limitations)



### 
This project conducts a comprehensive analysis of a movie dataset to uncover valuable insights into audience preferences, box office trends, and factors influencing success in the film industry. By employing data analytics techniques such as data cleaning, exploratory data analysis (EDA), and visualization, we aim to provide actionable insights for stakeholders in the movie industry.

**Data Source**
---------------

The dataset used in this project was provided by [Udacity](https://www.udacity.com/) as part of a task or assignment. You can access the dataset directly via this [link](https://video.udacity-data.com/topher/2022/November/6375a7af_tmdb-movies.csv/tmdb-movies.csv.zip). It contains information related to movies, including attributes such as IDs, popularity, budget, revenue, and more.


### **Tools Used**

#### **Programming Languages:**
- Python

#### **Libraries:**
- Pandas
- NumPy
- Matplotlib
- Seaborn

#### **IDE:**
- Jupyter Notebook

## Data Cleaning/Preparation {#data-cleaningpreparation}

1. **Dropped Useless Columns:**
   - After checking the columns, I found several columns that were not relevant to the analysis. I dropped these columns to streamline the dataset.

2. **Fixed NaN Values in Genres and Production Companies:**
   - I noticed NaN values in both the genres and production companies columns. To address this, I dropped the production companies column entirely and removed rows with NaN values in the genres column.

3. **Changed Data Types of Release Date and Release Year:**
   - The release_date and release_year columns were in the wrong data type (object) and should be datetime. I converted their data types to datetime for consistency and ease of analysis.

4. **Removed Duplicates:**
   - Upon inspection, I found a duplicate entry in the dataset. I removed this duplicate to ensure data integrity.

## Exploratory Data Analysis (EDA) {#exploratory-data-analysis-eda}

### Q1: What genres are used the most? {#q1-what-genres-are-used-the-most?}
- **Methodology**: I first split the rows containing multiple genres separated by "|" to have each genre on a single row. Then, I plotted the value counts of genres to identify the most frequently used genre.
- **Findings**: The most frequently used genre in the dataset was "Drama".

### Q2: Which director made the most movies? {#q2-which-director-made-the-most-movies?}
- **Methodology**: I used the `value_counts` function to determine which director made the most movies.
- **Findings**: The director who made the most movies was Woody Allen.

### Q3: Is the highest-rated movie of that director the highest-rated overall? {#q3-is-the-highest-rated-movie-of-that-director-the-highest-rated-overall?}
- **Methodology**: I aimed to see if the director who made the most movies had the highest-rated movie overall. To investigate, I compared the top-rated movie overall with the top-rated movie by Woody Allen.
- **Findings**: The top-rated movie overall had an average rating of 9.2, while the top-rated movie by Woody Allen had an average rating of 7.7. This suggests that the director with the most movies may not necessarily have the highest-rated movie overall.

### Q4: What is the most common year for releasing movies? {#q4-what-is-the-most-common-year-for-releasing-movies?}
- **Methodology**: I plotted the value counts of movie release years to determine the most common year for movie releases.
- **Findings**: The most common year for releasing movies was 2014.

### Q5: Does the year with the most movie releases have the highest revenue? {#q5-does-the-year-with-the-most-movie-releases-have-the-highest-revenue?}
- **Methodology**: I investigated if the year with the most movie releases (2014) had the highest revenue or if revenue depended on the number of movies released in a year.
- **Findings**: The year with the highest revenue was 2009, not 2014. This suggests that revenue does not necessarily depend on the number of movies released.

### Q6: Is there a relationship between movie budget and votes? {#q6-is-there-a-relationship-between-movie-budget-and-votes?}
- **Methodology**: I created a scatter plot to explore the relationship between movie votes and budgets. After removing outliers, I analyzed the scatter plot to identify any potential relationship.
- **Findings**: There was no clear relationship between movie votes and budgets, indicating that success is not solely determined by the budget.

### Q7: Is there a relationship between movie budget and revenue? {#q7-is-there-a-relationship-between-movie-budget-and-revenue?}
- **Methodology**: I created another scatter plot to investigate the relationship between movie budget and revenue. After removing outliers, I analyzed the scatter plot for any discernible patterns.
- **Findings**: Similar to the previous question, there was no clear relationship between movie budget and revenue. This suggests that profitability is not solely determined by budget, but also depends on creativity and other factors.

## Results/Findings Summary {#resultsfindings-summary}

### Key Findings:
- The most frequently used genre in the dataset was "Drama".
- Woody Allen was the director who made the most movies.
- The highest-rated movie overall had an average rating of 9.2, while the top-rated movie by Woody Allen had an average rating of 7.7.
- The most common year for releasing movies was 2014.
- The year with the highest revenue was 2009, not 2014, suggesting that revenue does not necessarily depend on the number of movies released.
- There was no clear relationship between movie budget and votes, indicating that success is not solely determined by the budget.
- Similarly, there was no clear relationship between movie budget and revenue, suggesting that profitability is not solely determined by budget.

## Recommendations {#recommendations}

Based on the findings of this analysis, the following recommendations are proposed for stakeholders in the movie industry:
1. Focus on producing more movies in the Drama genre, as it is the most frequently used genre.
2. Consider diversifying director choices beyond Woody Allen to explore new creative talents and potentially enhance overall movie ratings.
3. Explore the potential of releasing movies in less common years, as high revenue does not necessarily correlate with the most common release years.
4. Prioritize creativity and audience engagement over high budgets, as there is no clear relationship between budget and success in terms of votes or revenue.
5. Continuously monitor audience preferences and industry trends to adapt strategies and remain competitive in the ever-evolving movie market.

## Limitations {#limitations}

### Missing Data in `production_companies` Column
- One significant limitation encountered during the analysis was the presence of numerous NaN (missing) values in the `production_companies` column. These missing values prevented the exploration of questions related to production companies, such as identifying the most successful or wealthiest company in terms of budget or revenue. Additionally, the absence of data in this column hindered the analysis of the distribution of movies among production companies. Consequently, insights into the role and influence of production companies in the movie industry could not be fully explored.

