![This is an image](https://iea.imgix.net/b76ee6a7-ff18-4ee8-a557-5d4a5cbf421d/shutterstock_612227351.jpg?auto=compress%2Cformat&fit=min&q=80&rect=0%2C2105%2C4578%2C3047&w=1280&h=852&fit=crop&fm=jpg&q=70&auto=format)
* Electricity is a basic part of nature and it is one of our most widely used forms of energy. We get electricity, which is a secondary energy source, from the conversion of other sources of energy, like coal, natural gas, oil, nuclear power and other natural sources, which are called primary sources. Many cities and towns were built alongside waterfalls (a primary source of mechanical energy) that turned water wheels to perform work. Before electricity generation began slightly over 100 years ago, houses were lit with kerosene lamps, food was cooled in iceboxes, and rooms were warmed by wood-burning or coal-burning stoves. Beginning with Benjamin Franklin's experiment with a kite one stormy night in Philadelphia, the principles of electricity gradually became understood. In the mid-1800s, everyone's life changed with the invention of the electric light bulb. Prior to 1879, electricity had been used in arc lights for outdoor lighting. The lightbulb's invention used electricity to bring indoor lighting to our homes.
##  Data 
> * https://datahub.io/machine-learning/electricity
We read in data for the last 30 years. It represents electricity movement beetwen Canada and USA.
It has 7 columns:
    * Period
    * Activity 
    * Source 
    * Destination
    * Energy 
    * Total Value
    * Price
## 1. Problem statement
The need for electricity changes rapidly every year. With the advancement of tehnology, the number of electronic devices grows every year, and need for producing and importing aditional electricity grows with it. With help of our data we are going to explore the relation beetween Canada and USA,
and try to predict the future depedency. We are going to focus Canada's electric grid and try to explore if there are on the way to become self-sufficient.

## 2. Data wrangling
The most important columns for our project are Price, Energy and Total Value. We will check for possible outliers and missiing values and try to sort all the data properly.
![Price](https://user-images.githubusercontent.com/77463436/152405840-f71f61c0-a935-45f0-897c-5d853c77a6c2.png)
![energy](https://user-images.githubusercontent.com/77463436/152405934-28210803-c85e-4de0-9a2b-4dbd75557af3.png)
![total value](https://user-images.githubusercontent.com/77463436/152405970-2b5e5bda-ee90-4499-8f9f-431909cf9739.png)

## 3. EDA
Also we need to create adittional data visualization to check possible value trends.
![EDA](https://user-images.githubusercontent.com/77463436/152406598-64084412-931b-4f2f-9d7b-bfd81fc6c103.png)
![Total value EDA](https://user-images.githubusercontent.com/77463436/152406638-d4f534a9-ca11-4d84-a7cb-0dd2cb0bb7dd.png)
![Total value 2 eda](https://user-images.githubusercontent.com/77463436/152406774-e3f98a70-5dc0-4128-9481-f5c5c5309038.png)
![Price EDA](https://user-images.githubusercontent.com/77463436/152406815-d893f740-01ba-4348-82ef-9327bdf4b990.png)

## 4. Pre-processing and Training Data Development/Modeling
For our Pre-processing we will need to group values from cities in USA, in 4 different groups. And every group is going to represent an area in USA.
We have South, Middle, West and NorthEast area.
![CANADA NET](https://user-images.githubusercontent.com/77463436/152408876-7e7e67b9-d004-4a12-a53a-0c1240b1cd20.png)
![SOUTH](https://user-images.githubusercontent.com/77463436/152408911-b76ee1f6-b2d7-43aa-9436-eaaffa55d345.png)
![MIDDLE](https://user-images.githubusercontent.com/77463436/152408943-6ace549a-ce3a-4332-935e-ff466c9c5390.png)
![NORTHEAST](https://user-images.githubusercontent.com/77463436/152408990-e5511c18-9cfa-4d8f-84fe-603e504a695f.png)
![WEST](https://user-images.githubusercontent.com/77463436/152409044-3e923d8d-3393-4f5e-8450-94e80a4ff67a.png)

 ## 5. Machine learning - Multiple linear regression
 In out model we used different areas in USA to predict, electricity net value in CANADA.
 The best model with biggest is accuracy is the linear model that uses electricity net value from NorthEast area of USA, for a feature.
 ![South Predict](https://user-images.githubusercontent.com/77463436/152409417-f9fc8834-1dce-49e5-ab63-63a28b1aa908.png)
![MIDDLE PREDICT](https://user-images.githubusercontent.com/77463436/152409454-5c732a22-f3ec-4bbb-a0c9-78c5daa1bb8c.png)
![East predict](https://user-images.githubusercontent.com/77463436/152409525-25312d85-071b-4d19-8e53-7cde9ca0677f.png)
![West predict](https://user-images.githubusercontent.com/77463436/152409566-1f82884a-a10d-4db3-9889-a0020eab5069.png)
