# Walkthrough of a Data Visualization Project: World's Airports and Airlines Dataset ✈️


This will be my first project in data analysis and visualization. I love traveling and airports, so I chose a dataset that contains some information about the world's airports and airlines.

## Data Exploration 

I got the dataset from kaggle: https://www.kaggle.com/datasets/arbazmohammad/world-airports-and-airlines-datasets/data?select=Final_airlines there are three files in the dataset, but I choose only the Final_airlines dataset to perform my analysis on it. 
This dataset contains 8 fields: [ Airline ID, Name of the airline, Alias of the airline, IATA( 2-letter IATA code), ICAO (3-letter ICAO code), Airline callsign, Country or territory where the airline is incorporated, Active OR Inactive Airline ]. 

<img width="570" alt="Screenshot 2023-12-19 at 12 33 25 AM" src="https://github.com/mannaaaz/data-science-projects/assets/85847371/b752603c-8cf1-40ba-90b9-55c3141b980e">


## Quick Statistics 

After importing the required libraries, and reading the dataset into your notebook, you want to explore some basic statistics about the dataset right? So, let's start. I can explore many things here, such as: top value in each column, frequency of it, count of non-null and unique values in each column, and much more. Moreover, this step helps you gain a better understanding of the characteristics and structure of your data.
For example, from the picture below, you now know that National Airlines is the top name in your dataset and it appeared 5 times in the "Name" column. Also, look at the top country, you see the USA, this means that the dataset contains a significant number of airlines or airports from the USA. 

<img width="603" alt="Screenshot 2023-12-19 at 12 34 25 AM" src="https://github.com/mannaaaz/data-science-projects/assets/85847371/9082b524-b96b-45f7-9923-981eaa0e96ca">


## Cleaning the Data

In every dataset you will encounter missing values that you need to clean in a way you think is better. The first step you do is to check how many missing values are in each column by using the .null() method. 

<img width="576" alt="Screenshot 2023-12-19 at 12 34 57 AM" src="https://github.com/mannaaaz/data-science-projects/assets/85847371/95ff9d9b-b806-4527-8014-891f235cdfdc">

All of the columns have missing values except the name and active columns. Now it is time to clean the columns from missing and NaN values.
When you want to choose which method to use while cleaning your data (drop rows or columns, fill with zeros or other values, or use imputation methods) this depends on many many factors. You need to take into consideration the data types, characteristics, your visualization goals, and your audience. 
Since my main goal from this dataset is to explore airline distribution by country, I need to primarily focus on the country and name columns. So I think for the other columns: Alias, IATA, ICAO, and Callsign, I can simply fill the missing values with zeros because they will not affect my visualization. 

<img width="588" alt="Screenshot 2023-12-19 at 12 35 28 AM" src="https://github.com/mannaaaz/data-science-projects/assets/85847371/3a30c12e-a505-4077-aec3-35b42de96071">

For now I will only focus on this main goal but I might later add more visualizations and revisit this step to change my method of cleaning the data.

## Visualizing the Data

Now, I would like to implement a world map for each airline's origin country. But for some reason the column ‘Country’ is not well cleaned so I need to clean this column specifically because the map depends heavily on it. 
I will first check if the country column still has missing values. If not I will proceed to manually map some unconventional values to their correct country names and drop non-country rows. 

Then .. I implement the world map using GeoDataFrame. 

<img width="1147" alt="Screenshot 2023-12-19 at 1 47 30 AM" src="https://github.com/mannaaaz/data-science-projects/assets/85847371/4e0b2e10-d18d-4fef-9e32-d809b18c806d">



## Conclusion

In conclusion, this analysis has provided valuable insights into the global distribution of airlines. 

Some of the key observations: 

1- The concentration of airlines in certain countries, such as the United States and Mexico, suggests the presence of major players in the aviation industry. 

2- The map clearly illustrates regional disparities in the distribution of airlines. North America comes at the top, then Asia (specifically Russia), then Europe, and at the end comes Australia, South America, and Africa.  


This could help us raise some important questions .. 

What are the factors that caused the map to look like this? Technological Factors? Economic Factors? Is there a possibility that the current distribution could change quickly? 

And many more questions could be asked .. 

Zain


