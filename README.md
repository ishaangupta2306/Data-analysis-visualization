## Data Ingestion and Exploratory Data Analysis using Yelp API and IoT data


### 1. Exploratory data analysis for traffic violations in Rhode Island
- Cleaning messy data (included fixing incorrect data types
- Combined and reshaped datasets 
- Manipulated time series data.
- Analysis 
  - Compare violations by gender
  - Compare speeding outcomes by gender
  - Compare the rate of annual drug-related stops for each year
  
  ##### About Dataset
  The Stanford Open Policing Project is collecting and standardizing data on vehicle and pedestrian stops from law enforcement departments across the country. They've  collected data from 31 US states. Datasets used
  - police.csv  
  - weather.csv

### 2. Streamlined Ingestion using Yelp API

Used Yelp Business Search API to fetch information about all businesses in the state of Ohio. https://docs.developer.yelp.com/reference/v3_business_search
To authenticate API calls with the API Key, set the Authorization HTTP header value as Bearer API_KEY.

```bash
api_url = https://api.yelp.com/v3/businesses/search 
api_key = <create an app to obtain your private API key>
```

Extract the JSON data from the response and loaded the business listings to the dataframe businesses with pandas DataFrame() function. The listings are under the "businesses" key in data.

### 3. Analyzing IoT data
- Combined environmental data with the traffic datasets
- Calculated the correlation between the different columns
- Created a heatmap from the correlation and analyzed the heatmap with key observations
- Investigated the data further using a pairplot, showing the distribution between the different data columns and noted key conclusions


   ##### About Dataset
    - traffic_heavy_vehicles.json  - represents the number of heavy vehicles per hour on a road of a city.
    - traffic_light_vehicles.json  - represents the number of light vehicles per hour on a road of a city.
    - environment.json - consists of temperature in degree celsius, humidity in percent, sunshine duration in seconds

