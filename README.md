# Transformer for stock price prediction

## Installation
- Install pytorch 
- Install numpy by running ```pip install numpy```.
- Install os by running ```pip install os```.
- Install csv by running ```pip install csv```.
- Install matplotlib by running ```pip install matplotlib```.
- Install argparse by running ```pip install argparse```.
- Install pandas by running ```pip install pandas```.
- Install pandas_datareader by running ```pip install pandas-datareader```.
- Install yfinance by running ```pip install yfinance```.
- Install math by running ```pip install python-math```.
- Install sklearn by running ```pip install scikit-learn```.


## Running
run ```main.py```.


## Output
종목별 예측 결과, Time split별 결과와 그래프


## TransformerEncoder
자연어 처리에 뛰어난 성과를 보인 Transformer 구조에서
Encoder 구조만을 부분적으로 차용, Time series 데이터에 이용함.

- TransformerEncoder

![AttentionEncoder](https://user-images.githubusercontent.com/76574427/139543290-4f952916-39b6-411e-9ba1-f228b74b450d.PNG)



## Experiment setting
1. Data split

![nasted_cv](https://user-images.githubusercontent.com/76574427/139542833-d78683f0-293b-4549-8b3a-c67d19e77f3e.PNG)


데이터 분할방식으로는 Nasted Time series Cross validation을 사용.

2. metric
- MAE
- RMSE
- MAPE

3. Deeplearning library
- pytorch


## Datasets
```
from pandas_datareader import data as pdr
import yfinance as yfin

yfin.pdr_override()
self.data = pdr.get_data_yahoo(self.symbol, start=self.start, end=self.end)
```
pandas_datareader를 이용하여 야후 파이낸스에 있는 데이터셋을 위와같은 방법으로 불러올 수 있음.

yahoofinance에서 제공되는 정보(Open, Close, High, Low, Volume, AdjClose)를 불러옴.

## Citations
```
@InProceedings{Ashish Vaswani_2017_NIPS,
author = {Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Lukasz Kaiser, Illia Polosukhin},
title = {Attention Is All You Need},
booktitle = {Conference on Neural Information Processing Systems (NIPS 2017)},
month = {December},
year = {2017}
}
```
