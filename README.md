# Covid-19 Cases Prediction with Python

## Project Overview
This machine learning project predicts Covid-19 cases for the next 30 days using the **Facebook Prophet** time series forecasting model. The project analyzes global confirmed cases and deaths, visualizes the data with geographical and time series plots, and forecasts future cases based on historical trends. The dataset is sourced from publicly available Covid-19 data, and the project is implemented in Python.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features
- **Data Preprocessing**: Combines global confirmed cases and deaths datasets into a unified format for analysis.
- **Visualizations**:
  - Geographical choropleth map showing the worldwide spread of Covid-19 cases.
  - Time series plots of daily global cases and deaths with moving averages.
  - Forecast plot for the next 30 days with confidence intervals.
- **Forecasting**: Uses the Facebook Prophet model to predict Covid-19 cases for the next 30 days.
- **Model Evaluation**: Calculates the R² score to assess the forecasting model's performance.

## Dataset
The project uses two CSV files:
- [**CONVENIENT_global_deaths.csv**](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university/download): Contains daily Covid-19 deaths by country.
- [**continents2.csv**](https://www.kaggle.com/andradaolteanu/country-mapping-iso-continent-region/download): Provides country-to-continent mappings for geographical visualization.

These datasets are publicly available and sourced from reliable repositories (e.g., Johns Hopkins University or similar). Ensure you include these files in the `data/` directory of the repository.

## Installation
To run this project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/rohazshaik07/Covid-19-Cases-Prediction-with-Python.git
   cd Covid-19-Cases-Prediction-with-Python
   ```

2. **Set Up a Virtual Environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   Ensure you have Python 3.8+ installed. Then, install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

   The `requirements.txt` file includes:
   ```
   pandas>=2.2.2
   numpy>=2.0.2
   matplotlib>=3.10.0
   plotly>=5.0.0
   prophet>=1.1.6
   scikit-learn>=1.5.0
   ```

4. **Add Datasets**:
   Place the `CONVENIENT_global_confirmed_cases.csv`, `CONVENIENT_global_deaths.csv`, and `continents2.csv` files in a `data/` directory within the project folder.

## Usage
1. **Run the Script**:
   Execute the main Python script to preprocess data, generate visualizations, and produce the forecast:
   ```bash
   python covid_prediction.py
   ```

2. **Expected Outputs**:
   - A choropleth map showing global Covid-19 case distribution.
   - Time series plots for daily cases and deaths with 5-day moving averages.
   - A 30-day forecast plot with confidence intervals for future cases.
   - The R² score of the Prophet model's fit.

3. **Jupyter Notebook**:
   The project is compatible with Jupyter Notebook for interactive execution. Open `covid_prediction.ipynb` in Jupyter:
   ```bash
   jupyter notebook covid_prediction.ipynb
   ```

## Visualizations
The project generates three key visualizations:
1. **Geographical Spread**: A choropleth map using Plotly, color-coded by case ranges (e.g., <50K, 50K-200K, etc.).
2. **Daily Cases**: A time series plot of global daily Covid-19 cases with a 5-day moving average.
3. **Daily Deaths**: A time series plot of global daily Covid-19 deaths with a 5-day moving average.

The forecast visualization shows predicted cases for the next 30 days with upper and lower confidence bounds.

## Results
- The Prophet model provides a 30-day forecast of global Covid-19 cases, visualized with confidence intervals.
- The R² score indicates the model's goodness-of-fit, typically printed in the console after running the script.
- Example output (hypothetical):
  - R² Score: ~0.85 (varies based on data).
  - Forecasted cases for the next 30 days are plotted with uncertainty bounds.

## Technologies Used
- **Python**: Core programming language.
- **Pandas**: Data manipulation and preprocessing.
- **NumPy**: Numerical computations.
- **Matplotlib**: Time series visualizations.
- **Plotly**: Interactive geographical visualizations.
- **Prophet**: Time series forecasting.
- **Scikit-learn**: R² score calculation.

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

Please ensure your code follows PEP 8 guidelines and includes appropriate documentation.

## Contact
For questions or feedback, reach out to:
- GitHub: [rohazshaik07](https://github.com/rohazshaik07)
- Email: [Your Email] (shaikrohaz@gmail.com)
