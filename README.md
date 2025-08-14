# BTC Liquidity Predictor




```
│
├── .env                          # API keys and config
├── package.json                  # NPM dependencies & scripts
├── package-lock.json
│
├── README.md                     # Documentation
│
├── data/                         # For CSV logs & backtest results
│   ├── signals.csv               # Generated trade signals
│   └── backtest_results.csv
│
├── src/                          # All source code
│   ├── config/                   # Configuration constants & helpers
│   │   └── settings.js
│   │
│   ├── services/                 # External API calls
│   │   ├── binanceService.js     # Binance market/funding/OI data
│   │   ├── coinglassService.js   # Coinglass liquidity data
│   │
│   ├── utils/                    # Reusable math, scoring, file utils
│   │   ├── indicators.js         # EMA, ATR, etc.
│   │   ├── scoring.js            # Signal scoring & hard block checks
│   │   ├── fileUtils.js          # CSV header & append
│   │
│   ├── predictor/                # Main prediction engine
│   │   ├── summarizeLiquidity.js # Liquidity cluster processing
│   │   ├── generateSignal.js     # Creates trade signals w/ confidence
│   │   └── index.js              # Orchestrates prediction run
│   │
│   ├── backtest/                  # Scripts for evaluation/backtesting
│   │   └── evaluateSignals.js    # Checks if targets were hit
│   │
│   └── app.js                    # CLI entry point to run predictor
│
└── scripts/                      # Utility scripts (optional)
    └── cron.sh                   # Example cronjob runner
```
