# 캡스톤 프로젝트 예시 데이터
데이터 구성과 feature에 대한 자세한 설명은 출처 링크에 기재되어 있습니다.
EDA 및 전처리에 있어서 kaggle/dacon 링크의 여러 code를 참고하여 인사이트를 얻는 것을 추천드립니다.

## 2025 전력사용량 예측
https://dacon.io/competitions/official/236531/overview/description

Dataset Info.

1. 10개 유형, 100개 건물의 전력소비량 데이터(1시간주기, ‘24.6.1～8.31)
2. 기상데이터
3. 건물개요(면적, 태양광·ESS 용량 등)

* 공공, 학교, 백화점, 병원, 아파트, 호텔 등

* 기온, 강수량, 풍속, 습도, 일조, 일사

1. train.csv

85일 분량의 데이터
train 데이터 : 100개 건물들의 2024년 06월 01일부터 2024년 08월 24일까지의 데이터
일시별 기온, 강수량, 풍속, 습도, 일조, 일사 정보 포함
전력사용량(kWh) 포함


2. building_info.csv

100개 건물 정보
건물 번호, 건물 유형, 연면적, 냉방 면적, 태양광 용량, ESS 저장 용량, PCS 용량


3. test.csv

test 데이터 : 100개 건물들의 2024년 08월 25일부터 2024년 08월 31일까지의 데이터
일시별 기온, 강수량, 풍속, 습도의 예보 정보

## Time-Series of Industrial Boiler Operations
https://www.kaggle.com/datasets/nikitamanaenkov/time-series-of-industrial-boiler-operations/data

About Dataset
This dataset contains high-frequency time-series data collected from a coal-fired industrial boiler operating in a chemical plant in Zhejiang, China. The boiler is equipped with multiple sensors capturing parameters such as pressure, temperature, flow rate, and oxygen levels. The dataset reflects a real-world industrial scenario, where 8.6% of the data represents abnormal operating conditions (outliers), making it particularly suitable for long-tailed distribution studies, anomaly detection, and robust forecasting tasks in industrial time-series modeling.

## Weather Long-term Time Series Forecasting
https://www.kaggle.com/datasets/alistairking/weather-long-term-time-series-forecasting/data

Dataset Description
Weather is recorded every 10 minutes throughout the entire year of 2020, comprising 20 meteorological indicators measured at a Max Planck Institute weather station. The dataset provides comprehensive atmospheric measurements including air temperature, humidity, wind patterns, radiation, and precipitation. With over 52,560 data points per variable (365 days × 24 hours × 6 measurements per hour), this high-frequency sampling offers detailed insights into weather patterns and atmospheric conditions. The measurements include both basic weather parameters and derived quantities such as vapor pressure deficit and potential temperature, making it suitable for both meteorological research and practical applications. You can find some initial analysis using this dataset here: ["Weather Long-term Time Series Forecasting Analysis"](https://www.kaggle.com/code/alistairking/weather-long-term-time-series-forecasting-analysis).

## CMAPSS Jet Engine Simulated Data
https://www.kaggle.com/datasets/palbha/cmapss-jet-engine-simulated-data

Overview:
The NASA CMAPSS dataset consists of simulated jet engine sensor readings generated using the Commercial Modular Aero-Propulsion System Simulation (CMAPSS). It’s widely used for research in prognostics, health management, and remaining useful life (RUL) estimation.

Contents:
Training Data: Contains engine cycle information and sensor measurements.
Test Data: Engine cycle data without RUL labels, to be predicted.
RUL Values: Ground truth remaining useful life for the test engines.

Applications:
Ideal for time-series analysis, anomaly detection, and developing machine learning models focused on predictive maintenance.

Attribution:
Data provided by NASA’s CMAPSS simulation. For more details, please refer to the NASA Data Portal.
https://data.nasa.gov/Aerospace/CMAPSS-Jet-Engine-Simulated-Data/ff5v-kuh6/about_data

## Electricity Transformer Dataset(ETT-small)
https://github.com/zhouhaoyi/ETDataset

We donated two years of data, in which each data point is recorded every minute (marked by m), and they were from two regions of a province of China, named ETT-small-m1 and ETT-small-m2, respectively. Each dataset contains 2 year * 365 days * 24 hours * 4 times = 70,080 data point. Besides, we also provide the hourly-level variants for fast development (marked by h), i.e. ETT-small-h1 and ETT-small-h2. Each data point consists of 8 features, including the date of the point, the predictive value "oil temperature", and 6 different types of external power load features.

Specifically, the dataset combines short-term periodical patterns, long-term periodical patterns, long-term trends, and many irregular patterns. We firstly give an overall view in Figure 1, and it shows evident seasonal trends. To better examine the existence of long-term and short-term repetitive patterns, we plot the autorcorrelation graph for all the variables of the ETT-small-h1 dataset in Figure 2. The blue line in the above is the target 'oil temperature', and it maintains some short-term local continuity. However, the other variables (power load) shows short-term daily pattern (every 24 hours) and long-term week pattern (every 7 days).

## CWRU Bearing Dataset
https://engineering.case.edu/bearingdatacenter

해당 데이터는 timestamp는 없지만 각 결함 베어링에 대한 실험값 데이터가 존재하는 sequential data 입니다.
모델에 input으로 일정 길이의 시퀀스가 들어왔을 때 어떤 종류의 결함인지를 분류하는 task를 수행 가능합니다.

1. CWRU_Bearing_Numpy

https://github.com/srigas/CWRU_Bearing_NumPy

원본 .mat 데이터를 npz로 변환한 데이터
해당 데이터를 활용해서 진행하는 것을 권장

2. CWRU_Bearing_2048window_preprocessed

https://www.kaggle.com/datasets/brjapon/cwru-bearing-datasets

원본 .mat 데이터를 2048개 window size로 잘라 통계량을 계산하여 라벨링을 한 데이터로 전처리에 참고