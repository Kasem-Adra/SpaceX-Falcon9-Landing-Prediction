# SpaceX Falcon 9 Landing Prediction

A data science project by [Kasem Adra](https://github.com/Kasem-Adra) exploring Falcon 9 launch data and predicting first-stage landing outcomes.

| Step | Notebook |
| --- | --- |
| API data collection | [01 — Data collection](01_Data_Collection_API.ipynb) |
| Web scraping | [02 — Web scraping](02_Web_Scraping.ipynb) |
| Data preparation | [03 — Data wrangling](03_Data_Wrangling.ipynb) |
| SQL analysis | [04 — EDA with SQL](04_EDA_SQL.ipynb) |
| Exploratory charts | [05 — EDA visualization](05_EDA_Visualization.ipynb) |
| Launch-site map | [06 — Folium map](06_Folium_Map.ipynb) |
| Interactive dashboard | [07 — Plotly Dash](07_Plotly_Dash.ipynb) |
| Landing-outcome classification | [08 — Machine learning](08_Machine_Learning.ipynb) |

## Reproduce the workflow

Create a Python virtual environment, then install the notebook runtime and imported packages:

```sh
python -m pip install jupyterlab requests pandas numpy beautifulsoup4 sqlalchemy matplotlib seaborn folium dash plotly scikit-learn
python -m jupyter lab
```

Run notebooks from this directory. Notebook 01 fetches launch data and writes `dataset_part_1.csv`. Notebook 02 is a separate Wikipedia scraping exercise and writes `spacex_web_scraped.csv`. Notebook 03 reads the first CSV and writes `dataset_part_2.csv`, which notebooks 04–08 consume. Notebook 07 starts an interactive Dash server.

As a smoke check, run notebooks 01–06 and 08 in clean kernels, confirm both pipeline CSVs are created, and inspect the final classifier output. Run the Dash notebook interactively. The repository does not ship pinned dependencies, a data snapshot, an automated test suite or verified model scores. Record package versions and retrieval date if comparing runs.

## Data and attribution

The notebooks use the [community SpaceX API](https://github.com/r-spacex/SpaceX-API) and a [specific Wikipedia revision](https://en.wikipedia.org/w/index.php?title=List_of_Falcon_9_and_Falcon_Heavy_launches&oldid=1027686922). This is a coursework portfolio project. Consult linked source terms before redistributing data or exercise materials. No standalone repository license is provided.
