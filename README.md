# datafun-04-jupyter

## Create the project and clone to machine

#### I created a project repository on github and then cloned the repository to my machine.git 
'''shell
git clone url
'''

## Set up the environment
'''shell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install jupyterlab pandas matplotlib seaborn
py -m pip freeze > requirements.txt
'''
### I added .venv to the .gitignore file.
### Open the jupyter notebook

## Import dependencies
'''shell
import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
'''

### First - Load the data
'''shell
    # Load the Iris dataset into DataFrame
    df = sns.load_dataset('iris')

    # Inspect first rows of the DataFrame
    print(df.head())
'''

### Second - Inital Data Inspection
'''shell
    print(df.head(10))
    print(df.shape)
    print(df.dtypes)
'''

### Third - Initial Descriptive Statistics
'''shell
    print(df.describe())
'''

### Fourth - Initial Data Description by numerical columns
'''shell
    # Inspect histogram by numerical column
    df['petal_length'].hist()

    # Inspect histograms for all numerical columns
    df.hist()

    # Show all plots
    plt.show()
'''

### Fifth - Initial Data Description by categories
'''shell
    # Inspect histogram by numerical column
    df['species'].hist()

    # Inspect histograms for all numerical columns
    df.hist()

    # Show all plots
    plt.show()
'''
### Sixth - Data Transformation
'''shell
    #Adding new columns
    df['sepal_area'] = df['sepal_length'] * df['sepal_width']

    df['petal_area'] = df['petal_length'] * df['petal_width']

    # Inspect histograms for all numerical columns
    df.hist()

    # Show all plots
    plt.show()
'''

### Seventh - Data Visualization
'''shell
    sns.pairplot(df, hue="species")
    plt.show()
'''

### Conclusion