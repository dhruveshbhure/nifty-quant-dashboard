# nifty-quant-dashboard (public)

Public Nifty intraday data + GitHub Pages dashboard.  
Strategy code lives in the private [`nifty-quant-engine`](https://github.com/dhruveshbhure/nifty-quant-engine) repo; a GitHub Action there pushes updated CSVs and KPIs here daily.

## Contents

```
data/
  nifty_1m.csv          # 1-minute OHLCV (IST)
  nifty_5m.csv          # 5-minute OHLCV (IST)
docs/
  index.html            # dashboard UI
  strategies.json       # backtest metrics / trade log (generated)
```

Columns: `Datetime`, `Open`, `High`, `Low`, `Close`, `Volume` (Asia/Kolkata).

## View the dashboard

### GitHub Pages

Enable **Settings → Pages → Deploy from branch** → `main` / `/docs`.  
Site URL will be similar to:

`https://dhruveshbhure.github.io/nifty-quant-dashboard/`

### Local preview

```bash
cd docs
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000).

## Updates

Do not commit strategy scripts here. Daily updates are published automatically from `nifty-quant-engine` (CSVs + `strategies.json` only).
