# 📊 Social Media Engagement Analysis

## 📌 Project Overview

This project analyzes **5,000 social media engagement records** using Python, Pandas, NumPy, Matplotlib, Seaborn, and Plotly.

The main objective is to clean the raw social media data, explore engagement patterns, perform statistical analysis, create visualizations, and identify useful insights about content performance and user behavior.

---

## 🎯 Objectives

* Import and clean social media data
* Handle missing and duplicate values
* Fix incorrect data types and formatting
* Standardize categorical values
* Clean likes, comments, and shares
* Extract hashtag count
* Clean sentiment labels
* Explore data using Pandas
* Perform statistical analysis
* Create new engagement-related features
* Build meaningful visualizations
* Identify important social media trends and insights

---

## 🗂️ Dataset

**Dataset:** `social_media_engagement_5000.csv`

The dataset contains social media post and user engagement information such as:

* Post Type
* Category
* Country
* Gender
* Age
* Likes
* Comments
* Shares
* Impressions
* Watch Time
* Engagement Rate
* Followers
* Sentiment
* Device
* Hashtags
* Date
* Verified Account

---

# 🛠️ Technologies & Libraries

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn
* Plotly

### Development Environment

* Google Colab
* GitHub

---

# 🔹 Task 1 — Data Import & Setup

The CSV dataset was imported using Pandas.

### Activities performed:

* Imported CSV file
* Checked dataset structure
* Checked column names
* Checked data types
* Converted date columns to datetime format

Example:

```python
df = pd.read_csv("social_media_engagement_5000.csv")

df.head()
```

---

# 🔹 Task 2 — Data Cleaning

## Missing Data

Missing values were identified using:

```python
df.isnull().sum()
```

Missing values were handled using appropriate methods such as:

* `dropna()`
* `fillna()`
* Median
* Mode
* Forward fill
* Backward fill

## Duplicate Handling

Duplicate records were identified and removed:

```python
df.duplicated().sum()

df = df.drop_duplicates()
```

## Data Formatting

The following data formatting tasks were performed:

* Corrected incorrect data types
* Standardized categorical values
* Cleaned gender labels
* Corrected unrealistic negative values in likes, comments, and shares

## Feature Cleaning

### Hashtag Count

A new feature called `hashtag_count` was created by counting hashtags in each post.

### Sentiment Cleaning

Sentiment labels were standardized into consistent categories such as:

* Positive
* Neutral
* Negative

---

# 🔹 Task 3 — Data Exploration

The dataset was explored using Pandas.

### Dataset Structure

Used:

```python
df.head()
df.tail()
df.shape
df.columns
```

### Data Information

```python
df.info()
df.dtypes
```

### Summary Statistics

```python
df.describe()
```

### Categorical Analysis

Used:

```python
df.value_counts()
df.unique()
df.nunique()
```

Categorical fields analyzed included:

* Post Type
* Category
* Country
* Gender
* Sentiment
* Device

### Correlation Analysis

A correlation matrix was created for numeric variables to understand relationships between engagement metrics.

### GroupBy Analysis

Examples:

* Average likes by post type
* Average engagement rate by country
* Average likes by category
* Average watch time by device

---

# 🔹 Task 4 — Data Wrangling

New features were created to support deeper analysis.

## Engagement Score

```python
df['engagement_score'] = (
    df['likes'] +
    df['comments'] +
    df['shares']
)
```

## Log Transformation

Log-transformed metrics were created for highly skewed engagement values.

```python
df['log_likes'] = np.log1p(df['likes'])
df['log_comments'] = np.log1p(df['comments'])
df['log_shares'] = np.log1p(df['shares'])
```

## GroupBy Analysis

Data was summarized by:

* Post Type
* Country
* Sentiment
* Category
* Device

---

# 🔹 Task 5 — Statistical Analysis

Descriptive statistics were calculated for:

* Likes
* Comments
* Shares
* Watch Time
* Engagement Rate
* Followers

The following statistical measures were calculated:

### Central Tendency

* Mean
* Median
* Mode

### Dispersion

* Standard Deviation
* Variance

### Percentiles

* 25th Percentile
* 50th Percentile
* 75th Percentile

### Additional Analysis

* Skewness
* Kurtosis

---

# 🔹 Task 6 — Data Visualization

Multiple visualizations were created to understand social media performance.

## Matplotlib

### 1. Scatter Plot

**Likes vs Impressions**

### 2. Line Chart

**Daily Engagement Trend**

### 3. Bar Chart

**Posts by Category**

### 4. Pie Chart

**Gender Distribution**

### 5. Histogram

**Age Distribution**

### 6. Box Plot

**Engagement Rate Distribution**

---

## Seaborn

### 7. Count Plot

**Post Type Distribution**

### 8. Bar Plot

**Average Likes by Category**

### 9. Violin Plot

**Followers vs Sentiment**

### 10. Pair Plot

**Numeric Feature Relationships**

### 11. Heatmap

**Correlation Matrix**

### 12. Swarm Plot

**Engagement Rate vs Device**

---

## Plotly

Interactive visualizations were created using Plotly, including:

* Interactive Line Chart
* Interactive Bar Chart
* Interactive Scatter/Bubble Chart

These visualizations allow users to explore the data interactively.

---

# 📈 Key Analysis Areas

## Content Performance

The analysis investigates:

* Which post types generate the highest engagement
* Which content categories perform best
* Which countries have the highest average engagement rate

## User Trends

The project analyzes:

* Relationship between age and engagement
* Performance difference between verified and non-verified accounts

## Behavioral Insights

The project examines:

* Best time of day for impressions
* Device type impact on watch time

## Sentiment Analysis

The project compares:

* Positive sentiment performance
* Neutral sentiment performance
* Negative sentiment performance

---

# 🔍 Key Insights

The analysis helps identify:

* High-performing content types
* High-performing content categories
* Countries with stronger engagement
* Age groups with higher engagement
* Impact of verified accounts
* Best posting time
* Device behavior
* Sentiment-based engagement patterns

> **Note:** Final insight values depend on the results obtained from the cleaned dataset.

---

# 📁 Project Structure

```text
Social-Media-Engagement-Analysis/
│
├── social_media_engagement_5000.csv
├── social_media_engagement_cleaned.csv
├── Social_Media_Engagement_Analysis.ipynb
└── README.md
```

---

# 🚀 Project Workflow

```text
Raw CSV Data
     ↓
Data Import
     ↓
Data Cleaning
     ↓
Data Formatting
     ↓
Feature Engineering
     ↓
Exploratory Data Analysis
     ↓
Statistical Analysis
     ↓
Data Visualization
     ↓
Business Insights
```

---

# 💡 Skills Demonstrated

* Python
* Pandas
* NumPy
* Data Cleaning
* Data Transformation
* Feature Engineering
* Exploratory Data Analysis (EDA)
* Statistical Analysis
* Data Visualization
* Matplotlib
* Seaborn
* Plotly
* GroupBy Analysis
* Correlation Analysis
* Business Insights

---

# 👨‍💻 Author

**Kesavaraj M**

Aspiring Data Analyst | Python | SQL | Excel | Power BI | Data Analytics

📍 Erode, Tamil Nadu, India

---

## ⭐ Project Outcome

This project demonstrates the complete **Data Analyst workflow**, from raw data cleaning and transformation to exploratory analysis, visualization, statistical analysis, and business insights.

It helped strengthen practical skills in **Python-based data analysis and visualization**.

