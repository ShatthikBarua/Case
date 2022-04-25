
# Case

Bike sharing systems are a type of bicycle rental service where the process of obtaining a membership, renting a bike, and returning the bike is all automated through a network of pick up points around a city. People can rent a bike from one spot and return it to a different location as needed. In Oslo, Oslo City Bikes can be found at 250 stations in and around the city centre. If a rack is full or empty, the next one is always close by.

Apart from the real-world applications of bike-sharing systems, the features of the data created by these systems make them appealing for research. In contrast to other modes of transportation such as bus or subway, travel time, as well as the departure and arrival positions, are all recorded explicitly in these systems. This feature transforms the bike-sharing system into a virtual sensor network that can be used to monitor city movement.

In this case, you are asked to combine historical usage patterns with weather data in order to extract some useful insights. You are free to choose what you want to investigate and what the end result of the case is, it can be a model, a dashbord, report or something else.
Some interesting topcis could be:

- How does weather impact bike trips?
- How do bike trip patterns vary by time of day and the day of the week?

As stated, you are free to decide what you want to do.
The important thing is that you demonstrate how you work with new data, and how you produce insight. This is not supposed to be a very time consuming case, please do not use more than 3 hours.

You are free to choose what tools to use, but in the data wrangling part python is prefered. 

## Data


Bike_YYYY_MM.csv: Trips with a duration of at least one minute, made during Oslo City Bike regular opening times in year(YYYY) and month(MM).


| Variable                  | Format                   | Description                                   |   |   |
|---------------------------|--------------------------|-----------------------------------------------|---|---|
| started_at                | Timestamp                | Timestamp of when the trip started            |   |   |
| ended_at                  | Timestamp                | Timestamp of when the trip ended              |   |   |
| duration                  | Integer                  | Duration of trip in seconds                   |   |   |
| start_station_id          | String                   | Unique ID for start station                   |   |   |
| start_station_name        | String                   | Name of start station                         |   |   |
| start_station_description | String                   | Description of where start station is located |   |   |
| start_station_latitude    | Decimal degrees in WGS84 | Latitude of start station                     |   |   |
| start_station_longitude   | Decimal degrees in WGS84 | Longitude of start station                    |   |   |
| end_station_id            | String                   | Unique ID for end station                     |   |   |
| end_station_name          | String                   | Name of end station                           |   |   |
| end_station_description   | String                   | Description of where end station is located   |   |   |
| end_station_latitude      | Decimal degrees in WGS84 | Latitude of end station                       |   |   |
| end_station_longitude     | Decimal degrees in WGS84 | Longitude of end station                      |   |   |


Weather_YYYY_MM.csv: Daily temprature,rain,snow and wind data for year YYYY and month MM


| Variable                | Format  | Description                          |
|-------------------------|---------|--------------------------------------|
| Dato                    | Integer | Day of month                         |
| Min. temp.              | String  | Minimum temperature of day           |
| Maks temp.              | String  | Maximum temperature of day           |
| Gjennomsnitt            | String  | Avarage temperature of day           |
| Normal temp.            | String  | Normal historical temperature of day |
| Nedbør mm (måles kl 07) | String  | Rain in mm as of 07                  |
| Snødybde cm             | String  | Snow in cm                           |
| Vind m/s                | String  | Wind in m/s                          |
| Kraftigste vind m/s     | String  | Strongest wind of day in m/s         |


The data is ziped in the folders Weather.7z and Bike.7z, they can either be unziped using 7-zip
or the following python code

```python
import py7zr

with py7zr.SevenZipFile('ziped file location', mode='r') as z:
    z.extractall('your data folder')
```



# Acknowledgements
Data is taken from https://oslobysykkel.no/ and https://www.yr.no/
the data is published under the Norwegian Licence for Open Government Data (NLOD) 2.0