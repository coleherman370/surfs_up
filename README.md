# Surfs Up

# Overview
This analysis was performed at the Request to assess the temperature variation at a weather station in Oahu, HI. The goal is to compare the weather for the months of June and December.

# Results
- Between June and December there is only a 3° average temperature difference
- Despite the average being close, there is a wider swing in minimum temperature
  - June has a min temp of 64° while December has a min temp of 71°
- Max temperature for the two months vary by only 2°
  - June has a max temp of 85° while December has a max temp of 82°

June Temperatures            |  December Temperatures
:-------------------------:|:-------------------------:
![](https://github.com/coleherman370/surfs_up/blob/main/Resources/june_temps.png)  |  ![](https://github.com/coleherman370/surfs_up/blob/main/Resources/dec_temps.png)

# Summary
In regards to temperature, it can be seen that there is not much variation between the high and low months. This would be due to the Oahu, HI being located relatively close to the equator. Another analysis that may be insightful would be percipitation levels. This can be done for June and December in the following manner
- june_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month',Measurement.date) == 6).all()
- dec_prcp = session.query(Measurement.date, Measurement.prcp).filter(extract('month',Measurement.date) == 12).all()