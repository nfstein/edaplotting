# edaplotting

In the words of John Turkey :
> Exploratory data analysis can never be the whole story, but nothing else can serve as the foundation stone.

### Dependencies

pandas (required) : https://pandas.pydata.org  
numpy (required): http://numpy.scipy.org  
matplotlib (required): http://matplotlib.sourceforge.net  
seaborn (required): https://seaborn.pydata.org  

### Key features

* Plot command that supports 4-in-1 with no requirment to import any plotting libraries :sunglasses:
* Supports univariate and bivariate exploratory analysis on numerical variables
* Takes only a 100 random data points for plotting(only available for univariate)
* Includes the ECDF plot : https://en.wikipedia.org/wiki/Empirical_distribution_function
* Red diamonds on the ECDF plot indicate the following percentiles : 2.5,25,50(median),75,97.5

## looks cool!! But how do i use this library? :confused:

### Installation

```
pip install edaplotting
```

### Usage for univariate EDA

```python
import edaplotting as eda # import the edaplotting library and assign the alias eda
import pandas as pd # import pandas
data = pd.read_csv('Pokemon.csv') # read in a dataset of interest 
myobject = eda.explore(dataframe['Speed'],dataframe['Attack']) # initialize the class with a one-dimensional array
# x and y are passed as kwargs, for univariate only x is considered
myobject.plot() # plot the object
```

![png](image_univariate.png)

### Usage for bivariate EDA

```python
import edaplotting as eda # import the edaplotting library and assign the alias eda
import pandas as pd # import pandas
data = pd.read_csv('Pokemon.csv') # read in a dataset of interest 
myobject = eda.explore(dataframe['Speed'],dataframe['Attack']) # initialize the class with a two-dimensional array
# x and y are passed as kwargs, for bivariate both x and y are considered
myobject.plot() # plot the object
```

![png](image_bivariate.png)

### Todo

* Sample data for the bivariate array
* Expand for categorical variables

### License

MIT
