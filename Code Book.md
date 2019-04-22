The run_analysis.R file is a script that downloads the data from a website, extracts certain information from the data, and cleans it.

The following are the steps followed in the code (with each block of code counted as one step):
1) Download the UCI HAR Dataset via download.file() and unzip it using unzip(). Then, extract information from the dataset with the read.table() function and store these in different variables.

  File Downloaded:
  data.zip
  
  Data Stored:
  features  <-  class: data frame, 561 obs. of 2 variables
  sub.test  <-  class: data frame, 2947 obs. of 1 variable
  sub.train  <-  class: data frame, 7352 obs. of 1 variable
  x.test  <-  class: data frame, 2947 obs. of 561 variables
  x.train  <-  class: data frame, 7352 obs. of 561 variables
  y.test  <-  class: data frame, 2947 obs. of 1 variable
  y.train  <-  class: data frame, 7352 obs. of 1 variable
  
2) The dataframes are then merged using the functions rbind() and cbind() to create one dataset.

  Data Stored:
  x <-  merged x.test and x.train
  y <-  merged of y.test and y.train
  subject <-  merged sub.test and sub.train
  finaldata <-  merged x, y, and subject
  
3) Extract variables containing the mean and standard deviation of the measurements. The extracted dataset is then "tidied".

  Data Stored:
  df  <-  a subset of finaldata with fixed variable names
  
4) Creates an independent data set from the dataframe in step 3 and saves the file.

  Data Stored:
  df2 <-  contains the mean of each variable in df
  
  Files Created:
  Output.txt  <-  saves the df2 dataset into a textfile
