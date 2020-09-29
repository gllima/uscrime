uscrime
==============================

<a id="ch2_1"></a>
<div style="font-family:verdana; word-spacing:1.5px;">
    <h1 id="italic">
        Data Ingestion and Preparation
    </h1>
</div>
Criminologists are interested in the effect of punishment regimes on crime rates. This has been studied using aggregate data on 47 states of the USA for 1960. The data set contains the following columns:

| Variable 	| Description 	|
|-	|-	|
| M 	| percentage of males aged 14–24 in total state population 	|
| So 	| indicator variable for a southern state 	|
| Ed 	| mean years of schooling of the population aged 25 years or over 	|
| Po1 	| per capita expenditure on police protection in 1960 	|
| Po2 	| per capita expenditure on police protection in 1959 	|
| LF 	| labour force participation rate of civilian urban males in the age-group 14-24 	|
| M.F 	| number of males per 100 females 	|
| Pop 	| state population in 1960 in hundred thousands 	|
| NW 	| percentage of nonwhites in the population 	|
| U1 	| unemployment rate of urban males 14–24 	|
| U2 	| unemployment rate of urban males 35–39 	|
| Wealth 	| wealth: median value of transferable assets or family income 	|
| Ineq 	| income inequality: percentage of families earning below half the median income 	|
| Prob 	| probability of imprisonment: ratio of number of commitments to number of offenses 	|
| Time 	| average time in months served by offenders in state prisons before their first release 	|
| Crime 	| crime rate: number of offenses per 100,000 population in 1960 	|
<div style="color:white;
       display:fill;
       border-radius:5px;
       background-color:#90C820;
       font-size:110%;
       font-family:Verdana;
       letter-spacing:0.5px">
    <p style="padding: 10px;
          color:#333337;">
        Since we are dealing with a very small datasets, we will explore in some techniques to handle very small datasets in this note book in order to avoid overfitting.
So we will (1) Use simple models with barely none tuning, (2) Be aware for the outliers, (3) Select the features and avoid missing values and weak correlation and (4) Combine models for the final submission.
    </p>
</div>


<h1 id="t7">References</h1>

**Overfitting:**
* IRIC's Bioinformatics Platform. Overfitting and Regularization. https://bioinfo.iric.ca/overfitting-and-regularization/

**Models:**
* scikit-learn. LogisticRegression. https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html
* Tscikit-learn. Random Forest. https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html
* XGBoost. XGBoost Parameters. https://xgboost.readthedocs.io/en/latest/parameter.html

**Feature selection:**
* scikit-learn. Feature selection. https://scikit-learn.org/stable/modules/feature_selection.html

**Ensemble Models**
* Tang, J., S. Alelyani, and H. Liu. "Data Classification: Algorithms and Applications." Data Mining and Knowledge Discovery Series, CRC Press (2015): pp. 498-500.


Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original us crime, immutable data dump.
    │
    ├── docs               <- The presentation is placed here !!!!
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
