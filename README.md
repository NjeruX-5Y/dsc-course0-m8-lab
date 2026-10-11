# Aviation Accident Analysis

## Project overview
This project compares injuries and aircraft damage in aviation accident reports. It helps an insurer shortlist airplane makes and models for more review. The dataset contains accidents, so it cannot tell us how likely an aircraft is to have an accident.

## Files

- `Aviation_Accidents_Cleaning.ipynb` cleans the data and creates injury and damage measures.
- `Aviation_Accidents_Data_Analysis.ipynb` compares small and large planes, makes, models, weather, and engine types.
- `data/Aviation_Data.csv` is the original data.
- `outputs/aviation_accidents_cleaned.csv` is made by the cleaning notebook and used by the analysis notebook.

## How to run

1. Open the notebooks in Jupyter from the project folder.
2. Run the cleaning notebook from top to bottom.
3. Run the analysis notebook from top to bottom.

The notebooks use pandas for data cleaning and summaries, and Matplotlib and Seaborn for charts.

## Main choices

- Keep professionally built airplanes and events from 1983 onward.
- Standardize make and model names and keep makes with at least 50 records.
- Estimate people on board by adding fatal, serious, minor, and uninjured counts. Blank counts are treated as zero for this estimate.
- Calculate the fatal/serious injury fraction from the estimated number of people on board.
- Mark damage as destroyed only when the source says `Destroyed`. Unknown damage stays blank.
- Separate small and large planes at 20 estimated people on board, as requested.
- Show sample counts with averages. Comparisons with few accident records are less certain.

## Reading the results

These are comparisons among accidents in the dataset. A low injury fraction or destruction rate does not mean an aircraft is less likely to have an accident. The analysis does not account for flight hours, aircraft age, maintenance, or mission, so use the results as a starting point for further review.
