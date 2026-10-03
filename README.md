# IT171IU — Lab 01 (Chapter 2): Statistical Learning and Python

Solutions for **Lab 01**, covering NumPy, pandas, data cleaning, visualization, and
two worked examples on the bias–variance trade-off and K-nearest-neighbours
classification.

## Project structure

```
Lab1/
├── IT171IU_Lab01_Ch02_Statistical-Learning-and-Python.ipynb
├── Auto.data.csv                      # Auto dataset (used in Ex3, Ex4, Ex5, Ex7)
├── College.csv                        # College dataset (used in Ex6)
├── Ex1.py
├── Ex2.py
├── ex2_scatter.png                    # output of Exercise 2
├── Ex3.py
├── Ex4.py
├── Ex5.py
├── ex5_boxplots.png                   # output of Exercise 5
├── Ex6.py
├── ex6_boxplots.png                   # output of Exercise 6
├── ex6_histogram.png                  # output of Exercise 6
├── Ex7.py
├── Ex8.py                             # bonus
├── ex8_bias_variance.png              # output of Exercise 8
├── Ex9.py                             # bonus
└── ex9_knn_errors.png                 # output of Exercise 9
```

## Requirements

- Python 3.10+
- `numpy`
- `pandas`
- `matplotlib`
- `ISLP` (only needed for Exercise 6, the `College` dataset)

Install with:

```bash
pip install numpy pandas matplotlib ISLP
```

## How to run

Each exercise is a standalone script. All scripts expect the data files
(`Auto.data.csv`, `College.csv`) to be in the **same folder** as the script, so run
them directly from inside `Lab1/`:

```bash
cd Lab1
python Ex3.py
```

## Exercise summary

| # | Topic | Key output |
|---|-------|------------|
| 1 | NumPy warm-up: `arange`, `reshape`, slicing, `axis` reductions, view vs `.copy()` | printed arrays |
| 2 | Simulating correlated data, `corrcoef`, scatter plot with true line | `ex2_scatter.png` |
| 3 | Cleaning the `Auto` dataset, quantitative vs qualitative variables, summary stats | printed table |
| 4 | Subsetting rows with `iloc`, re-checking summary stats | printed comparison |
| 5 | Scatter-plot matrix, box plots of `mpg` by `origin`/`cylinders` | `ex5_boxplots.png` |
| 6 | `College` dataset: private colleges, `Elite` variable, box plots, histograms | `ex6_boxplots.png`, `ex6_histogram.png` |
| 7 | Loop + f-string formatting over quantitative variables | printed report |
| 8 (bonus) | Estimating Bias² and Variance by simulation (polynomial degree) | `ex8_bias_variance.png` |
| 9 (bonus) | Choosing K for KNN: training vs test error vs `1/K` | `ex9_knn_errors.png` |

## Notes

- `Auto.data.csv` is comma-separated (not whitespace-separated like the original
  ISLR `Auto.data` file), so `pd.read_csv` is used without `sep=r"\s+"`.
- Exercises 8 and 9 reuse the simulation setup from the notebook's Worked
  Examples 1 and 2 (polynomial regression and KNN classifier).
