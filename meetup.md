# Meet Up Schedule 

In this section we want to track the Meet Up contents and information. 

## 02.06.2020 Kick-Off Meeting 

## 07.07.2020 Synthetic control in time series 

**Speaker:** [Sebastian Martinez](https://smartinez.co/)

**Abstract:** Synthetic control is a method for estimating *causal* effects (evaluate the effect of an intervention) in comparative case studies when there is only one treatment unit. The method chooses a set of weights for a group of corresponding units that produces an optimally estimated *counterfactual* to the unit that received the treatment. This unit is referred to as the “synthetic unit” and can be used to outline what would have happened to the treated unit had the treatment never occurred.

## 11.08.2020 Exploring [Facebook Prophet](https://facebook.github.io/prophet/) (Book Club)

<img src="images/sample_data_1_plot.png">

**Moderator:** [Aaron Pickering](https://www.linkedin.com/in/aaron-p-87a139175/)

**Descripton:** We want to discuss the capabilities and limitations of Facebook’s forecasting package *Prophet*. We want to work a concrete example: On the file `data/sample_data_1.csv` you can find (dummy) `sales` data (`2018-01-01` to `2021-06-30`). In addition there is a feature `media` which could be used as an external predictor. The objective is to create a time series forecasting model using [Facebook Prophet](https://facebook.github.io/prophet/). The forecasting window is 30 days. Here are some hints/steps for the challenge: 

1. Do an EDA on the sample data. 
2. Is there any clear seasonality or trend? 
3. Is the feature `media` useful for prediction? 
4. How do you evaluate model performance?
5. Can you estimate model uncertainty (credible intervals)? 

Try to generate predictions for the whole month of *July 2021*. We will provide the "true" values during the meetup so that we can all test our models. Again, this is not a competition, but rather a concrete use case to apply what we learn about Prophet. 

Please bring questions and suggestions to make the best out of this session!

## 08.09.2020 Introduction to sktime : A Unified Interface for Machine Learning with Time Series

**Speaker:** [Markus Löning](https://www.geog.ucl.ac.uk/people/research-students/markus-loning) (PhD Student @UCL)

**Abstract:** We present sktime, a new unified toolbox for machine learning with time series in Python. We provide state-of-the-art time series algorithms and scikit-learn compatible tools for model composition. The goal of sktime is to make the time series analysis ecosystem more usable and interoperable. In this talk, you'll learn about different time series learning tasks, how algorithms for one task can be used to help solve another one, sktime's key design ideas and our plans for the future.

**Resources:**
- MeeUp Code [https://github.com/mloning/intro-to-sktime-berlin-tsa-meetup-2020](https://github.com/mloning/intro-to-sktime-berlin-tsa-meetup-2020)
- GitHub [https://github.com/alan-turing-institute/sktime](https://github.com/alan-turing-institute/sktime)
- Paper [sktime: A Unified Interface for Machine Learning
with Time Series](http://learningsys.org/neurips19/assets/papers/sktime_ml_systems_neurips2019.pdf)

## 13.10.2020 Amazon DeepAR (Book Club)

**Moderator:** [Korbinian Kuusisto](https://kkuusisto.github.io/) (Co-Founder @ Kineo.ai)

**Abstract:** Probabilistic forecasting, i.e. estimating the probability distribution of a time series’ future given its past, is a key enabler for optimizing business processes. In retail businesses, for example, forecasting demand is crucial for having the right inventory available at the right time at the right place.

The prevalent forecasting methods in use today have been developed in the setting of forecasting individual or small groups of time series. In this approach, model parameters for each given time series are independently estimated from past observations. The model is typically manually selected
to account for different factors, such as autocorrelation structure, trend, seasonality, and other explanatory variables.

However, especially in the demand forecasting domain, one is often faced with highly erratic, intermittent or bursty data which violate core assumptions of many classical techniques, such as Gaussian errors, stationarity, or homoscedasticity of the time series.

Amazon's DeepAR is a forecasting method based on auto-regressive recurrent networks (LSTMs), which learns a global model from historical data of all time series in the data set. In their paper the authors demonstrate how by applying deep learning techniques to forecasting, one can overcome many of the challenges faced by widely-used classical approaches to the problem.

**Resources:**
- [DeepAR: Probabilistic forecasting with autoregressive recurrent networks](https://www.sciencedirect.com/science/article/pii/S0169207019301888)
- [Understanding LSTM Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- [Entity Embeddings of Categorical Variables](https://arxiv.org/abs/1604.06737)

**Remarks/Questions:***
- *Do you have a guideline when DeepAR would NOT be useful/appropriate?*
  > One big assumption that holds for all deep learning models as well as deepAR is that the distribution of the data does not change in the future. If that happens then of course DeepAR is not appropriate. Another issue is that if your problem has covariates which are not available in the time slots you are doing prediction then this method will not work. Also this method is uni variate method so if your problem is multivariate it will also not be appropriate. Finally due to the LSTM the sequence length might be an issue i.e. if you want to predict daily for 2 years for example. LSTMs suffer from forgetting for long time sequences and then also its not appropriate. In addition, data points must be regular in time (Kashif Rasul).

## 03.11.2020 Multi-variate Probabilistic Time Series Forecasting via Conditioned Normalizing Flows

**Speaker:** Dr. Kashif Rasul (Research Scientist @[Zalando SE](https://en.zalando.de/?_rfl=de))

**Abstract:**  I will present an overview of deep learning based probabilistic forecasting methods and then show how we can extend it to do multivariate probabilistic forecasting in an efficient manner by using Normalizing Flows. I will cover all the background material needed to understand these concepts as well so don't worry if you are new to them.

**Resources:**
- ArXiv: [Multi-variate Probabilistic Time Series Forecasting via Conditioned
Normalizing Flows](https://arxiv.org/pdf/2002.06103.pdf)

## 08.12.2020 Exploratory data analysis on time series data

<img src="python/fundamentals/images/beer_ma.png" height="400">

**Moderator:** BTSA Organizers

**Descripton:** We will have a hands on session on exploratory data analysis (EDA) for time series data. EDA depends of course on the data and the objective of the study. We will give some hints on how to start with it. Again, it is not set in stone, but a guiding principle.
- Missing values and data frequency ([notebook](https://github.com/juanitorduz/btsa/blob/master/python/fundamentals/notebooks/eda_part_1_viz_and_missing_values.ipynb)).
- Stationarity and correlation analysis ([notebook](https://github.com/juanitorduz/btsa/blob/master/python/fundamentals/notebooks/eda_part_2_correlations.ipynb)).
- Seasonality, decomposition, and outlier detection ([notebook](https://github.com/juanitorduz/btsa/blob/master/python/fundamentals/notebooks/eda_part_3_decomposition.ipynb)).

## 09.02.2021 Azure Automated Machine Learning for Time Series Forecasting

**Speaker:** [Dr. Francesca Lazzeri](https://developer.microsoft.com/en-us/advocates/francesca-lazzeri)

**Resources:**

- GitHub repository: https://github.com/FrancescaLazzeri/AutoML-for-Timeseries-Forecasting-Berlin-MeetUp
- [Article](https://www.oreilly.com/content/3-reasons-to-add-deep-learning-to-your-time-series-toolkit/ ) around classical methods vs deep learning methods for time series forecasting.


## 13.04.2021 Rocket and MiniRocket: Fast time series classification using convolutional kernels

**Speaker:** Angus Dempster

**Resources:** 

- Paper Links:
  - https://arxiv.org/abs/1910.13051 (ROCKET)
  - https://arxiv.org/abs/2012.08791 (MINIROCKET)
- GitHub repositories:
  - https://github.com/angus924/rocket
  - https://github.com/angus924/minirocket

## 18.05.2021 Unsupervised Pre-Training of Audio with Wav2vec

**Speaker:** [Ritwika Mukherjee](https://ritwika3.wixsite.com/mysite)

**Abstract:** 
Self-supervised methods for learning embedded feature spaces have increased in popularity over the last couple of years. These techniques allow for efficient representation learning despite complex high dimensional input spaces. In this session, we will explore the 'wav2vec' model developed by Facebook research and its applications in audio signal processing. The model has implications in speech, vastly reducing the need for annotated labels, and can be transferred across other time-series data.

**Resources:**
- [MeetUp Slides](/presentations/wave2vec/Wav2vec.pdf)
- [Demo Notebook](/python/wave2vec/wav2vec_demo.ipynb)

## 15.06.2021 Introduction [CausalImpact](https://google.github.io/CausalImpact/)

**Speaker:** [Munji Choi](https://www.linkedin.com/in/munjichoi/)

**Resources**
- [Notebook & Data](/python/CausalImpact)

## 06.07.2021 Forecasting practitioners: What can we learn from Kaggle Competitions?

**Speaker:** [Thomas Bierhance](https://www.linkedin.com/in/datenzauberai/)

**Abstract:** Although Kaggle contests are not directly comparable to a real-life task for a forecasting practitioner, the contests are closer to reality than many of the standard data sets found in the scientific literature. They are therefore a goldmine of practice-relevant ideas. Thomas explains the lessons learned from various Kaggle competitions, what needs to be considered when using them in practice, and what loose ends he believes still exist.

**Resources**
- [Presentation](presentations/forecast_kaggle_tips/Forecast%20practitioners%20What%20can%20we%20learn%20from%20Kaggle%20competitions.pdf)

## 07.09.2021 Introduction to Time Series Forecasting: Classical Statistical Methods

<img src="python/intro_forecasting/images/unobserved_components_predictions.png">

**Abstract:** In this session we will explore three classical time series forecasting methods:

  - Exponential Smoothing (Aaron Pickering)
  - ARIMA Models (Sebastian Martinez)
  - State Space Models (Juan Orduz)

We will have 20 min session for each method focusing on explaining the main idea behind it through examples. No prior knowledge is required.

Recommended reference: Forecasting: Principles and Practice
by Rob J Hyndman and George Athanasopoulos: [https://otexts.com/fpp3/](https://otexts.com/fpp3/) Chapters 8 and 9.

You can find the notebooks of the session [here](/python/intro_forecasting/). In addition, here is a summary article on [Introduction to Exponential Smoothing](https://btsa.medium.com/introduction-to-exponential-smoothing-9c2d5909a714).

## 12.10.2021 Temporal Point Processes for Modeling Continuous-time Event Data

**Speaker**: [Oleksandr Shchur](https://shchur.github.io/)

**References:**
  - [MeetUp Presentation](/presentations/temporal_point_processes/tpp_presentation.pdf)
  - [Neural Temporal Point Processes: A Review](https://arxiv.org/abs/2104.03528)
  - Blog post from [Oleksandr Shchur](https://shchur.github.io/):
    - [Temporal Point Processes 1: The Conditional Intensity Function](https://shchur.github.io/blog/2020/tpp1-conditional-intensity/)
    - [Temporal Point Processes 2: Neural TPP Models](https://shchur.github.io/blog/2021/tpp2-neural-tpps/)
  - Python packages related to TPP:
    - [tick](https://x-datainitiative.github.io/tick/)
    - [pyhawkes](https://github.com/slinderman/pyhawkes)

## 09.11.2021 Using ARIMA models to make causal statements

**Speaker**: [Dr. Fiammetta Menchetti](https://scholar.google.com/citations?user=o1dMQ88AAAAJ&hl=it) and [Eugenio Palmieri](https://palmierieugenio.github.io/)

**Abstract:**  In this talk we will provide an overview of C-ARIMA, an approach based on ARIMA models that can be used to make causal statements under the potential outcomes framework. After a brief description of the methodology, we will have a practical session on a real data set where we will illustrate the use of the CausalArima R package, see [FMenchetti/CausalArima](https://github.com/FMenchetti/CausalArima).

## 15.02.2022 Time Series Bootstrapping

**Speaker:** [Dr. Tom Kealy](https://github.com/TomKealy)

**Speaker:** Dr. Tom Kealy, Senior Data Scientist at HelloFresh

**Abstract:** Bootstrapping is a common non-parametric technique which uses resampling with replacement to estimate the distribution of a test statistic. Fatally, for time series methods, bootstrapping relies on the exchangeability of data points for statistical analysis consistency. This talk will introduce methods for bootstrapping time series data, with a particular focus on the Maximum Entropy Bootstrap family of algorithms to estimate distributions of test statistics for time series data.

## 15.03.2022 An Introduction to Temporal GNNs

**Speaker:** [Flavio Morelli](https://flaviomorelli.com/)

**Abstract:** Graph Neural Networks (GNNs) make it possible to apply deep learning methods to graph data. By taking into account the geometric structure of the graph, it is possible to improve model performance compared to more classical methods of graph analysis. Some examples of data that have a natural graph structure include knowledge graphs, chemical compounds, social and telecommunication networks. However, classical GNNs can only be applied to static graphs. This talk will introduce temporal GNNs, which can be applied to graphs changing through time. We will discuss the different flavors of temporal GNNs and the specific challenges that arise when dealing with dynamic graphs. 

**References:**

- **Slides:** [Here](https://github.com/flaviomorelli/talks/blob/main/temporal_gnn_introduction/GNN_intro_plus_temporal.pdf)

- [Rozemberczki et al. (2021)](https://arxiv.org/pdf/2104.07788.pdf)
- [Rossi et al. (2020)](https://arxiv.org/pdf/2104.07788.pdf)


## 05.04.2022 Modern Time Series Analysis with [STUMPY](https://stumpy.readthedocs.io/en/latest/) 

**Speaker:** [Dr. Sean Law](https://seanlaw.github.io/)

**Abstract:** [STUMPY](https://stumpy.readthedocs.io/en/latest/) is a powerful and scalable Python library that efficiently computes something called the matrix profile which can be used for a variety of time series data mining tasks. In this talk, we'll cover all of the background necessary for understanding how to leverage matrix profiles to automatically find patterns/anomalies in your time series data.

## 10.05.2022 Probabilistic energy forecasting: successes and challenges

**Speaker:** [Dr. Jethro Browell](http://www.jethrobrowell.com/)

**Abstract:** Energy systems are evolving rapidly as they decarbonize, consequences of which include an increasing dependence on weather and new consumer (and producer) behaviours. As a result, all actors in the energy sector are more reliant than ever on short-term forecasts, from the National Grid to me and (maybe) you. Furthermore, in operate as economically as possible and maintain high standards of reliability, forecast uncertainty must be quantified and managed. This seminar will introduce energy forecasting, highlight statistical challenges in this area, and present some recent solutions including forecasting extreme quantiles and modelling time-varying covariance structures.

## 14.06.2022 Open Source Time-Series Forecasting

**Speaker:** Federico Garza (Co-founder: https://github.com/Nixtla/nixtla)

**Abstract:** Open source time series forecasting with the Nixtla library.

## 07. 2022 - Taking a break for summer 

**Speaker:** Work Life Balance 

## 13.09.2022 TBD **[POSTPONED]**

**Speaker** Aaron Pickering (Co-founder http://seenly.io)

**Abstract:** TBD

## 08.11.2022 Intro to QuestDB Time Series Database

**Speaker** Javier Ramirez (https://es.linkedin.com/in/ramirez)

**Abstract** Time Series forecasting and modelling is fun, but capturing time-series data and dealing with large volume datasets not so much.
In this talk we will introduce QuestDB, an Apache 2.0 licensed database specialised in time-series. We will see how QuestDB can help ingesting, interactively querying, downsampling or augmenting your data. Since QuestDB is postgreSql-compatible, we can interact easily using python with or without Pandas. We will run a demo using QuestDB and skforecast to illustrate how QuestDB can be integrated to your data science workflows.

## 10.01.2023 Uncertainty Estimation in Time Series with Neural Processes

**Speaker** Xuesong Wang (https://xuesongwang.github.io/)

**Abstract** TBD

## 07.02.2023 Tenuous Relations and Time Series Analysis in PyMC

**Speaker** Nathaniel Forde

**Abstract** We'll discuss the nature of lagged impact between multiple time series and sketch some details about how we can implement and use VAR models and their hierarchical variants to quantify the nature of these relationships.
