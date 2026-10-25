# BCHUSDT 1-Minute Historical Kline Dataset

An institutional-grade, open-source archive of cleaned, standardized, and validated **1-minute intraday historical kline data** for **BCHUSDT** (Binance Spot).

---

## 📊 Dataset Specifications
- **Symbol:** `BCHUSDT`
- **Market:** Binance Spot
- **Timeframe:** 1 Minute (`1m`)
- **Total Months:** `84` months
- **Total Candles:** `3,630,194` 1-minute candles
- **Historical Range:** `2019-11-28 10:00:00` to `2026-10-24 23:59:00` (UTC)
- **Schema:** `timestamp, datetime_utc, open, high, low, close, volume, quote_volume, trade_count, taker_buy_volume, taker_buy_quote_volume`

---

## 🏛️ Directory Hierarchy
```text
BCHUSDT-Historical-Data/
├── README.md
└── 1m/
    └── <YYYY>/
        └── <MM>/
            └── BCHUSDT_1m_<YYYY-MM>.csv
```

---

## ⚡ 1-Line Pandas Stream Loader
Load any month directly from GitHub's raw CDN without cloning the repository:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/parshant231234-eng/BCHUSDT-Historical-Data/main/1m/2026/10/BCHUSDT_1m_2026-10.csv"
df = pd.read_csv(url)
print(df.head())
```
