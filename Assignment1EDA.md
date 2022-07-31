def eda_script(data_path):
    import pandas as pd
    import numpy as np
    import matplotlib.pyplot as plt
    import seaborn as sns
    from scipy.stats import skew
    import os
    import time
    
    # load data and some basic info
    try:
        df = pd.read_csv(data_path)   
    except Exception :
        try : 
            df = pd.read_excel(data_path) 
        except Exception : 
            try :
                df = pd.read_json(data_path)
          
                    
    else :
        print('DataFrame : ')
        display(df.head())

        print('-----------------------------------------------------------------------------')
        print('data info : ')
        print(df.info())
        
         
        print('=============================================================================')
        nan_percentage_dict = dict()
        print('NaN percentage for every column  is : ')
        name = []
        percentage = []
        for i in df.columns:
            name.append(i)
            s = (str((df[i].isnull().sum()/df.shape[0]*100).round(2))+'%')
            percentage.append(s)
        nan_percentage_dict['name'] = name
              display(nan_percentage_df)
    
    #  This part of the code is used to seperate  categorical  and numerical columns of data 
    
    # FOR NAN OF TYPE FLOAT

import pandas as pd
value = float(nan)
type(value)
<class 'float'>
pd.isnull(value)
True
value = 'nan'
type(value)
 <class 'str'>
pd.isnull(value)
False


    numerical_col = []
    cat_col = []
    cols = df.columns
    for i in range(len(cols)):
        if df[cols[i]].dtype == np.int64 or df[cols[i]].dtype == np.int32  
        else :
            cat_col.append(cols[i])
    
    # Check not a number or (NAN) which is a numeric data type used to represent any value that is undefined or unpresentable
    numerical_col_nan = [] 
    cat_col_nan = []       
    for i in numerical_col:
        if(df[i].isnull().sum()>0 ):
            numerical_col_nan.append(i)
    for i in cat_col:
        if(df[i].isnull().sum() >0):
            cat_col_nan.append(i)
    
    
    
    # Fill in not a number
    
    
 
        
    # If variables are Numerical then  this is a check for their skewness   
    print('-------------------------------------------------------') 
    print('If variables are Numerical then  this is a check for their skewness   : ')
    name = []
    skew_value_list = []
    skew_type_list = list()
 
 load columns from data set 
 
 x= 
  n = len(x)
  mean_ = sum(x) / n
  var_ = sum((item - mean_)**2 for item in x) / (n - 1)
 std_ = var_ ** 0.5
 skew_ = (sum((item - mean_)**3 for item in x)
          * n / ((n - 1) * (n - 2) * std_**3))


 
    # This part of the code is concerned with counting  the No. of  values in the data 
    print('------------------------------------------------') 
    print('Count  the no. of values  in columns containing categorical Data : ')
    value_count_dict = dict()
    for i in cat_col:
        print(i,'column\'s count values : ' )
        index , count = df[i].value_counts().index , df[i].value_counts().values
        value_count_dict['value']  = list(index)
        value_count_dict['count'] = list(count)
      
       
    
     # Draw a Box Plot  for Data 
     
     
    
     # Draw a Box Plot  for Data  or "Box and Whisker" .  Median isn't swayed by outliers like median     

# A box and whisker plot is defined as a graphical method of displaying variation in a set of data. 
""" A  box and whisker plot can provide additional detail while allowing multiple sets of data to be displayed in the same graph.
Box and whisker plots can summarize data from multiple sources and display the results in a single graph. 
Box and whisker plots allow for comparison of data from different categories for easier, more effective decision-making.
In a box and whisker plot:
The left and right sides of the box are the lower and upper quartiles. The box covers the interquartile interval, where 50% of the data is found.
The vertical line that split the box in two is the median. Sometimes, the mean is also indicated by a dot or a cross on the box plot.
The whiskers are the two lines outside the box, that go from the minimum to the lower quartile (the start of the box) and then from the upper quartile (the end of the box) to the maximum.
The graph is usually presented with an axis that indicates the values  
The box and whisker plot can be presented horizontally  or vertically.
A variation of the box and whisker plot restricts the length of the whiskers to a maximum of 1.5 times the interquartile range. 
That is, the whisker reaches the value that is the furthest from the centre while still being inside a distance of 1.5 times the interquartile range from the lower or upper quartile. 
Data points that are outside this interval are represented as points on the graph and considered potential outliers."""
  
    cat_col_unique_less = []
    for i in cat_col :
        if len(df[i].unique())<=10:
            cat_col_unique_less.append(i)
    
    total = len(numerical_col) * len(cat_col_unique_less)
    index = 1
    if (total > 7 ):
       
    else : 
        plt.figure(figsize=(x,y)) 
        
    for i in range(len(cat_col_unique_less)):
        
        
            
    # Drawing of Various types of Graphs and Plots  
  
                

    
    
    #  Create a Heatmap
 
            
        
    
