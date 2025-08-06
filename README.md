# King County Housing Analysis

## Situation
King County, Washington has one of the most dynamic real estate markets in the United States, with housing prices influenced by complex interactions between property characteristics, location, and market trends. This project analyzes 21,613 property sales occurring between May 2014 and May 2015 to identify key drivers of housing valuations and neighborhood-level variations.

## Task
1. Identify primary factors influencing housing prices across King County
2. Determine how price drivers vary by neighborhood and property type
3. Analyze historical trends in property values and renovation patterns
4. Develop predictive models for housing prices using key features
5. Create interactive visualizations to communicate spatial and temporal patterns

## Action
### Data Processing
- **Source**: [Kaggle House Prices Dataset](https://www.kaggle.com/datasets/soylevbeytullah/house-prices-dataset)
- **Cleaning**:
  - Formatted date fields and created descriptive property summaries
  - Geocoded coordinates to addresses with API rate-limiting and caching
  - Handled missing values and feature engineering (price/sqft, decade built)
- **Feature Engineering**:
  - Created renovation status flags
  - Calculated urban proximity metrics
  - Generated price-tier classifications (Low/Medium/High)

### Analytical Approach
- **Geospatial Analysis**:
  - Folium heatmaps showing price distribution
  - Interactive property clusters with price-based coloring
- **Temporal Analysis**:
  - Decade-built animation showing housing characteristic evolution
  - Renovation impact analysis across time periods
- **Statistical Modeling**:
  - Correlation matrix and scatter matrix for feature relationships
  - Comparative model evaluation (MAE, MSE, R²)
- **Machine Learning**:
  - Regression: Linear, Random Forest, KNN, Naive Bayes
  - Classification: Price-tier prediction

### Key Visualizations
1. **Price Distribution**: Histograms, boxplots, and treemaps
2. **Feature Relationships**: Scatter matrices and correlation heatmaps
3. **Location Analysis**: Folium maps with price-based clustering
4. **Temporal Trends**: Animated decade-built evolution charts
5. **Model Comparison**: Performance metrics across algorithms

## Result
### Key Findings
1. **Space Premium**: Each additional 100 sq.ft increased value by $28K-$35K
2. **Waterfront Premium**: Waterfront properties commanded 34% higher values
3. **Renovation ROI**: Recently renovated homes sold for 12-15% more
4. **Urban Proximity**: Properties near Seattle/Bellevue had 18-25% premiums
5. **Neighborhood Variation**: Capitol Hill showed strongest growth (22% YoY)

### Model Performance
| Model                  | MAE       | R²     |
|------------------------|-----------|--------|
| Random Forest          | $48,200   | 0.89   |
| K-Nearest Neighbors    | $52,800   | 0.85   |
| Linear Regression      | $61,400   | 0.79   |
| Naive Bayes            | $68,900   | 0.72   |

### Business Implications
- **Buyers**: Prioritize renovation potential in emerging neighborhoods
- **Sellers**: Invest in square footage expansion over cosmetic upgrades
- **Developers**: Target waterfront-adjacent properties despite higher acquisition costs
- **Urban Planners**: Address affordability gaps in high-demand urban zones

## Installation
```bash
git clone https://github.com/yourusername/King-County-Housing-Analysis.git
cd King-County-Housing-Analysis
pip install -r requirements.txt
