# FIFA Player Dataset Analysis (2015–2020)

Data analysis in **Python** of the FIFA 15 to FIFA 20 player datasets published on Kaggle. The scripts compare consecutive editions to find which players were added or removed each year, generate charts about nationalities and market value, and build a dataset of players still active in 2020.

Personal practice project in data analysis (August 2025).

> The original Spanish documentation is kept in [README.es.md](README.es.md).

## Objective

Practice loading, cleaning, comparing and visualizing tabular data with pandas and matplotlib.

## Technologies

- Python
- pandas, matplotlib (and openpyxl to read `.xlsx` files)

## Main features

- Load every `.csv`/`.xlsx` file in `dataset_fifa/` and show its shape and first rows
- Compare each edition with the previous one and export the players added and removed per year
- Charts per year: most added nationalities, most removed nationalities, and top 5 most valuable players added and removed
- Generate `jugadores_activos_2020.csv` with the players not removed up to 2020

## Project structure

```text
scripts/
├── leer_datasets.py                  # Load and preview the datasets
├── comparador_dataset.py             # Added / removed players per year
├── estadisticas_jugadores.py         # Charts (PNG) by year
└── generador_dataset_actualizado.py  # Active players in 2020
dataset_fifa/
├── players_15.csv … players_20.csv   # Source data
├── teams_and_leagues.csv
├── jugadores_agregados/              # Generated: added players per year
├── jugadores_eliminados/             # Generated: removed players per year
├── jugadores_actualizados_2020/      # Generated: active players in 2020
└── estadisticas/                     # Generated charts
```

## Requirements

- Python 3.10 or later

## Installation and running

```bash
git clone https://github.com/leandro-ortegon/fifa-dataset-analysis.git
cd fifa-dataset-analysis
pip install -r requirements.txt

cd scripts            # the scripts use paths relative to this folder
python leer_datasets.py
python comparador_dataset.py
python estadisticas_jugadores.py
python generador_dataset_actualizado.py
```

## Project status

Completed practice project.
