<h1 align="center">Hi, I'm Carson</h1>

<p align="center">
  <b>Financial Analyst</b> · FP&amp;A · Equities &amp; Options · Crypto · Tokenization · AI
</p>

<p align="center">
  <a href="https://wavebyrd.com"><img src="https://img.shields.io/badge/wavebyrd.com-111111?style=flat-square&logo=googlechrome&logoColor=white" alt="Website"></a>
  <a href="https://pantherterminal.com"><img src="https://img.shields.io/badge/Panther_Terminal-0b7a3e?style=flat-square&logo=databricks&logoColor=white" alt="Panther Terminal"></a>
  <a href="mailto:contact@wavebyrd.com"><img src="https://img.shields.io/badge/contact@wavebyrd.com-c0392b?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

### About me

Financial analyst focused on forecasting, budgeting, and variance analysis. Active in equities and options trading, with a strong interest in crypto, asset tokenization, and AI-driven financial tools. I build open source Python tools for finance work that has to tie out: [OpenVariance](https://github.com/wavebyrd/openvariance) for variance analysis and forecasting, and [Form4Clean](https://github.com/wavebyrd/form4clean) for SEC insider trading data.

### What I focus on

| Area | What that looks like |
| --- | --- |
| **FP&A** | Budgeting, rolling forecasts, budget-vs-actual variance analysis, driver-based models |
| **Equities & options** | Fundamental and technical research, options pricing and Greeks, volatility, strategy backtesting |
| **Crypto** | Market structure, on-chain data, exchange APIs, DeFi mechanics |
| **Tokenization** | Tokenized stocks, bonds, stablecoins, and real-world assets (RWAs) |
| **AI** | LLM agents and MCP tools for financial analysis, forecasting, and research automation |

### Projects

| Project | What it does |
| --- | --- |
| [OpenVariance](https://github.com/wavebyrd/openvariance) | Open source FP&A variance analysis. Explains why the numbers moved with driver bridges that reconcile to the cent, builds linked three-statement forecasts, pulls public-company data from SEC EDGAR, writes formula-driven Excel, and runs as an MCP server so AI agents can use it. Python. |
| [Form4Clean](https://github.com/wavebyrd/form4clean) | Clean, research-ready SEC Form 4 insider trading data. Downloads filings from EDGAR, classifies every transaction code, reconciles amendments without double-counting, runs 39 data quality checks, and gives point-in-time views with no look-ahead bias. Library, CLI, exports and a local dashboard. Python. |
| [panther-tokenization-onboarding](https://github.com/wavebyrd/panther-tokenization-onboarding) | Educational portfolio simulator for tokenized assets. Mean-variance allocation, a glide path with correlated stock and bond returns, and live checks of which issuer and chain can fill each order at its real size. TypeScript. |
| [Panther Terminal](https://pantherterminal.com) | Market intelligence platform for tokenized securities and real-world assets. |

OpenVariance and Form4Clean are MIT licensed. Both run locally, use only free public data, and keep money math exact. The tokenization simulator is public but not licensed for reuse.

### Open source contributions

53 pull requests merged into 30 public repositories outside my account, as of October 31, 2026 ([search](https://github.com/search?q=author%3Awavebyrd+is%3Apr+is%3Amerged+is%3Apublic+-user%3Awavebyrd&type=pullrequests)). Mostly correctness fixes in the Python finance and crypto libraries I use.

| Project | Fix | What was wrong |
| --- | --- | --- |
| [yfinance](https://github.com/ranaroussi/yfinance/pull/2718) | Make `download()` thread-safe | Concurrent calls shared module-level result dicts, so one thread could overwrite another's data and return a corrupted DataFrame. Added a lock and a two-thread test. |
| [vectorbt](https://github.com/polakowo/vectorbt/pull/886) | Record active drawdowns when a series ends in NaN | The numba kernel only saved a running drawdown on the last row, and skipped that check on NaN, so any asset whose data ended early reported no drawdown at all. |
| [viem](https://github.com/wevm/viem/pull/5240) | Keep an empty `version` in the EIP-712 domain | A truthiness check dropped `version: ""` from the type hash, so signatures for contracts like OpenZeppelin's `EIP712("Name", "")` failed to verify. Result now matches ethers v6. |
| [solana-py](https://github.com/michaelhly/solana-py/pull/709) | Decode every signer in M-of-N multisigs | The decoders read the last `m` accounts as signers, but `m` is the signature threshold, so an M-of-N multisig with M < N lost its first N - M signers on round trip. |
| [ffn](https://github.com/pmorissette/ffn/pull/429) | Ignore leading missing prices in monthly and yearly stats | An asset that started trading later got empty months before its first price, which zeroed its first month, skewed YTD, and inflated the win-rate denominators. Single-series and grouped stats disagreed on the same data. |

Others: a UK bank holiday calendar fix in FinancePy, ccxt tickers missing bid and ask, a news cache in yfinance that ignored its arguments, and smaller fixes in aiohttp, bokeh, CPython, cryptofeed, FinanceToolkit, nostr-tools and skfolio.

### Toolkit

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="pandas">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL">
  <img src="https://img.shields.io/badge/Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white" alt="Excel">
  <img src="https://img.shields.io/badge/Ethereum-3C3C3D?style=flat-square&logo=ethereum&logoColor=white" alt="Ethereum">
  <img src="https://img.shields.io/badge/Solana-9945FF?style=flat-square&logo=solana&logoColor=white" alt="Solana">
</p>

### Currently

- Building [OpenVariance](https://github.com/wavebyrd/openvariance) and [Form4Clean](https://github.com/wavebyrd/form4clean)
- Contributing fixes to the Python finance and crypto libraries I use, including yfinance, FinancePy, ffn, bt and solana-py
- Researching tokenized securities and RWA market structure

---

<p align="center"><sub>Open to conversations about FP&amp;A, markets, and on-chain finance. Say hi at <a href="mailto:contact@wavebyrd.com">contact@wavebyrd.com</a>.</sub></p>
