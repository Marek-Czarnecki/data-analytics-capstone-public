# data-analytics-capstone-public

This repository exists to make the cleaned ASX prices dataset visible and runnable for faculty review.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Marek-Czarnecki/data-analytics-capstone-public/blob/main/notebooks/asx_ohlcv_panel_public_demo.ipynb)

## Included Files

- `data/processed/market_ohlcv_daily_v2/exchange=ASX/asx_ohlcv_panel_clean.parquet`
- `notebooks/asx_ohlcv_panel_public_demo.ipynb`

## What This Proves

The parquet file is the processed output of the preprocessing workflow, not a raw vendor extract.

Evidence in the file:

- 465,607 rows across 201 ASX tickers
- date coverage from `2016-07-25` to `2026-07-20`
- cleaned price columns: `open_clean`, `high_clean`, `low_clean`, `close_clean`
- validation fields: `ohlc_valid_flag`, `ohlc_issue_type`
- derived return field: `daily_return`

These fields show that quality checks and cleaning were already applied before export.

## Open In Jupyter

From the repository root:

```bash
jupyter notebook
```

Then open:

- `notebooks/asx_ohlcv_panel_public_demo.ipynb`

The notebook loads the parquet file, verifies the preprocessing columns, and runs a small example analysis.
