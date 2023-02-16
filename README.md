### Back up my notebooks on Google Colab

After discovering the usefulness of Google Colab, I ran some small programs there as practice. Some of them were interesting, so I moved them to [this GitHub repository](https://github.com/YorkJong/Colab) to share.

These notebooks are currently divided into the following categories:

* Pytorch Tutorial Series
* Visualizing Stocks

---

### Pytorch Tutorial Series

This Colab notebook files of PytorchTutorial series includes the following:

* [PytorchTutorial2_Regression.ipynb](https://github.com/YorkJong/Colab/blob/3c8181e391d9f4215db19717c3473c8e4894224d/PytorchTutorial2_Regression.ipynb)
* [PytorchTutorial3_Classfication.ipynb](https://github.com/YorkJong/Colab/blob/3c8181e391d9f4215db19717c3473c8e4894224d/PytorchTutorial3_Classfication.ipynb)
* [PytorchTutorial6_min_batch.ipynb](https://github.com/YorkJong/Colab/blob/3c8181e391d9f4215db19717c3473c8e4894224d/PytorchTutorial6_min_batch.ipynb)
* [PytorchTutorial7_CNN.ipynb](https://github.com/YorkJong/Colab/blob/3c8181e391d9f4215db19717c3473c8e4894224d/PytorchTutorial7_CNN.ipynb)

I initially copied and pasted these files from [Professor Mofan's teaching website](https://juejin.cn/search?query=莫凡Pytorch教程&type=0) to Colab for code verification and familiarization with PyTorch. 

After performing a lot of refactoring, I also added new features for them.The original example code's visualization was through Matplotlib, to better compatibility with Colab, I added a Plotly version. Both are side by side, allowing for easy comparison.

The following chart is the final result from [PytorchTutorial7_CNN.ipynb](https://github.com/YorkJong/Colab/blob/3c8181e391d9f4215db19717c3473c8e4894224d/PytorchTutorial7_CNN.ipynb), which is a CNN model trained using PyTorch in Google Colab to recognize the Arabic numerals 0 to 9 in the MNIST dataset. During the process, it was dimensionality reduced using TSNE and visualized using Plotly.

![PT7_VisualizeLastLayer](https://user-images.githubusercontent.com/11453572/216806724-e583279f-7754-4de2-bc50-90d966ca1d8f.png)

---

### Visualizing Stocks

Initially, just for fun, I gave ChatGPT a simple task, to write a program to draw basic charts such as candlesticks, moving average lines, and volume. However, after ChatGPT struggled for a whole day, it still couldn't produce accurate results. So I had to roll up my sleeves, with the assistance of ChatGPT, and spend two days studying Plotly to finally achieve the current result. The following is its Colab notebook file.

* [ViStock.ipynb](https://github.com/YorkJong/Colab/blob/main/ViStock.ipynb)
  * Please also refer to [vistock_demo.ipynb](https://github.com/YorkJong/vistock/blob/main/examples/vistock_demo.ipynb) which is a demonstration of the extending project.

I retrieve the historical data of a stock using [yfinance](https://pypi.org/project/yfinance/), after obtaining the stock's [DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html) table, I plot related charts using both [mplfinance](https://github.com/matplotlib/mplfinance) (a Matplotlib utilities for the visualization, and visual analysis, of financial data) and [Plotly](https://plotly.com/python/). I also tried using [TA-Lib](https://github.com/TA-Lib/ta-lib-python) with mplfinance to plot technical analysis indicators.

As an example, below are the TSLA's price and volume accumulation charts so-called Volume Profile (or Price-by-Volume), the first one is plotted using mplfinance and the latter two  are plotted using Plotly.

![TSLA_20230203_VolumeProfile_mpl](https://user-images.githubusercontent.com/11453572/216813644-fcc4aa48-af00-47a5-af72-d79821c96b89.png)
![TSLA_20230207_VolumeProfile_Plotly2s](https://user-images.githubusercontent.com/11453572/217300613-ba824f59-4595-4aac-bf7f-051094b02b32.png)
![TSLA_20230203_VolumeProfile_Plotly](https://user-images.githubusercontent.com/11453572/216813652-690de806-f5c2-40d0-9692-a3be27fe0e57.png)








