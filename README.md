# YouTube Analytics Dashboard 📊

A comprehensive Streamlit-based analytics dashboard that transforms YouTube channel data into actionable insights, enabling content creators to track performance metrics, compare videos, and understand audience behavior.

## 🚀 Features

### 📈 Aggregated Metrics View
- **Key Performance Indicators**: Track views, likes, subscribers, shares, and comments
- **6-Month vs 12-Month Comparison**: See how your channel is trending
- **Engagement Metrics**: RPM, CPM, average view duration, and engagement ratios
- **Color-coded DataFrames**: Negative values in red, positive in green for easy spotting

### 🎥 Individual Video Analysis
- **Video Selector**: Choose any video for detailed analysis
- **Audience Breakdown**: View subscriber vs. non-subscriber performance by country
- **Performance Comparison**: Compare video performance against percentiles
- **30-Day Cumulative Views**: Track how your video performs in its first month

### 📊 Advanced Analytics
- **Engagement Ratio**: (Comments + Shares + Dislikes + Likes) / Views
- **Views per Subscriber Gained**: Measure subscriber acquisition efficiency
- **Percentile Comparisons**: 20th, 50th, and 80th percentile benchmarks
- **Country-wise Distribution**: See where your viewers come from

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/youtube-analytics-dashboard.git
cd youtube-analytics-dashboard
```

2. Install required packages:
```bash
pip install streamlit pandas numpy plotly openpyxl
```

3. Run the application:
```bash
streamlit run app.py
```

## 📋 Requirements

- Python 3.7+
- streamlit
- pandas
- numpy
- plotly
- openpyxl (for Excel file handling)

## 📊 Data Requirements

The dashboard expects three CSV files from YouTube Analytics:

### 1. Aggregated_Metrics_By_Video.csv
Contains video-level metrics including:
- Video title and publish time
- Views, likes, dislikes, comments
- Subscribers gained/lost
- RPM, CPM, revenue
- Average view duration
- Impressions and CTR

### 2. Aggregated_Metrics_By_Country_And_Subscriber_Status.csv
Demographic breakdown:
- Country-wise performance
- Subscriber vs. non-subscriber metrics

### 3. Video_Performance_Over_Time.csv
Daily performance data:
- Daily views by video
- Date-wise tracking
- Video-specific performance over time

## 🎯 How to Use

### Aggregated Metrics View
1. Select "Aggregated Metrics" from the sidebar
2. View KPI metrics with 6-month vs 12-month comparisons
3. Scroll through the color-coded dataframe showing video performance relative to median
4. Green = above median, Red = below median

### Individual Video Analysis
1. Select "Individual Video Analysis" from the sidebar
2. Choose a specific video from the dropdown
3. View the audience breakdown bar chart (subscribers vs. non-subscribers by country)
4. See the cumulative views comparison against percentiles for the first 30 days

## 🔍 Key Metrics Explained

| Metric | Description |
|--------|-------------|
| **RPM (USD)** | Revenue per thousand views |
| **CPM (USD)** | Cost per thousand impressions |
| **Average % viewed** | Percentage of video typically watched |
| **Engagement Ratio** | Interaction rate (comments+shares+likes+dislikes)/views |
| **Views / Sub gained** | Views needed to acquire one subscriber |
| **Avg_duration_sec** | Average watch time in seconds |

## 📈 Visualizations

### Audience Bar Chart
- Horizontal bar chart showing views by subscriber status
- Color-coded by country
- Helps identify which countries drive views from subscribers vs. non-subscribers

### Cumulative Views Comparison
- Line chart comparing video performance against percentiles
- 20th, 50th, and 80th percentile benchmarks
- First 30 days cumulative views tracking
- Instantly see if your video is above or below average

## 🎨 Styling Features

- **Negative values**: Displayed in red for quick problem identification
- **Positive values**: Displayed in green for success metrics
- **Percentage formatting**: All comparative metrics shown as percentages
- **Interactive charts**: Hover for details, zoom for closer inspection


## 🚦 Quick Start Guide

```python
# 1. Place your YouTube Analytics CSVs in the same directory
# 2. Run the app
streamlit run app.py

# 3. Navigate to http://localhost:8501
# 4. Start analyzing!
```

## 🔧 Customization Options

You can easily customize:
- Time periods (change 6/12 months in the code)
- Percentile thresholds (modify 20th/80th percentiles)
- Color schemes (update the style functions)
- Chart types (swap Plotly chart types)
