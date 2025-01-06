# WAR DOLLARS - Winning the Budget Game in Baseball Management

## Overview
This repository contains the research project **"WAR Dollars: Winning the Budget Game in Baseball Management"**, which examines the relationship between MLB player salaries and Wins Above Replacement (WAR) during the 2019-2022 seasons. The goal of the study is to analyze the cost-effectiveness of pitchers versus position players in contributing to team success, measured by WAR, and provide actionable insights for optimizing payroll allocation.

## Key Objectives
- Determine whether position players or pitchers provide better WAR per dollar spent.
- Identify which positions offer the most value in terms of WAR for their salaries.
- Explore resource allocation strategies that maximize financial efficiency and team performance.

## Hypotheses
1. **Null Hypothesis (H0):** There is no difference in WAR between a pitcher and position player based on salary.
2. **Alternative Hypothesis (Ha):** Pitchers are overpaid relative to their contributions to WAR, while position players are underpaid relative to their contributions.

## Data Sources
The analysis integrates data from the following sources:
- **Wins Above Replacement (WAR):** Data retrieved from FanGraphs using the `pybaseball` Python package.
- **Player Salaries:** Data from Spotrac, a comprehensive resource for sports contracts and team payrolls.
- **Player Positions:** Data from Statcast (via `pybaseball`), providing details on players' primary positions.

## Methodology
The research employs:
- Statistical regression analysis to explore relationships between salary and WAR.
- Decision tree models and k-fold cross-validation for model accuracy and reliability.
- Factor analysis to evaluate significant metrics impacting WAR.

Key performance indicators (KPIs) analyzed include:
- On-base Plus Slugging (OPS)
- Walks-to-Strikeouts ratio (BB/K)
- Innings pitched (for pitchers)
- Home runs per nine innings (HR/9)

Logarithmic transformations were applied to address data skewness, and diagnostic tests (e.g., Variance Inflation Factor analysis) were used to ensure model robustness.

## Results
### Position Players
- Players in premium defensive positions (shortstop, centerfield, catcher) contributed higher WAR at similar salary levels compared to non-premium positions (e.g., left field, designated hitter).
- Age negatively correlated with WAR, highlighting the importance of avoiding overinvestment in aging players.
- R-squared value of 0.55 indicated that selected variables explained 55% of the variability in WAR for position players.

### Pitchers
- High WAR values were strongly associated with higher innings pitched and a lower HR/9 ratio.
- Starting pitchers demonstrated greater cost-effectiveness due to their ability to "eat innings."
- R-squared value of 0.80 suggested a high explanatory power for the regression model.

## Key Takeaways
- Position players generally provide more WAR per dollar spent than pitchers.
- Investing in "up-the-middle" players (e.g., SS, CF, C) yields the highest returns.
- While pitchers are crucial, their cost-effectiveness is less pronounced compared to position players, especially as salaries increase.
- Teams can benefit from targeting durable starting pitchers and players with high plate discipline metrics (BB/K ratio).

## Limitations
- Dataset is limited to the 2019-2022 seasons, including the shortened 2020 season (due to COVID-19).
- Positional flexibility was not fully captured, as only primary positions were analyzed.

## Tools Used
- Python (with `pybaseball` for data retrieval)
- JMP software for regression and diagnostic analysis
- Data visualization libraries (e.g., Matplotlib, Seaborn)

## Repository Structure
```
|-- data/             # Raw and processed datasets
|-- notebooks/        # Jupyter notebooks for analysis
|-- scripts/          # Python scripts for data processing and modeling
|-- results/          # Visualizations and regression outputs
|-- README.md         # Project overview (this file)
```

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/WAR-Dollars-Baseball.git
   ```
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Navigate to the `notebooks/` directory to explore the analysis step-by-step.

## Contributions
Contributors: Graeme Ashley, Matthew Kassiman, Jose Smith, Daniel Wong Ortiz, and Yusef Trad.

If you'd like to contribute, feel free to submit a pull request or open an issue.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
