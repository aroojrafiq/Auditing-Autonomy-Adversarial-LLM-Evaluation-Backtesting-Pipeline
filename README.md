Auditing Autonomy: Adversarial LLM Evaluation & Backtesting Pipeline

An enterprise-grade Multi-Stage Stress Test (MSST) framework evaluating the technical reliability, adversarial robustness, and decision-making maturity of frontier Large Language Model (LLM) agents (specifically evaluated on Gemini 3.1 Pro) acting as autonomous Quantitative Data Scientists.

This repository implements raw data curation, adversarial injection of physical and logical anomalies, recursive code generation safety reviews, and a high-fidelity algorithmic backtesting engine modeling market frictions and asymmetric slippage.

🎯 Profile & SEO Parsing Metadata (Recruiter Keywords)

Primary Domains: Quantitative Engineering, Algorithmic Trading Systems, AI Safety, LLM Evaluation, Financial Data Pipelines.

Core Competencies: Adversarial Testing, Structural Anomaly Detection, Time-Series Analysis, Risk Mitigation Architecture, Human-in-the-Loop (HITL) Debugging.

Tech Stack: Python 3.13+, Pandas, NumPy, Math/Stat Modeling, Vectorized Backtesters, Data Governance Frameworks.

📊 Quantitative Performance Scorecard

The agent's strategic capabilities and vulnerability profiles are measured across three core quantitative metrics:

KPI Metric

Mathematical Definition

Empirical Evaluation

Audit Takeaway

Anomaly Detection Rate

$DR = \frac{\text{Detected Traps}}{\text{Injected Traps}}$

75% (3/4 traps identified)

Critical failure in row-level redundancy; heavy reliance on semantic parsing over data cardinality.

Optimization Alpha ($\alpha_{\text{opt}}$)

$\frac{PnL_{\text{final}} - PnL_{\text{initial}}}{\lvert PnL_{\text{initial}}\rvert}$

+486.6% Profit Improvement

Validates system utility as a guided "Code Force Multiplier" under manual trend-filtering heuristics.

Fragility Coefficient ($FC$)

$\frac{PF_{\text{Asymmetric}}}{PF_{\text{Standard}}}$

-17.5% Robustness Decay

Quantified "Edge Erosion" under structural market friction. Hard basis for the institutional 'NO-GO' verdict.

🛠️ System Architecture & MSST Pipeline

The evaluation pipeline challenges the agentic workflow across three sequential validation phases, illustrated below:

                  [Input] Raw EURUSD 15M Data (Neutral Masked)
                                      │
                                      ▼
                  [Phase 1: Adversarial Outlier Injection]
             (Spikes, Logical Paradoxes, Temporal Gaps, Duplicates)
                                      │
                                      ▼
                   [Phase 2: Agentic Data Governance Audit]
                 (Outlier Isolation & Code Verification Loop)
                                      │
                                      ▼
                [Phase 3: Backtesting & Advanced Optimization]
                (Fair Value Gap Logic & 200 SMA Trend Filtering)
                                      │
                                      ▼
                  [Phase 4: Worst-Case Market Friction Stress]
                  (Asymmetric Slippage & Execution Constraints)
                                      │
                                      ▼
                 [Final Output] Institutional Deployment Verdict
                           (1.08 PF -> 'NO-GO' Seal)


1. Adversarial Injection Layer

The dataset is programmatically compromised with four distinct, hard-to-detect stress vectors to verify semantic vs. quantitative data boundary parsing:

Structural Redundancy: Duplicated index values simulating system telemetry lag.

Statistical Outlier: An anomalous spike (Z-Score $> 15.0$) simulating fat-finger trade failures.

Logical Paradox: Candle limits violating physical boundaries ($Low > Open$).

Temporal Discontinuity: Missing data segments simulating network drops on high-volatility days (e.g., London Open).

2. Algorithmic Trading & Sequential Logic

The strategy evaluates Fair Value Gaps (FVG). To prevent "Look-ahead Bias", the logic strictly enforces sequential index lookbacks utilizing a three-candle state space ($i-2, i-1, i$):

Bullish FVG Condition:


$$High[i-2] < Low[i]$$

Bearish FVG Condition:


$$Low[i-2] > High[i]$$

To filter high-frequency noise, a 200-Period Simple Moving Average (SMA) is added. Long positions are strictly filtered to occurrences where $\text{Close}[i] > \text{SMA}_{200}[i]$, and short positions where $\text{Close}[i] < \text{SMA}_{200}[i]$.

3. Asymmetric Slippage & Market Friction

In live broker conditions, execution isn't clean. The engine tests robustness by simulating extreme market friction:

Asymmetric Limit Orders: If the price gaps past a Limit Buy, the broker captures the difference; we are filled at the intended FVG top (no positive slippage).

Slippage-Prone Stops: If the price gaps past our Stop Loss, negative slippage forces execution at the Open of the next candle.

This rigorous simulation collapsed the strategy's Profit Factor ($PF$) from $1.31$ down to 1.08, leading to an objective, capital-preservation-first NO-GO Recommendation for live account deployment.

📂 Repository Structure

├── 00_README.md                       <- Master roadmap & architectural design (This file)
├── 01_Final_Report/
│   └── Auditing_Autonomy_Report.pdf   <- Executive summary & quantitative evaluation write-up
├── 02_Source_Code/
│   ├── initial_audit_v1_silent_failure.py <- Unrefined agent script showing data ingestion faults
│   ├── data_governance_audit.py       <- Hardened pipeline isolating data anomalies
│   ├── precision_probe_debug.py       <- Time-series index integrity analyzer
│   └── fvg_backtest_engine.py         <- Friction-aware, 200 SMA-filtered backtesting suite
├── 03_Data_Assets/
│   ├── EURUSD_15M_Reference.csv       <- Clean base-truth historical series
│   └── EURUSD_15M_BATCH_02.csv        <- Adversarially poisoned validation batch
├── 04_Verification_Evidence/
│   └── figures/                       <- High-resolution terminal traces & visual execution proof
└── 05_Appendix_Transcripts/
    └── GEMINI_TRANSCRIPTS.txt         <- Complete, raw 7-session agent developer transcripts


🔁 Reproducibility Protocol

Follow these steps to programmatically reproduce the complete evaluation audit trail:

Environment Setup: Ensure Python $3.13+$ is configured.

pip install pandas numpy matplotlib


Execute Data Governance Audit:

python 02_Source_Code/data_governance_audit.py


Verify that the data engineering pipeline flags the structural anomalies, temporal gaps, and logical boundary violations.

Run Backtest Engine:

python 02_Source_Code/fvg_backtest_engine.py


Toggle asymmetric_slippage = True inside the script to observe the mathematical decay of the strategy's Profit Factor down to the $1.08$ baseline.

Developed as part of the Turing Frontier AI Data Scientist Challenge.
