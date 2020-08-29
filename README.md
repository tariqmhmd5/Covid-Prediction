# Univariate LSTM Model

**Introduction**

In late December of 2019, a cluster of pneumonia cases of unknown causes was reported in Wuhan city of Hubei Province in China. Later it was concluded that the reason behind this is a virus that belongs to the β - Coronavirus family which can severely affect the lungs of victims which causes difficulty in breathing. The World Health Organization named this coronavirus as COVID-19 in January 2020. The spread rate of this virus is very high and because of this various countries applied lockdown for a few months to reduce mobility. In this Repository, the study mainly focuses on the prediction of cases in India in August for the upcoming 60 days.

---
## **LSTM Data Prepration:**
In LSTM models you cannot directly feed the data into model. LSTM's takes 3D array as input so we have to convert the data into mini batches. To prepare these batches iterate through the data and create batches of n shape in which last element is its label. As shown below.

<img src="https://raw.githubusercontent.com/tariqmhmd5/Covid-Prediction/master/Diagrams/Data%20Prepration%20Diagram.jpg"
     style="float: left; margin-right: 10px;" />





## **LSTM Model:**

<img src="https://raw.githubusercontent.com/tariqmhmd5/Covid-Prediction/master/Diagrams/Model%20Diagram.jpg"
     style="float: left; margin-right: 10px;" />

The architecture of the LSTM model which is used is given in above. It contains a single LSTM layer in which 3D input is passed, these inputs are passed through the LSTM layer which contains 100 units, then it is passed to a dense layer that converges the output and gives a Numpy array of shape (None, 1)  as output.

## **Future Prediction:**
<img src="https://raw.githubusercontent.com/tariqmhmd5/Covid-Prediction/master/Diagrams/Prediction%20Diagram.jpg"
     style="float: left; margin-right: 10px;" />

Above picture shows how the forecasting is done. The problem is converted to a supervised learning task in which batches of 20 data points each is treated as the feature and the last element in it as the label then fed to the LSTM model to learn the trend in the graph. After model training, In above fig (1) the last batch is used to predict the value, (5) then the first value from the batch is popped and (4) predicted value is added at the end of batch (2) to predict the next value and so on (3) the forecasting for the next 30 days is done.


---
## **Result**

<img src="https://raw.githubusercontent.com/tariqmhmd5/Covid-Prediction/master/Diagrams/image.png"
     style="float: left; margin-right: 10px;" />
