# Structured Data Analysis Using NumPy: IPL Case Study

A complete IPL data analysis project implemented using only NumPy and core Python without using Pandas. This project demonstrates how structured datasets can be processed, aggregated, filtered, and analyzed efficiently using vectorized NumPy operations.

Dataset Source:  
https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020

---

# Project Objective

The goal of this project is to perform advanced cricket analytics on IPL datasets using only:

- NumPy
- Core Python

This project avoids:
- Pandas
- SQL
- DataFrames
- High-level aggregation libraries

The project focuses on:
- Vectorized operations
- Boolean masking
- NumPy grouping logic
- Ranking and sorting
- Real-world structured data processing

---

# Rules and Constraints

## Allowed
- NumPy
- Core Python

## Not Allowed
- Pandas
- External aggregation libraries

## Preferred Techniques
- Vectorized operations
- Boolean masking
- NumPy indexing
- NumPy aggregation functions

## Required NumPy Functions
- `np.genfromtxt()`
- `np.unique()`
- `np.where()`
- `np.argsort()`
- Boolean masking

---

# Dataset Files

The project uses two IPL dataset files:

| File | Description |
|---|---|
| deliveries.csv | Ball-by-ball IPL data |
| matches.csv | Match-level IPL metadata |

---

# Project Structure

```bash
project/
│
├── data/
│   ├── deliveries.csv
│   └── matches.csv
│
├── task0_data_loading.py
├── task1_total_runs.py
├── task2_top_batters.py
├── task3_strike_rate.py
├── task4_economy_rate.py
├── task5_runs_per_over.py
├── task6_boundary_analysis.py
├── task7_death_overs.py
├── task8_highest_scoring_match.py
├── task9_match_winner.py
├── task10_toss_impact.py
├── task11_scorecard.py
│
└── README.md
```

---

# Task Breakdown

# Task 0: Data Loading and Preprocessing

## Objective
Load IPL datasets using NumPy.

## Concepts Used
- `np.genfromtxt()`
- Handling missing values
- Mixed datatype handling
- Header skipping

## Output
Extracted arrays:
- `match_ids`
- `batting_team`
- `batter`
- `bowler`
- `batsman_runs`
- `over`

---

# Task 1: Total Runs per Match

## Objective
Compute total runs scored in each IPL match.

## Concepts Used
- `np.unique()`
- Boolean masking
- Vectorized aggregation

## Output Format

```python
[(match_id, total_runs), ...]
```

---

# Task 2: Top 5 Batters

## Objective
Find top 5 highest run scorers.

## Concepts Used
- `np.unique()`
- `np.argsort()`
- Aggregation using masking

## Output Format

```python
[(player_name, total_runs), ...]
```

---

# Task 3: Strike Rate Calculation

## Objective
Calculate strike rate of every batter.

## Formula

```text
Strike Rate = (Total Runs / Balls Faced) × 100
```

## Concepts Used
- Ball counting
- Run aggregation
- Vectorized calculations

---

# Task 4: Economy Rate of Bowlers

## Objective
Calculate economy rate of bowlers.

## Formula

```text
Economy = Runs Conceded / Overs Bowled
```

## Concepts Used
- Ball-to-over conversion
- Boolean filtering
- Aggregation

---

# Task 5: Runs per Over

## Objective
Compute average runs scored in each over.

## Overs Covered
- Over 1 to Over 20

## Output Format

```python
[avg_over_1, avg_over_2, ..., avg_over_20]
```

---

# Task 6: Boundary Analysis

## Objective
Analyze:
- Total fours
- Total sixes
- Team with most boundaries

## Concepts Used
- Conditional masking
- Aggregation

---

# Task 7: Death Overs Analysis

## Objective
Analyze scoring in overs 16–20.

## Requirements

```python
(over >= 16) & (over <= 20)
```

## Output
- Total death over runs
- Highest scoring team in death overs

---

# Task 8: Highest Scoring Match

## Objective
Find match with highest total runs.

## Output Format

```python
(match_id, total_runs)
```

---

# Task 9: Match Winner Approximation

## Objective
Approximate match winners based on total runs scored.

## Concepts Used
- Team-wise aggregation
- Match comparison
- Boolean filtering

---

# Task 10: Toss Impact Analysis

## Objective
Analyze whether toss-winning teams score more runs.

## Concepts Used
- Manual joining using NumPy
- Match ID mapping
- Team score comparison

---

# Task 11: Match Scorecard Generation

## Objective
Generate structured scorecards for each IPL match.

## Example Output

```text
Match 1:
 Team A: 180 runs
 Team B: 175 runs

Match 2:
 Team X: 200 runs
 Team Y: 198 runs
```

---

# NumPy Concepts Practiced

| Concept | Usage |
|---|---|
| Boolean Masking | Data filtering |
| Vectorized Operations | Fast calculations |
| `np.unique()` | Grouping |
| `np.argsort()` | Ranking |
| Aggregation | Summation and statistics |
| Indexing | Data extraction |
| Conditional Logic | Advanced filtering |

---

# Learning Outcomes

By completing this project, you will gain:

- Strong understanding of NumPy arrays
- Expertise in vectorized operations
- Skills in manual grouping logic
- Experience with structured CSV processing
- Real-world data analysis without Pandas
- Sorting and ranking techniques using indices
- Advanced filtering using boolean masks

---

# How to Run

## Install NumPy

```bash
pip install numpy
```

## Run Any Task

```bash
python task1_total_runs.py
```

---

# Sample Analysis Outputs

## Top Batters

```text
1. Virat Kohli - 5878
2. Suresh Raina - 5368
3. Rohit Sharma - 5230
```

## Death Overs Analysis

```text
Highest Scoring Team in Death Overs:
Mumbai Indians
```

## Highest Scoring Match

```text
Match ID: 411
Total Runs: 469
```

---

# Key Highlights

- 100% NumPy-based analysis
- No Pandas usage
- Real-world IPL analytics
- Optimized vectorized operations
- Manual grouping implementations
- Efficient large dataset processing

---

# Future Improvements

- Advanced player analytics
- Visualization using Matplotlib
- Powerplay analysis
- Bowling phase analysis
- Predictive modeling
- Performance optimization

---
