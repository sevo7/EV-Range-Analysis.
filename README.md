# EV Range Analysis

Analysing how electric vehicle range changes with temperature, using Python.

This project looks at the real-world range of 25 electric vehicles across six temperatures (−20°C to 40°C) and compares it against manufacturers' rated range.

## Key findings

- **Range peaks near room temperature (21°C) and falls at both colder and hotter extremes.** This pattern holds across every car in the dataset.
- **Cold weather is costly:** real range at −20°C is only around 44% of the 21°C peak — a loss of roughly 56%. For example, the Nissan Leaf drops from 253 km to 110 km.
- **Rated range overstates everyday range:** the manufacturer's quoted figure roughly matches the best case (≈21°C), so real range in typical conditions sits below the headline number.
- **Price buys range with diminishing returns:** higher-priced EVs tend to have more range, but with notable exceptions — the €180k Porsche Taycan has less 21°C range than the cheaper Lucid Air.

![Rated range vs real range across temperatures](images/rated_vs_real_range.png)

## A note on the data

The dataset appears to be modelled rather than directly measured — several cars show identical range values at different temperatures, suggesting fixed multipliers were applied to a rated figure. The findings should be read as illustrating the expected *pattern* of temperature-driven range loss rather than precise measured values.

## Data

EV models with rated range, price, and real range at six temperatures, held in the `data/` folder. [Add the source if you have it, e.g. "Data sourced from EV Database."]

## Project structure

- `src/` — Python scripts for the analysis and plots
- `data/` — the EV dataset
- `images/` — generated plots

## How to run
1. Clone the repository:https://github.com/sevo7/EV-Range-Analysis.git
2. Install dependencies: pip install pandas matplotlib seaborn
3. Run the analysis: python src/ev_range_analysis.py

## Dependencies

- pandas
- matplotlib
- seaborn
