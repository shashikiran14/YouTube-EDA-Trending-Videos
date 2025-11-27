# YouTube EDA: US Trending Videos Analysis

## 📘 Project Overview

This repository contains a comprehensive **Exploratory Data Analysis (EDA)** of US YouTube trending videos dataset. The project aims to uncover patterns, trends, and insights that influence video virality on YouTube.

### Objectives
1. **Data Loading & Preparation** - Import and understand the dataset structure
2. **Feature Engineering** - Extract temporal and categorical features
3. **Data Cleaning** - Handle missing values and outliers
4. **Statistical Analysis** - Compute descriptive statistics and correlations
5. **Visual Analysis** - Create insightful visualizations and word clouds
6. **Trend Identification** - Identify key factors in trending videos
7. **Documentation** - Summarize findings and insights

---

## 📊 Dataset Information

- **Total Records**: 35,299 US YouTube trending videos
- **Source**: US YouTube Trending Videos dataset
- **Key Columns**:
  - `video_id` - Unique video identifier
  - `title` - Video title
  - `channel_title` - Channel name
  - `publish_time` - Publication timestamp
  - `trending_date` - When video trended
  - `views` - Total views count
  - `likes` - Total likes count
  - `dislikes` - Total dislikes count (when available)
  - `comment_count` - Total comments
  - `category_id` - Video category
  - `comments_disabled` - Boolean flag
  - `ratings_disabled` - Boolean flag

---

## 🛠️ Technologies & Libraries

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Matplotlib** - Static visualizations
- **Seaborn** - Statistical visualizations
- **WordCloud** - Text visualization
- **Jupyter Notebook** - Interactive analysis environment

---

## 📁 Project Structure

```
YouTube-EDA-Trending-Videos/
├── README.md                 # Project documentation
├── .gitignore               # Git ignore file (Python)
├── UsVideos.ipynb          # Main analysis notebook
├── notebooks/              # Additional notebooks (if any)
├── data/                   # Dataset files
│   └── USvideos.csv       # Main dataset
├── outputs/                # Generated visualizations & reports
└── docs/                   # Additional documentation
```

---

## 🔍 Analysis Performed

### Step 1: Data Import & Exploration
- Loaded CSV dataset into Pandas DataFrame
- Examined dataset shape, data types, and missing values
- Dropped non-essential columns (thumbnail_link, description, video_error_or_removed)

### Step 2: Feature Engineering
- Converted datetime columns with proper error handling
- Extracted temporal features:
  - `publish_day` - Day of week when published
  - `publish_hour` - Hour of publication
  - `trending_day` - Day of week when trended
- Calculated `days_to_trend` - Time from publication to trending
- Handled timezone conversions for accurate time difference calculations

### Step 3: Data Cleaning
- Removed rows with critical null values
- Validated data integrity after transformations
- Final dataset: 35,299 records with 14 columns

### Step 4: Statistical Analysis
- Computed descriptive statistics for all columns
- Analyzed distribution of views, likes, dislikes, and comments
- Identified outliers and data anomalies

### Step 5: Visual Analysis
- **Top Trending Channels** - Bar chart of channels with most trending videos
- **Likes vs Dislikes** - Scatter plot with log scale to show correlation
- **Feature Correlation** - Heatmap showing relationships between numeric features
- **Word Cloud** - Most frequent words in video titles
- **Days to Trend Distribution** - Histogram showing time taken to trend
- **Disabled Content Analysis** - Videos with disabled comments/ratings

### Step 6: Key Findings
- Top channels frequently appear in trending list
- Most videos published during mid-day to evening hours
- Strong positive correlation between likes and dislikes
- Majority of videos trend within 0-3 days of publication
- Some content creators disable ratings and comments

---

## 📈 Key Insights

1. **Channel Dominance**: Certain channels consistently appear in trending lists
2. **Publishing Patterns**: Optimal publishing times correlate with higher views
3. **Engagement Metrics**: Likes and dislikes show strong correlation (0.98+)
4. **Time to Trend**: Most videos achieve trending status within 3 days
5. **Content Strategy**: Title keywords influence virality
6. **Comments/Ratings**: Small percentage of videos disable engagement metrics

---

## 🚀 How to Use

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn wordcloud jupyter
```

### Running the Analysis
1. Clone the repository
   ```bash
   git clone https://github.com/shashikiran14/YouTube-EDA-Trending-Videos.git
   cd YouTube-EDA-Trending-Videos
   ```

2. Place the dataset in the `/data/` directory
   ```bash
   # Ensure USvideos.csv is in the data folder
   ```

3. Open Jupyter Notebook
   ```bash
   jupyter notebook UsVideos.ipynb
   ```

4. Run all cells to generate analysis and visualizations

---

## 📊 Output Files

After running the notebook, the following are generated:
- Statistical summaries
- Visualization plots (PNG format)
- Data-driven insights document
- Cleaned dataset (if exported)

---

## 👥 Author Information

**Project By**: Mubashir Bilal & Kuruva Shashi Kiran  
**Course**: AI/ML SIT2025  
**Internship**: The Web Blinders × The Wisdom Wells  
**Date**: June 18, 2025

---

## 📝 License

This project is open source and available for educational and research purposes.

---

## 🔗 Related Resources

- [Pandas Documentation](https://pandas.pydata.org/)
- [Matplotlib Guide](https://matplotlib.org/)
- [Seaborn Tutorial](https://seaborn.pydata.org/)
- [YouTube API Documentation](https://developers.google.com/youtube/v3)

---

## 📧 Questions or Feedback?

Feel free to open an issue or reach out through GitHub.

---

**Status**: ✅ EDA Complete  
**Last Updated**: November 27, 2025
