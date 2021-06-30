This is my small challange for MLH INIT 2022 Day3 and I have started my first project in data science with this.
 # Commands Description:
 ### 1. 
 ```
 weather = pd.read_csv('weather.csv')
 ```
***read_csv*** is an important pandas function to read csv files like my ***weather.csv*** file and do operations on it.

### 2. 
```
weather.head()
```

***head()*** returns the first n rows for the object based on position.

### 3. 
```
weather.info()
```
extract the weather info using the JSON module from the response.

### 4.
```
sns.barplot(weather['humidity'], weather['temperature'])
```
Here humidity will be in x axis and temperature in y axis, all data will be shown in x, y axis and we can see from first line that ***sns*** comes from seaborn which we have already imported
```
import pandas as pd
import seaborn as sns
sns.set(color_codes=True)
```
And ***barplot*** is basically used to aggregate the categorical data according to some methods and by default it’s the mean

### 5.
```
sns.distplot(weather['humidity'])
```
***Seaborn's distplot*** lets you show a histogram with a line on it. This can be shown in all kinds of variations.

### 6.
```
sns.jointplot(weather['humidity'], weather['temperature'])
```
***Seaborn's jointplot*** displays a relationship between 2 variables (humidity and temperature) as well as 1D profiles (univariate) in the margins.

### 7.
```
sns.distplot(weather['humidity'], kde=False, rug=True)
```
Here ***kde** described as Kernel Density Estimate is used for visualizing the Probability Density of a continuous variable.
And ***rug*** is a plot of data for a single quantitative variable, displayed as marks along an axis. It is used to visualise the distribution of the data.

### 8.
```
sns.pairplot(weather[['humidity', 'temperature', 'air_pollution_index']])
```
***sns.pairplot*** means Plot pairwise relationships in a dataset. By default, this function will create a grid of Axes such that each numeric variable in data will by shared across the y-axes across a single row and the x-axes across a single column. This result we can see in our output.

### 9.
```
sns.stripplot(weather['weather_type'], weather['temperature'])
```
A ***stripplot*** is drawn on its own. It is a good complement to a boxplot or violinplot in cases where all observations are shown along with some representation of the underlying distribution. It is used to draw a scatter plot based on the category.

### 10.
```
sns.stripplot(weather['weather_type'], weather['temperature'], jitter = True)
```
Here we can see the use of ***jitter*** that is a great technique in dot plots, box plots with dots, and scatter plots. Jitter is a random value (or for our purposes pseudo-random) that is assigned to the dots to separate them so that they aren't plotted directly on top of each other.

### 11.
```
sns.countplot(weather['weather_type'])
```
***countplot*** shows the occurrences of the days of the week that are represented in the days column of the tips data set.
