# YouTube Trending Video Analytics

## Global Content, Engagement & Sentiment Analysis

Data analytics project analyzing YouTube trending videos across five countries using Python, NLP, SQL, and Power BI.

---

## 📌 Project Overview

This project analyzes YouTube trending video data from:

- 🇮🇳 India
- 🇺🇸 United States
- 🇩🇪 Germany
- 🇬🇧 Great Britain
- 🇲🇽 Mexico

The goal is to understand which types of content trend the most, how video performance differs between countries, how long videos remain trending, and whether title/tag sentiment is associated with video performance.

The project combines data cleaning, exploratory analysis, multilingual sentiment analysis, SQL analysis, and interactive Power BI visualization.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze popular YouTube content categories.
- Compare video performance across countries.
- Examine views, likes, and comments.
- Analyze how long videos remain on the trending list.
- Perform sentiment analysis on video titles and tags.
- Compare sentiment distributions across countries.
- Study the relationship between sentiment and video views.
- Build an interactive Power BI dashboard.

---

## 🗂️ Dataset

The project combines YouTube trending datasets from five countries.

### Final dataset

- Original records: **198,508**
- Exact duplicate records removed: **4,531**
- Final records: **193,977**
- Unique valid video IDs: **84,090**
- Categories: **18**

The final dataset contains information such as:

- Video ID
- Country
- Category
- Trending date
- Publish time
- Views
- Likes
- Dislikes
- Comments
- Title
- Tags
- Sentiment
- Sentiment confidence
- Video status fields

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Hugging Face Transformers**
- **XLM-RoBERTa**
- **SQLite / SQL**
- **Power BI Desktop**
- **Excel**
- **Google Colab**

---

## 🔄 Project Workflow

### 1. Data Collection & Combination

YouTube trending datasets from the five selected countries were loaded into Google Colab and combined into a single dataset.

### 2. Data Cleaning

The data was cleaned by:

- Removing exact duplicate rows.
- Handling corrupted video IDs.
- Converting date columns to appropriate datetime formats.
- Validating numerical engagement fields.
- Mapping category IDs to category names.
- Cleaning titles and tags.
- Checking missing values and inconsistent records.

### 3. Sentiment Analysis

Because the dataset contains multilingual content, a multilingual transformer model was used:

**cardiffnlp/twitter-xlm-roberta-base-sentiment**

Sentiment was analyzed using video titles and tags.

The final sentiment categories were:

- Positive
- Neutral
- Negative

The sentiment model's score was treated as model confidence rather than sentiment intensity.

### 4. SQL Analysis

SQLite was used to perform analytical queries including:

- Average views by category.
- Country and category performance.
- Trending duration of videos.
- Country-level trending duration.
- Monthly unique trending videos.
- Views by sentiment and country.

### 5. Power BI Dashboard

The cleaned dataset was imported into Power BI to create an interactive four-page dashboard.

#### Executive Overview
Provides an overall view of:

- Total views
- Total likes
- Total comments
- Video records
- Views by category
- Views by country
- Trending activity over time

#### Category Analysis
Compares categories using:

- Average views
- Video records
- Average likes
- Average comments

#### Regional Analysis
Compares the five countries using:

- Total views
- Video records
- Average views
- Average trending days

#### Sentiment & Trends
Analyzes:

- Sentiment distribution by country
- Average views by sentiment
- Sentiment trends over time

---

## 📊 Key Findings

### Category Performance

Music recorded the highest average views among categories with substantial numbers of records.

Categories with very small sample sizes, such as Movies and Trailers, were treated cautiously when comparing average performance.

### Regional Performance

Great Britain showed the highest average trending duration among videos that appeared on the trending list at least twice.

The United States also showed relatively high average trending duration compared with the other countries.

### Sentiment

The overall sentiment distribution was:

| Sentiment | Records |
|---|---:|
| Neutral | 168,316 |
| Negative | 17,232 |
| Positive | 8,429 |

Neutral sentiment represented the majority of records.

Neutral videos also had the highest average views in each of the five countries. This represents an observed association in the dataset and does not establish causation.
