Mutual Fund Plan with PythonA quantitative finance project built using Python, Pandas, and Plotly to analyze Nifty 50 historical closing prices, evaluate risk-return profiles, and construct an optimized algorithmic mutual fund investment strategy.📌 Project OverviewThis repository contains data processing pipelines and exploratory visualizations designed to build a systematic mutual fund portfolio. By analyzing daily adjusted closing prices across 50 major Indian equities from January 2024 to May 2025, the project evaluates asset volatility, growth rates, and return on investment (ROI) to simulate long-term wealth accumulation through disciplined SIP (Systematic Investment Plan) modeling.📊 Technical Architecture & WorkflowMutual_Fund_Python_Project/
│
├── 1. Data Ingestion & Validation
│   ├── Ingestion of Nifty 50 daily closing prices (50 equities)
│   ├── Native datetime conversion for chronological trading alignment
│   └── Null value audit (confirmed 0 missing records across dataset)
│
├── 2. Exploratory Data Analysis (EDA)
│   ├── Interactive multi-asset time-series trends (Plotly)
│   ├── Volatility sorting (Standard Deviation profiling)
│   ├── Daily percentage change & compound annual growth rate calculation
│   └── Cumulative ROI ranking across all constituent assets
│
├── 3. Portfolio Construction & Optimization
│   ├── Median filtering for risk-reward asset screening
│   ├── Inverse-volatility weighting methodology for risk mitigation
│   └── Comparative benchmarking against high-growth volatile equities
│
└── 4. Wealth Accumulation & SIP Simulation
    ├── Modeling monthly investments (₹5,000 starting capital)
    ├── Incorporating 10% annual step-up growth in SIP contributions
    └── Multi-horizon compounding projections (1Y, 3Y, 5Y, and 10Y horizons)
🔍 Key Analytical FindingsRisk-Return Trade-Off: High-growth momentum stocks (e.g., Bajaj Auto, Bajaj Finserv) exhibit high volatility but superior return potential, whereas defensive or stable dividend assets show lower volatility with moderate, consistent gains.Diversification Benefits: Selecting assets with volatility below the market median and ROI above the median creates a balanced portfolio tailored for capital preservation and steady long-term compounding.Power of Compounding: Simulating a step-up SIP strategy demonstrates exponential wealth expansion over a 10-year horizon, highlighting the efficacy of disciplined, automated investing.🛠️ Proposed Enhancements & Quantitative RoadmapTo elevate this notebook into an institutional-grade portfolio management system, the following quantitative upgrades are recommended:Enhancement DomainCurrent LimitationRecommended Algorithmic UpgradeNormalized PerformanceRaw prices obscure comparative percentage gains across low and high-priced stocks.Implement daily log returns ($\ln(P_t / P_{t-1})$) and cumulative normalized growth index (Base 100).Portfolio OptimizationEqual or unconstrained weighting across selected assets leads to inefficient asset allocation.Apply Modern Portfolio Theory (Markowitz Mean-Variance Optimization) using scipy.optimize to generate the Efficient Frontier (Max Sharpe Ratio portfolio).Risk-Adjusted MetricsVisual inspection fails to account for downside tail risk and maximum drawdowns.Compute explicit Sharpe Ratios, Sortino Ratios, and Maximum Drawdown (MDD) benchmarks.Dynamic RebalancingStatic buy-and-hold approach ignores portfolio drift during market shifts.Build automated quarterly rebalancing engines to restore target asset weightings and incorporate monthly SIP NAV unit allocations.💻 Tech Stack & DependenciesLanguage: Python 3.12+Data Manipulation: pandas, numpyVisualization: plotly, matplotlib, seabornEnvironment: Google Colab / Jupyter Notebook
