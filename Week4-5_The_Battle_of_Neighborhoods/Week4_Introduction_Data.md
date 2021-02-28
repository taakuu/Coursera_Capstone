## Introduction: Business Problem <a name="introduction"></a>

### Backgroud

As COVID-19 has spread around the world for more than a year, vaccination is showing signs of convergence. However, there are still many unclear points about COVID-19 infection.

According to statistics, East Asians have a fairly low number of COVID-19 infections. It cannot be concluded that the cause has yet to be determined, whether it is due to genetic characteristics, many people already have immunity, or cultural differences.
It is strange that the number of infected people is smaller than in the West in the big city of Tokyo, which has a murderous crowded train commuter.

People infected with COVID-19 vary from region to region. It cannot be said that there are many infected people because of the large population. The risk of COVID-19 infection varies depending on what kind of city you live in or stay in.

_Note: For convenience, this document refers to the cities and wards of Tokyo as Borough._

### Problem

The problem is to answer the question of what kind of city is the one with many COVID-19 infections.

There are various factors that cause a city with many infected people, such as many overseas travelers, many foreigners, and many bars where clusters are likely to occur.
The purpose of this survey is to focus on the number of foreign residents and the number of bars to gain insight into the causal relationship with the number of people infected with COVID-19.

Sample use case:
- As a person planning to move to Tokyo, find out what kind of city has the same characteristics as a city with few infected people.
- As a visitor planning a trip to Tokyo, I would like to find a safe city with the same characteristics as a city with few infected people and enjoy eating and drinking.

It would be greatly appreciated if the causative factors could be clarified by solving this problem.

### Target Audience

- Those who want to move to or stay in Tokyo
- Those who want to know which city is relatively safe against infection

-------------------

## Data <a name="data"></a>

### Data Requirements

Based on definition of our problem, factors that will influence our decission are:
* the number of foreign residents in Tokyo
* the number of COVID-19 test positives in Tokyo
* the number of existing bars in the neighborhood (any type of bar)

### Data Collection

Following data sources will be needed to extract/generate the required information:

* The number of Foreign residents in Tokyo will be obtained from the following site:

  - Source: [_"2-4  FOREIGN RESIDENTS BY DISTRICT AND NATIONALITY ( 2019 )" in "TOKYO STATISTICAL YEARBOOK"_ ](https://www.toukei.metro.tokyo.lg.jp/tnenkan/2018/tn18q3i002.htmhttps://www.toukei.metro.tokyo.lg.jp/tnenkan/2018/tn18q3i002.htm)
    - by [_Statistics Division, Bureau of General Affairs, Tokyo Metropolitan Government_](https://www.toukei.metro.tokyo.lg.jp/homepage/ENGLISH.htm)
  - The data is as of 2019.
  - The data is aggregated by Borough, which means ward and city in Tokyo.
  
  > Foreign residents here mean foreign nationals who are registered according to the Basic Resident Registration Act.
    
* The number of COVID-19 test positive in Tokyo will be obtained from the following site:

  - Source: 
      - [_COVID-19 The information website by Tokyo Metropolitan Government_](https://stopcovid19.metro.tokyo.lg.jp/en)
      - [_Tokyo COVID-19 Task Force website (https://github.com/tokyo-metropolitan-gov)_](https://github.com/tokyo-metropolitan-gov/covid19/blob/development/docs/en/README.md)
  - The data is as of the day before yesterday.
  - The data is aggregated by Borough, which means ward and city in Tokyo.

* The list of Special wards and districts in Tokyo

  - Source:
      - [_Wikipedia: Special wards of Tokyo_](https://en.wikipedia.org/wiki/Special_wards_of_Tokyo)
      
* The number of bars and their type and location in every neighborhood will be obtained using **Foursquare API**

--------------------------------
