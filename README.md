# Analyzing Credit Card Fraud: A Case Study of Transactions from 2019-2020

## Project Overview
This project investigates patterns and trends in credit card fraud using a simulated dataset of credit card transactions from January 2019 to December 2020. The dataset includes transactions from 1000 customers and 800 merchants, offering insights into fraudulent behavior, demographic influences, and regional trends. The analysis identifies key factors contributing to fraud detection and provides visualizations to illustrate findings.

The goal is to demonstrate data science skills, from preprocessing and analysis to effective visualization, while tackling a real-world problem with significant societal impact.

## Data Sources and Preparation
### Data Sources
The dataset was sourced from Kaggle. 

### Data Format
The dataset includes various fields such as transaction details, customer demographics, and merchant information. Key variables include `trans_date_trans_time`, `amount`, `gender`, `state`, `merchant`, and `category`.

## File and Folder Structure
- `code/`: Contains the RMarkdown file containing all code for data preparation, analysis, and visualization.
- `data/fraudTest.zip`: Directory where the dataset is stored. To use the dataset, download the folder and unzip it.
- `plots/`: Directory for saving output plots and visualizations (generated during execution).


### Preparation Steps
1. Verified the dataset for missing values and correct data types; no missing values were found.
2. Transformed the `trans_date_trans_time` field into a datetime format (`tr_datetime`) using `dmy_hm()`.
3. Converted the `dob` field into a date format (`DOB`) using `dmy()` to calculate customer age.
4. Created new variables for analysis, such as `hour`, `day`, `month`, `age_category`, and fraud summaries by gender, age, and state.
5. Filtered data to include only fraudulent transactions where needed for specific analyses.

Required R packages for preparation:
```r
install.packages(c("ggmap", "maps", "mapdata", "dplyr", "lubridate", "tidyverse"))
```

## Research Questions
1. How do demographics affect fraudulent credit card transactions?
2. Are there noticeable trends (hourly, monthly, seasonal) in fraudulent transactions?
3. Which U.S. states are most affected by credit card fraud?

## Explanation of Methods
### Analytical Approach
1. **Demographics Analysis**: Grouped and summarized fraudulent transactions by `age_category` and `gender`.
2. **Temporal Trends**: Extracted `hour`, `day`, and `month` from transaction timestamps to identify time-based patterns.
3. **Geographical Insights**: Used state-wise transaction data to compute fraud frequency, average fraud amount, and total fraudulent amounts. Integrated geographical data for visualization.

### Algorithms and Visualizations
- Employed grouping and summarization functions (e.g., `group_by()` and `summarize()`) in R to analyze trends.
- Visualized data using `ggplot2` for bar charts, line graphs, and geospatial heatmaps.
- Merged datasets with map data (`maps`, `mapdata`) for regional analysis.

## Code Execution
1. Download the dataset from Kaggle.
2. Clone or download this repository.
3. Run the `project_code.Rmd` file in RStudio.
4. Install required R packages if not already installed:
   ```r
   install.packages(c("ggmap", "maps", "mapdata", "dplyr", "lubridate", "tidyverse"))
   ```
5. Ensure the working directory includes the downloaded dataset. Modify file paths in the RMarkdown file if necessary.

## Why is the Project Useful?
Fraud detection is critical in safeguarding financial systems and protecting consumers. This project provides insights into the patterns of fraudulent behavior, enabling data-driven prevention strategies. By completing this project, users gain hands-on experience in preprocessing, analysis, and visualization—key skills in data science.

Additionally, the analysis raises awareness of ethical considerations in data usage and privacy, bridging technical capabilities with societal impact.


