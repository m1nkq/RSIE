# Road Safety in Estonia (2013–2025)

## Authors

- Milena Nikišina
- Ratmir Bezrodnõi

University of Tartu – Introduction to Data Science (2026)

## Motivation

Road traffic accidents are an important public safety issue. Understanding how accident severity differs across environmental conditions, geographical locations and time periods can help identify patterns in road traffic accidents in Estonia.

## Project Goal

The main goal of this project is to analyse road traffic accidents in Estonia between 2013 and 2025 and compare the proportions of fatal accidents under different conditions.

Our analysis focuses on:

- Changes in the proportion of fatal accidents over time.
- Differences between daylight and darkness.
- Differences across weather conditions.
- Regional differences in accident severity.
- Differences between accident types and road characteristics.

We use descriptive statistics, exploratory data analysis (EDA) and data visualisation rather than predictive machine learning models.

## Dataset

The dataset was provided by the Estonian Transport Administration (Transpordiamet). The original dataset covers the period from 2011 to 2026.

We selected the period from 2013 to 2025 because geographical data for 2011–2012 were not corrected and the data for 2026 are incomplete.

After filtering and removing duplicates, the prepared dataset contains 19,867 accident records. The main analysis uses 13 selected columns.

## Repository Structure

| File | Description |
|---|---|
| `IDS2026_HW07.ipynb` | Initial project setup, business understanding and exploratory data analysis. |
| `IDS2026_HW10.ipynb` | Data preparation, statistical comparisons and visualisations. |
| `lo_2011_2026.csv` | Original road traffic accident dataset. |
| `README-lo-AA.md` | Official dataset documentation. |
| `README.md` | Project description and instructions. |
| `requirements.txt` | Required Python libraries. |

## Data Preparation

The main data preparation steps include:

- Filtering the dataset to the period 2013–2025.
- Removing duplicate records.
- Converting accident dates to datetime format.
- Checking missing and inconsistent values.
- Selecting relevant columns for analysis.
- Creating the `Year` and `Fatal accident` variables.
- Excluding unknown values from relevant comparisons without removing records from the full dataset.

For the preliminary weather visualisation, only known weather categories with at least 100 recorded accidents are displayed.

## How to Reproduce the Analysis

1. Clone the repository:

   `git clone https://github.com/m1nkq/RSIE.git`

2. Open the project directory:

   `cd RSIE`

3. Install the required Python libraries:

   `pip install -r requirements.txt`

4. Start Jupyter Notebook:

   `jupyter notebook`

5. Open `IDS2026_HW10.ipynb` and run all cells in order.

Make sure that the original CSV file is located in the same directory as the notebook.

## Limitations

The dataset contains only registered road traffic accidents involving injuries or fatalities. It does not include all traffic accidents or information about traffic volume.

Therefore, the results describe differences in accident severity among recorded accidents rather than the actual probability of experiencing an accident under specific conditions.

The observed relationships should not be interpreted as causal relationships.
