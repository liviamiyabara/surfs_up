# Surfs Up
Week 9, Module 9: Surf's Up with Advanced Data Storage and Retrieval

## Overview of the statistical analysis

In this week, the student wants to open a new business, Surf n’Shake Shack, a store that provides surf boards and ice cream to locals in Hawaii. After the business plan was created, there is an investor interested, W. Avy, but he is concerned about how the weather can affect the sales of the shop. He asks the student to run analytics on the weather data of Oahu island in order to secure additional investors to the enterprise.

In this challenge, W. Avy asked to perform specific analysis for the months of June and December to determine if the surf and ice cream shop business is sustainable year-round.
## Results

June statistics 

  ![ScreenShot](https://github.com/liviamiyabara/surfs_up/blob/main/Resources/june_stats.png)

June histogram

![ScreenShot]( https://github.com/liviamiyabara/surfs_up/blob/main/Resources/june_histogram.png)

December statistics

![ScreenShot]( https://github.com/liviamiyabara/surfs_up/blob/main/Resources/dec_stats.png)


December histogram 

![ScreenShot]( https://github.com/liviamiyabara/surfs_up/blob/main/Resources/dec_histogram.png)

* The average temperature for December is only 4 F degrees lower than in June, demonstrating that even during the winter, the temperatures in Oahu are still warm enough for surfing and ice cream

* Even during December, Oahu experience warm temperatures, with a maximum temperature of 83 F and third quartile of 74; for June, the maximum was 85 F and the third quartile 77

* The standard deviations are similar, 3.7 for December and 3.3 for June, so the group of numbers are similarly spread in both months 

* Although December has lower temperatures due to the winter season, the largest frequencies on the histogram are within 70 F to 75 F, still good temperatures for surfing and for ice cream consumption   

## Summary

In summary, based on the specific analysis of temperature for June and December, it seems that the surf and ice cream shop business is sustainable year-round, the temperature average temperature difference between summer and winter is only 4 F. 

An additional analysis to be performed is related to the precipitation. The temperatures are only one factor that is relevant to the shop, if there’s too much rain in the location, that can also impact sales. To perform the query, user can replace the ‘Measurement.tobs’ to ‘Measurement.prcp’. Below is the example for the June analysis:

> results_jun = session.query(Measurement.date, Measurement. prcp).\
filter(extract('month', Measurement.date)==6).all()

Another idea of query would be to use the ‘station’ table to gather information about the latitude, longitude and elevation. Some specific locations could be more favorable, warmer and with less rain. A query to compare the different GPS coordinates with precipitation and temperature could provide new insights on the best location. 
