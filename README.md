# Store Item Demand Forecasting Challenge on Kaggle (CZ4041 Project AY2020-21 Semester 2)

### Organisation of Contents
Contents are organised such that they can be dropped in onto Kaggle platform and run as-is without modifications required.
- Output files `submission.csv` created can be found in the respective notebook folders

### Environment Setup
It is recommended to use a virtual environment to contain required packages for running the notebooks.
- Alternatively, running them on Kaggle will be easier with no/minimal package modifications.
- Packages required:
	- `statsmodels`
	- `xgboost`
	- `scikit-learn=0.23.2`
		- This requirement must be satisfied even on Kaggle kernels.
	- `scikit-optimize`
	- `pystan` and `fbprophet`
	- `tensorflow` for `pip` or `tensorflow-gpu` for `conda`

### Notebooks
It is recommended to run the notebooks in order: 1 - 6; Jupyter is required to run `.ipynb` notebooks.

Packages required for each notebook are listed as follows:
1. SARIMAX
- `statsmodels`
	- `conda install -c conda-forge statsmodels` or `pip install statsmodels`
	
2. Custom Predictor referencing a Kaggle submission by [XYZT](https://www.kaggle.com/thexyzt/keeping-it-simple-by-xyzt)

3. XGBoost with Feature Engineering
- `xgboost`
	- version 0.23.2 for `scikit-learn` is required to avoid deprecated param iid error in `scikit-optimize` version 0.81
	- `conda install scikit-learn==0.23.2` or `pip install scikit-learn==0.23.2`
	- `conda install scikit-optimize` or `pip install scikit-optimize` 
	- `conda install -c conda-forge xgboost` or `pip install xgboost`
	
4. [Prophet](https://facebook.github.io/prophet/docs/quick_start.html) - Time Series Forecasting model by `facebook`
- `Prophet`
	- not available on `conda`
	- `pip install pystan`; `pystan` is required prior to installing `fbprophet`
	- `pip install fbprophet`
	
5. Neural Network - simple NN model in Tensorflow
- `Tensorflow`
	- `conda install tensorflow-gpu` or `pip install tensorflow`

6. RandomForestRegressor with additional features engineered in `3_xgboost.ipynb`
- `scikit-learn`
	- version 0.23.2 for `scikit-learn` is required to avoid deprecated param iid error in `scikit-optimize` version 0.81
	- `conda install scikit-learn==0.23.2` or `pip install scikit-learn==0.23.2`