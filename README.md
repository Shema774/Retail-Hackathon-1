# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

##  Dataset Content
For this project, I worked with three core datasets:
- Features_data_set.csv – Store-level attributes, including promotional events and holiday indicators.
- Sales_data.csv – Historical weekly sales data across various departments.
- Stores_data.csv – Store metadata such as size and type classification.
Each dataset was structured with appropriate indexing, cleaned for missing values, and transformed to ensure consistency for analysis.

 Business Requirements
The objective of this analysis was to uncover trends in retail sales performance while optimizing key business metrics. Detect seasonal or promotional impacts on weekly sales.
 Compare store types (A, B, C) and performance differences.
Assess feature scaling for standardizing store size comparisons.


Hypothesis and Validation Strategy
Hypothesis 1: Holiday promotions significantly influence sales trends.
Validation: Compare holiday vs. non-holiday sales distributions using boxplots and statistical analysis.
Hypothesis 2: Larger stores tend to generate higher revenue.
Validation: Normalize Size using MinMaxScaler, then correlate store size with total sales via scatter plots.
Hypothesis 3: Promotional events create measurable spikes in weekly sales.
Validation: Overlay event occurrences on sales trend charts to measure impact.

Project Plan & Data Management
ETL Workflow
 Extract: Read raw datasets and verify their structure.
 Transform: Apply data cleaning techniques (handling null values, duplicate removal, feature scaling).
 Load: Store processed datasets in an organized folder structure for further visualization.
 Data Processing: Pandas for manipulation, Scikit-learn for feature scaling.
 Storage: CSV format in the processed/ directory for seamless loading.
Analysis: Matplotlib, Seaborn, and Plotly for visualization.

Mapping Business Requirements to Visualizations
| Requirement | Visual Technique | 
| Holiday impact on sales | Boxplot (sns.boxplot()) | 
| Store performance | Scatter plot (px.scatter()) | 
| Weekly sales trends | Line chart (px.line()) | 
| Feature scaling impact | Histogram (sns.histplot()) | 


Analysis Techniques Used
Correlation Analysis – Measured relationships between store attributes and sales.
Time-Series Trends – Visualized fluctuations in sales over time.
Feature Engineering – Applied scaling methods to normalize store size differences.
Challenge: Some feature scaling approaches produced biased results. The solution was to test multiple methods (StandardScaler vs. MinMaxScaler) before settling on the optimal approach.

Use of AI for Ideation & Code Optimization
Generative AI tools helped refine my approach in various ways:
Suggested best practices for handling missing values in datasets.
Provided alternative visualization techniques for readability improvements.
Assisted in debugging dependency conflicts with Pandas, Plotly and Seaborn installations.

Ethical Considerations
- Bias in promotional events: Some sales spikes were due to region-specific campaigns, requiring careful contextual interpretation.
- Data privacy: Ensured no personally identifiable information was included in analysis.
- Fairness in comparisons: Normalized store sizes to prevent skewed interpretations.

Unfixed Bugs & Framework Limitations
 Challenges Encountered
Issue: FileNotFoundError due to incorrect dataset paths.
Solution: Used os.path.exists() and adjusted working directories.
Issue: Overlapping x-axis labels in time-series plots.
Solution: Applied plt.xticks(rotation=45) for better readability.
Unfixed Bugs
While most bugs were resolved, some framework-specific limitations remained:
- Plotly sometimes misaligned date labels under certain zoom settings.
- Large datasets caused memory overflow issues in Jupyter Notebook during high-resolution plotting.

Development Roadmap
Implemented automated data pipeline for seamless ETL processing.
Built modularized notebooks for easy debugging.
Next Steps: Expand analysis with predictive modeling using Scikit-learn’s regression techniques.

Data Analysis Libraries Used
| Library | Usage Example | 
| Pandas | Data cleaning (df.dropna()) | 
| NumPy | Mathematical computations (np.mean()) | 
| Matplotlib | Static charts (plt.plot()) | 
| Seaborn | Statistical visualizations (sns.boxplot()) | 
| Plotly | Interactive dashboards (px.scatter()) | 



## Credits & References
 Data sources curated from Kaggle and open retail datasets.
 Visualization insights refined using examples from Seaborn Docs and Plotly Guide.
 Tutorials referenced for debugging GitHub workflows and deployment strategies.

## Acknowledgements
A huge thanks to peers who provided valuable feedback, helping to refine methodology and improve visualization clarity.


