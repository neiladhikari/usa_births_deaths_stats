# USA Birth and Death statistics.
This data is current as of: 2022-07-29.
The objective is to get national vital statistics data from the [CDC](https://www.cdc.gov/) website, specifically births and deaths by US states and territories.
Currently available data summary is for 2020 only, and that is what [this url](https://www.cdc.gov/nchs/fastats/state-and-territorial-data.htm) used in the jupyter notebook will pull. This is the most complete data, not most current.
This page will in its complete form will probably report the most complete numbers to date, so if you check in subsequent years, it should still work.
If you want, the most current vital statistics data can be requested from each state. The process for each state varies, and is a different topic for discussion for some other time.
In this case, the CDC data is tabular, so we will try to use pandas to directly read in the table, instead of going through beautifulsoup.

Formulas used in this analysis:

1) Fertility Rate = Number of births per 1000 women between 15-44 years of age.
2) Crude Birth Rate = Number of births per 1000 individuals of a population. i.e. (number of births * 1000)/ population.
3) Death Rate = Number of deaths per 100,000 individuals. i.e. (number of deaths * 100000)/ population.
4) Percent Births = (Total Births * 100) / population.
5) Percent Deaths = (Total Deaths * 100) / population.

Useful links:
1) https://wonder.cdc.gov/controller/datarequest/D76;jsessionid=9CC7C52E44642DAFCE5BCA2CBAC9
2) https://www.cdc.gov/publichealthgateway/healthdirectories/healthdepartments.html

Citation: Centers for Disease Control and Prevention, National Center for Health Statistics. National Vital Statistics System, Mortality 1999-2020 on CDC WONDER Online Database, released in 2021. Data are from the Multiple Cause of Death Files, 1999-2020, as compiled from data provided by the 57 vital statistics jurisdictions through the Vital Statistics Cooperative Program. Accessed at http://wonder.cdc.gov/ucd-icd10.html on Jul 29, 2022 8:19:19 PM
