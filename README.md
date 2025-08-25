# qda-algorithm-for-fault-detection
# QDA Algorithm for Fault Detection in Boeing 737 Aircraft

## Project Overview
This repository contains the implementation and research code for:

**Development of a Quadratic Discriminant Analysis (QDA) Algorithm for Fault Detection in Boeing 737 Aircraft**

By Shittu Rofeeq Adeleke (U21CS1046)
Department of Computer Science, Air Force Institute of Technology, Kaduna
August 2025

## Abstract
Undetected faults in Boeing 737 aircraft pose significant safety risks and contribute to costly unscheduled downtime. This project advances fault detection by developing a QDA algorithm trained on the NASA CMAPSS FD001 dataset, simulating 20,631 turbofan engine cycles. The workflow includes feature standardization, Remaining Useful Life (RUL) labeling, class balancing with SMOTE, and robustness validation under noise. The resulting model achieves 99% accuracy, 94% recall, and an AUC of 0.9955, surpassing FAA safety benchmarks. Results demonstrate QDA’s capability to strengthen predictive maintenance and operational efficiency in aviation.

## Table of Contents
- [Project Overview](#project-overview)
- [Abstract](#abstract)
- [Methodology](#methodology)
- [Results](#results)
- [Installation & Usage](#installation--usage)
- [Dataset](#dataset)
- [Key Files](#key-files)
- [References](#references)

## Methodology
- **Data Source:** NASA CMAPSS FD001 dataset (simulated turbofan engine cycles)
- **Preprocessing:**
	- Feature selection and standardization
	- RUL labeling (fault if RUL < 20 cycles)
	- Class balancing using SMOTE
- **Model:** Quadratic Discriminant Analysis (QDA) with hyperparameter tuning (GridSearchCV)
- **Evaluation:**
	- Metrics: Accuracy, Precision, Recall, F1-score, AUC
	- Robustness tested by adding Gaussian noise
	- Visualizations: ROC curves, confusion matrices, feature importance

## Results
- **Test Accuracy:** 99%
- **Test Recall:** 94%
- **Test AUC:** 0.9955
- **Confusion Matrix:** Only 6 false negatives and 152 false positives on 13,096 test cycles
- **Feature Importance:** Key sensors (e.g., T30, P30, Wf_Ps30) are most predictive
- **Comparison:** Outperforms prior work (Xia et al. 2025) in scope and accuracy

## Installation & Usage
1. **Clone the repository:**
	 ```bash
	 git clone https://github.com/rofeeqshittu/qda-algorithm-for-fault-detection.git
	 cd qda-algorithm-for-fault-detection
	 ```
2. **Install dependencies:**
	 - Recommended: Use Google Colab (no local setup needed)
	 - For local use:
		 ```bash
		 pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
		 ```
3. **Run the notebook:**
	 - Open `QDA_algo_for_fault_detection_in_aircraft.ipynb` in Jupyter or Colab
	 - Upload the required data files: `train_FD001.txt`, `test_FD001.txt`, `RUL_FD001.txt`
	 - Execute cells sequentially

## Dataset
- **Source:** NASA CMAPSS FD001
- **Files Needed:**
	- `train_FD001.txt`
	- `test_FD001.txt`
	- `RUL_FD001.txt`
- **Description:** Simulated engine cycles, operational settings, and sensor measurements

## Key Files
- `QDA_algo_for_fault_detection_in_aircraft.ipynb`: Main analysis and code
- `README.md`: Project documentation

## References
See the project report for full references, including:
- NASA CMAPSS dataset documentation
- Xia et al. (2025), FAA standards, and related ML/aviation research

## License
This project is for academic and research purposes. Please cite appropriately if used.

---
For questions or collaboration, contact Shittu Rofeeq (U21CS1046).
