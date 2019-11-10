# Berlin dashboard
## 1. Description
Today, [3.6 billion people](https://www.mckinsey.com/featured-insights/urbanization/how-to-make-a-city-great)  are living in cities. By 2030, that number is expected to reach 5 billion. That means that by 2030, 60 percent of the world’s population will live in cities.

Considering this forecast and the increasing constitution of Megacities, air quality as become one of the most important indicators of lifequality.

For this reason I have collected pollution data from the Berlin city, with the aim of analyzing the correlation among different pollutants, and building a "city-dashboard" that could potentially be used for monitoring the evolution of the pollutants in the different districts of Berlin.

Data collected: historical pollution data from 01-01-2017 to 06-11-2019 for the following pollutants: CO(mg/m3), NO_2(µg/m3), NOx(µg/m3), O_3(µg/m3), PM10(µg/m3), SO_2(µg/m3). Max granularity is hourly.

## 2. Files
- 1_berlin_pollution_stations.ipynb: notebook that automatically downloads, opens and cleans data about berlin's pollution from guvernamental website (https://luftdaten.berlin.de/lqi). It also loads information about the location of the stations. Converts both dataframes as pickles.
- 2_coordinates_to_lat_lon.ipynb: notebook that coverts the latitude and longitud from degrees, minutes, and seconds to decimal format. Converts the dataframe as pickle.
- 3_merge_poll_and_stations.ipynb: notebook that reads the pickle files and merge the stations dataframe and the pollution dataframe. Exports the merged dataframe as pickle.
- 4_subsetting.ipynb: notebook that from the merged dataframe, subsets to obtain different granularity dataframes: hourly, daily and monthly. Export the three dataframes as csv so it can be imported in Tableau for data visualization.

## 3. Tableau
Once all the data has been prepared in python, it is imported in Tableau. Tableau has been used to create monthly and daily dashboards that allow seamlesslyexplore the different districts and pollutants. 

Recomendation: analyze the Tableau dashboards in full-screen. 

To be found here: https://public.tableau.com/profile/atomohe#!/vizhome/Berlin_Dashboard/BerlinPollution?publish=yes

## 4. Environment dependancies:
- appnope==0.1.0
- asn1crypto==1.2.0
- attrs==19.2.0
- backcall==0.1.0
- beautifulsoup4==4.8.1
- bleach==3.1.0
- certifi==2019.9.11
- cffi==1.13.0
- chardet==3.0.4
- colorama==0.4.1
- cryptography==2.8
- cycler==0.10.0
- decorator==4.4.0
- defusedxml==0.6.0
- entrypoints==0.3
- geographiclib==1.50
- geopy==1.20.0
- idna==2.8
- ipykernel==5.1.2
- ipython==7.8.0
- ipython-genutils==0.2.0
- jedi==0.15.1
- Jinja2==2.10.3
- joblib==0.13.2
- jsonschema==3.0.2
- jupyter-client==5.3.3
- jupyter-core==4.5.0
- kiwisolver==1.1.0
- langdetect==1.0.7
- LatLon==1.0.2
- MarkupSafe==1.1.1
- matplotlib==3.1.1
- mistune==0.8.4
- mkl-fft==1.0.14
- mkl-random==1.1.0
- mkl-service==2.3.0
- nbconvert==5.6.0
- nbformat==4.4.0
- notebook==6.0.1
- numpy==1.17.2
- pandas==0.25.1
- pandocfilters==1.4.2
- parso==0.5.1
- patsy==0.5.1
- pexpect==4.7.0
- pickleshare==0.7.5
- prometheus-client==0.7.1
- prompt-toolkit==2.0.10
- ptyprocess==0.6.0
- pycountry==19.8.18
- pycparser==2.19
- Pygments==2.4.2
- PyMySQL==0.9.3
- pyOpenSSL==19.0.0
- pyparsing==2.4.2
- pyproj==2.4.1
- pyrsistent==0.15.4
- PySocks==1.7.1
- python-dateutil==2.8.0
- pytz==2019.3
- pyzmq==18.1.0
- requests==2.22.0
- scikit-learn==0.21.3
- scipy==1.3.1
- seaborn==0.9.0
- Send2Trash==1.5.0
- six==1.12.0
- soupsieve==1.9.3
- SQLAlchemy==1.3.10
- statsmodels==0.10.1
- terminado==0.8.2
- testpath==0.4.2
- tornado==6.0.3
- traitlets==4.3.3
- urllib3==1.24.2
- wcwidth==0.1.7
- webencodings==0.5.1
- xlrd==1.2.0



