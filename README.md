# Forensics Process Optimization using Simul8, Excel, and Python

This project simulates and analyzes DNA forensics processes for West Yorkshire Police to identify the most cost-effective operational setup for delivering results within a 48-hour window. The study was part of the MANM304 Operational Analytics module at the University of Surrey (2025 cohort).

## 🎯 Objective
To model and compare different forensics process configurations using discrete-event simulation and perform ROI analysis to support strategic decision-making for Rapid DNA implementation.

## 🧰 Tools Used
- **Simul8** – to simulate the current and proposed forensic process scenarios.
- **Excel** – to generate and organize datasets from Simul8 output (5,000 trials).
- **AtRisk (Palisade)** – to conduct Monte Carlo simulations and compute ROI estimates.
- **Jupyter Notebook (Python)** – to perform sensitivity analysis and visualize queueing distributions.

## 📁 Project Structure

forensics-optimization-simul8/
├── data/                      # Excel datasets created from Simul8 exports
│   ├── queue_times_scenario1.xlsx
│   └── ...
├── simulate_models/           # Simul8 models for all 6 scenarios
│   ├── current_process.s8
│   ├── scenario1.s8
│   └── ...
├── visualizations/            # Python analysis and plots
│   ├── sensitivity_analysis.ipynb
│   ├── queue_distributions.png
│   └── ...
├── reports/                   # Final report and presentation
│   ├── group_presentation.pdf
│   └── final_report.pdf
└── README.md

## 📊 Scenarios Modeled
Six scenarios were developed and compared:
1. **Current process**
2. **Rapid DNA machine**
3. **Rapid DNA + courier**
4. **Rapid DNA + 24hr CSI**
5. **Rapid DNA + 24hr lab**
6. **Full 24/7 operation (CSI + lab)**

Each scenario was run for 5,000 trials to ensure convergence and reliability of results.

## 📈 Key Analyses
- **Simulation Metrics**: Total time in system, queueing delays, validation bottlenecks.
- **Queue Distributions**: Plotted for each stage using Python subplots with consistent axes.
- **Sensitivity Analysis**: Tornado and spider plots generated from correlation and perturbation methods.
- **ROI Analysis**:
  - ROI = Arrests per £m spent
  - ROI computed using AtRisk simulations in Excel
  - Arrest probability modeled as a function of delay using provided objective function

## 💡 Findings
- Scenario 6 (full 24/7 CSI and lab operation) had the highest arrest potential but at the highest cost.
- Scenario 4 and 5 offered balanced trade-offs between cost and turnaround time.
- Queueing at the DNA sequencer and CSI availability were major bottlenecks in early scenarios.
- Sensitivity analysis revealed that transport delays and validation times significantly impacted system performance.

## 📌 Conclusion
This project highlights the value of simulation in operational decision-making. Through scenario modeling and ROI analysis, we provide actionable insights into how West Yorkshire Police can optimize their forensic DNA process to balance cost, speed, and arrest likelihood.

## 🖥️ Requirements (for Jupyter Visualizations)
Install dependencies with:

```bash
pip install pandas matplotlib seaborn
