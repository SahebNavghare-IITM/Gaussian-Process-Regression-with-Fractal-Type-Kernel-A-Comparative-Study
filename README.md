# Gaussian-Process-Regression-with-Fractal-Type-Kernel-A-Comparative-Study

This repository contains the complete implementation and report for the course project:

**"Gaussian Process Regression with Fractal-Type Kernel: A Comparative Study"**  
(May 2025)

---

## 📁 Repository Structure

```
Project Root/
├── Program/                                   # Python programs used to produce results
├── Report/                                    # PDF report, figures, and LaTeX ZIP
├── Crude Oil WTI Futures Historical Data.csv  # Dataset
└── README.md                                  # Project documentation
```

---

## 📌 1. `Program/` – Code

This directory contains all source code files used for:

- ✅ Constructing fractal-type kernels (cosine & polynomial basis)
- ✅ Performing Gaussian Process Regression (GPR)
- ✅ Estimating the mean function via Priestley-Chao regression
- ✅ Tuning hyperparameters using **Optuna** with TPESampler (4000+ trials)
- ✅ Reproducing all experimental figures and metrics

Each script is modular and corresponds directly to results discussed in the report and research paper.

---

## 📌 2. `Report/` – Project Report Files

- 📄 `Project_Report__Modeling_Workshop.pdf` – Full detailed report including:
  - Mathematical framework
  - Kernel construction and theory
  - Experimental results with figures
  - Performance comparison
  - Extensions and future work
- 🖼️ Visualization images
- 📦 ZIP archive of LaTeX source for the report

---

## 🧪 Results Summary

All models were tested on **Crude Oil WTI Futures** daily high prices (Oct 2021 – Jul 2022).

| **Kernel**               | **Log Marginal Likelihood** | **MSE** | **MAE** | **R²**  | **CI Coverage** |
|--------------------------|-----------------------------|---------|---------|--------|-----------------|
| RBF                      | -31.87                      | 28.42   | 3.88    | —      | 82%             |
| Fractal - Cosine Basis   | -30.01                      | 29.77   | 3.85    | 0.86   | 89%             |
| Fractal - Polynomial     | **-29.74**                  | 29.93   | 3.92    | 0.86   | Not Reported    |

📌 **Observation**: The fractal-type kernel with polynomial basis yielded the best log marginal likelihood, indicating better model fit.

---

## ⚙️ Requirements

To run the code, install the required Python libraries:

```bash
pip install numpy pandas matplotlib optuna
```

---

## 🚀 Run Instructions

- Clone the repository
- Navigate to the `Program/` folder
- Execute individual scripts or notebooks to reproduce figures and metrics from the report
- All plots and predictions will be saved or displayed inline

---

## 📚 References

1. Luor, D.C. & Liu, C.W. (2024).  
   *Applications of fractal-type kernels in Gaussian process regression and support vector machine regression*,  
   [Computational and Applied Mathematics](https://link.springer.com/10.1007/s40314-024-02952-8)

2. Rasmussen & Williams (2006).  
   *Gaussian Processes for Machine Learning*, MIT Press.  
   [Read online](http://gaussianprocess.org/gpml/chapters/RW.pdf)

3. Optuna Framework:  
   [https://optuna.readthedocs.io/en/stable/](https://optuna.readthedocs.io/en/stable/)

4. Crude Oil WTI Futures Dataset:  
   [https://www.investing.com/commodities/crude-oil-historical-data](https://www.investing.com/commodities/crude-oil-historical-data)

---

## 📬 Contact

**Author**: Saheb D. Navghare  
**Email**: ma24m020@smail.iitm.ac.in

---

Feel free to raise issues or contribute improvements. Thank you for visiting this repository!
