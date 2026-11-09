# Time-Series Forecasting

Learning Time-Series Experiment Design by Forecasting Transformer Oil Temperature.

This project explores time-series forecasting using the **ETTh1 dataset** from the Electricity Transformer Temperature (ETT) benchmark.

The objective is to predict future transformer oil temperature (OT) using historical observations of electrical load variables and oil temperature.

## Dataset

**Dataset:** ETTh1 (Electricity Transformer Temperature – Hourly)

**Source:** [ETDataset GitHub Repository](https://github.com/zhouhaoyi/ETDataset)

The dataset contains approximately two years of hourly observations.

Each observation includes:

- 1 timestamp (`date`)
- 6 external power load variables (HUFL, HULL, MUFL, MULL, LUFL, LULL)
- 1 target variable: Oil Temperature (`OT`)

**Forecasting Task:**
Using all seven numerical variables from the previous **L hours**, predict oil temperature for the next **H hours**.

- **Input:** Past L hours of all 7 variables
- **Output:** Future H hours of oil temperature

## Forecasting Models

- Naive Baseline
- Seasonal Naive Baseline
- Linear Regression
- Gated Recurrent Unit (GRU)

## Experimental Setup

The dataset is divided chronologically into:

| Dataset    | Duration  |
|------------|-----------|
| Training   | 12 months |
| Validation | 4 months  |
| Testing    | 4 months  |

Data is not shuffled to preserve temporal ordering.

Models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
