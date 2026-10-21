# SpaceX Falcon 9 First Stage Landing Prediction – IBM Applied Data Science Capstone

**Author:** Paul Togbe Yao

Goal: predict whether the Falcon 9 first stage will land successfully. A successful landing makes a launch much cheaper ($62M for SpaceX vs. $165M+ for other providers), so this prediction helps estimate launch costs.

## Notebooks and files

| # | File | Content |
|---|------|---------|
| 1 | `1_jupyter-labs-spacex-data-collection-api.ipynb` | Data collection with the SpaceX REST API (GET requests, `json_normalize`, Falcon 9 filter, missing values) |
| 2 | `2_jupyter-labs-webscraping.ipynb` | Web scraping of the Wikipedia Falcon 9 launch list with BeautifulSoup (121 records) |
| 3 | `3_labs-jupyter-spacex-Data_wrangling.ipynb` | Data wrangling and landing-outcome label `Class` (success rate 66.7%) |
| 4 | `4_jupyter-labs-eda-sql.ipynb` | Exploratory data analysis with SQL (10 queries) |
| 5 | `5_jupyter-labs-eda-dataviz.ipynb` | Exploratory data analysis with visualizations and feature engineering (one-hot encoding) |
| 6 | `6_lab_jupyter_launch_site_location.ipynb` | Interactive map with Folium (launch sites, marker clusters, distances) |
| 7 | `7_spacex_dash_app.py` | Plotly Dash dashboard (site dropdown, pie chart, payload slider, scatter chart) |
| 8 | `8_SpaceX_Machine_Learning_Prediction_Part_5.ipynb` | Machine learning: Logistic Regression, SVM, Decision Tree, KNN with GridSearchCV |
| – | `data/` | Datasets used (IBM Skills Network) |

## Key results
- 90 Falcon 9 launches; overall landing success rate **66.7%**, rising to 84–90% in 2019–2020
- Best launch site: **KSC LC-39A** (76.9% success)
- Orbits ES-L1, GEO, HEO, SSO: 100% success; GTO: 52%
- All models reach **83.3%** test accuracy; the **Decision Tree** has the best validation accuracy (**87.5%**)

## Run the dashboard
```bash
pip install pandas dash plotly
python 7_spacex_dash_app.py
```
