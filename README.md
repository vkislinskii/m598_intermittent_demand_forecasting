## Improving intermittent demand forecasting with gradient boosting

#### Overview
This is a thesis project for the Gisma University of Applied Sciences. 
The goal is to investigate the limitations of using exogenous features in the intermittent demand prediction task (as the specialized algorithms are univariate) and whether the gradient boosting models could improve the forecast.
To do this, it compared the predictions from statistical (ETS), specialized (SBA, TSB, ADIDA, IMAPA), gradient boosting regression (XGBoost, CatBoost), and the ensemble (IMAPA + CatBoost) approaches.

#### Dataset
For the project, two referenced datasets were used. 
The first is the M5 dataset from the M5 competition, held by the University of Nicosia, and it is [publicly available at Kaggle](https://www.kaggle.com/competitions/m5-forecasting-accuracy/data). The second is the Royal Air Force (RAF) dataset and is available in [this repository](https://github.com/vkislinskii/m598_intermittent_demand_forecasting/tree/de5ab6503847adf61e2fad819dbc93fcd5be187e/data).

#### How to Use
* Or open the "RAF.ipynb" or "M5.ipynb" file in Google Colab by simply clicking the blue button on the first line of the Jupyter Notebook file

* Or clone the repository
  
```sh
git clone https://github.com/vkislinskii/m598_intermittent_demand_forecasting.git
```

Install all the needed packages

   ```sh
   pip install pandas
   pip install numpy
   pip install matplotlib
   pip install sklearn
   pip install statsforecast
   pip install xgboost
   pip install catboost
   pip install optuna
   ```
Finally, open either of the two projects in Jupyter Notebook 

#### Results
* Comparing single models, ADIDA and IMAPA performed the best on the different datasets, and gradient boosting models performed worse than specialized approaches.
* The CatBoost classifier improved the IMAPA model’s performance by up to 10% according to the RMSSE metric in the combination, showing that even a simple ensemble performs better than any single model.
