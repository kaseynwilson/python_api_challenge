#WeatherPy Analysis

###In order to analyze global weather trends, I took a random sample of more than 500 cities across the globe with varying distance from the equator to have a good sample size to analyze. 

###To do this I generated a random list of latitude and longitude points and then used citipy to locate a nearby city to that intersection. I then utilized the Open Weather Map API to gather weather and city information points, which include:
    *Temperature (F)
    *Humidity (%)
    *Cloudiness (%)
    *Wind Speed (mph)
    *Country
    *Date
    
###With these data points gathered, I compiled into a dataframe and exported to a .csv file. I checked for any data points showing greater than 100% humidity to eliminate if needed and identified outliers in order to exclude from the data analysis. With the remaining data points I completed a scatter plot and linear regression to showcase the following relationships:
    *Scatter Plot:
        *Temperature (F) vs. Latitude
        *Humidity (%) vs. Latitude
        *Cloudiness (%) vs. Latitude
        *Wind Speed (mph) vs. Latitude
    *Linear Regression:
        *Northern Hemisphere - Temperature (F) vs. Latitude
        *Southern Hemisphere - Temperature (F) vs. Latitude
        *Northern Hemisphere - Humidity (%) vs. Latitude
        *Southern Hemisphere - Humidity (%) vs. Latitude
        *Northern Hemisphere - Cloudiness (%) vs. Latitude
        *Southern Hemisphere - Cloudiness (%) vs. Latitude
        *Northern Hemisphere - Wind Speed (mph) vs. Latitude
        *Southern Hemisphere - Wind Speed (mph) vs. Latitude

###Findings based on the data:
    *This data demonstrates that as you get further away from the equator, the max temperature decreases. In the Southern Hemisphere (latitude below 0) the max temperature does not have as steep of a drop off as is seen in the Northern Hemisphere.
    *The city latitude vs. humidity plots for both Northern and Southern Hemispheres depicts no statistically significant correlation. With an r-value of close to 0 for each, humidity level seems to be independ of proximity to the equator. 
    *The city latitude vs. cloudiness plots for both Northern and Southern Hemispheres depicts no statistically significant correlation. With an r-value of close to 0 for each, cloudiness level seems to be independ of proximity to the equator. 
    *The city latitude vs. wind speed plots for both Northern and Southern Hemispheres depicts no statistically significant correlation. With an r-value of close to 0 for each, cloudiness level seems to be independ of proximity to the equator. 
    *Overall, temperature seems to be the only weather factor analyzed that is directly related to distance from the equator. Other weather patterns seem to be dictated by other factors in the environment. 
    
#VacationPy Analysis

###To determine the best vacation spots based on ideal weather trends, I utilized the csv export of city and weather data points collected from the WeatherPy Analysis. 

###I utilized gmaps to create a heatmap based on humidity and then narrowed down my vacation selections using the following criteria:
    *A max temperature lower than 80 degrees but higher than 75.
    *Wind speed less than 10 mph.
    *Zero cloudiness.    

###To ensure lodging is available in the desired locations, I used the Google Places API to identify the closest hotel within 5000 meters of the cities selected. I then plotted these on the existing heatmap so I could easily see the hotel details with an associated city on teh map. 
