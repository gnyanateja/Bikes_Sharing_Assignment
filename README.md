# Bike Demand Sharing Analysis using Linear Regression with Hybrid approach (RFE & Manual)
> To understand the factors affecting the demand for shared bikes like which variables are significant in predicting the demand for shared bikes & well those variables describe the bike demands


## Table of Contents
* [Project Info](#project-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## Project Information

### 1. Business Problem Statement
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

They have to understand the factors on which the demand for these shared bikes depends. Specifically, they want to know which variables are significant in predicting the demand for shared bikes and how well those variables describe the bike demands.

We will use Linear Regression with Hybrid approach to solve this problem statement.

### 2. Dataset
1. You can observe in the dataset that some of the variables like 'weathersit' and 'season' have values as 1, 2, 3, 4 which have specific labels associated with them. These numeric values associated with the labels may indicate that there is some order to them - which is actually not the case. So, it is advisable to convert such feature values into categorical string values before proceeding with model building.
 
2. You might notice the column 'yr' with two values 0 and 1 indicating the years 2018 and 2019 respectively. At the first instinct, you might think it is a good idea to drop this column as it only has two values so it might not be a value-add to the model. But in reality, since these bike-sharing systems are slowly gaining popularity, the demand for these bikes is increasing every year proving that the column 'yr' might be a good variable for prediction. So think twice before dropping it. 



## Technologies Used
- numpy - 1.23.5v
- pandas - 1.5.3v
- matplotlib.pyplot - 3.7.0v
- seaborn - 0.12.2v
- sklearn - 1.2.1v
- statsmodels - 0.13.5v
- python - 3.10.12v


## Conclusions
The equation of our best fitted line is: 
```groovy
 cnt = (0.231) * yr + (0.046) * workingday + (0.467) * atemp + (-0.28) * hum + (-0.121) * windspeed + (-0.151) * spring + (0.078) * winter + (-0.059) * Nov + (0.074) * Sep + (0.051) * Sunday + (-0.18) * Light Snow and Rain + (0.346)
```
1. I have observed that the values of R-Sqaured and adj R-Sqaured of both train and test dataset are more than 80% of bike demand. 
2. The coeffiencients of the variables explains the factors effecting the bike demand. 
3. I have also proved all the assumptions taken on linear regression. 
4. The top features that contributes significantly towards bike demands w.r.t model are:
     - Feel Like Temperature
     - Humidity
     - Year
     - Weathersit : Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds

So it is recommended to consider these variables while planning to achieve maximum bikes demand.


## Acknowledgements

- I would like to thank [Dinesh J Babu](https://www.linkedin.com/in/dinesh-babu-jayagopi-22a706/) for his explanation on Linear Regression.
- References for seaborn plots are taken form [Tutorials Point](https://www.tutorialspoint.com/seaborn/seaborn_tutorial.pdf)
- References for linear regression assumptions are taken from [ML Mind](https://machinelearningmind.com/2019/10/27/assumptions-of-linear-regression-how-to-validate-and-fix/).


## Contact
Created by [@gnyana_teja](https://www.linkedin.com/in/somanchi-gnyana-teja/) 

Feel free to contact me 👍
