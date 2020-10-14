<div align="center"><img width="100%" src="https://github.com/sfu-db/dataprep/raw/develop/assets/logo.png"/></div>

-----------------
<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/pypi/l/dataprep?style=flat-square"/></a>
  <a href="https://sfu-db.github.io/dataprep/"><img src="https://img.shields.io/badge/dynamic/json?color=blue&label=docs&prefix=v&query=%24.info.version&url=https%3A%2F%2Fpypi.org%2Fpypi%2Fdataprep%2Fjson&style=flat-square"/></a>
  <a href="https://pypi.org/project/dataprep/"><img src="https://img.shields.io/pypi/pyversions/dataprep?style=flat-square"/></a>
  <a href="https://www.codacy.com/gh/sfu-db/dataprep?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=sfu-db/dataprep&amp;utm_campaign=Badge_Coverage"><img src="https://app.codacy.com/project/badge/Coverage/ed658f08dcce4f088c850253475540ba"/></a>
<!--   <a href="https://codecov.io/gh/sfu-db/dataprep"><img src="https://img.shields.io/codecov/c/github/sfu-db/dataprep?style=flat-square"/></a> -->
  <a href="https://www.codacy.com/gh/sfu-db/dataprep?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=sfu-db/dataprep&amp;utm_campaign=Badge_Grade"><img src="https://app.codacy.com/project/badge/Grade/ed658f08dcce4f088c850253475540ba"/></a>
  <a href="https://discord.gg/xwbkFNk"><img src="https://img.shields.io/discord/702765817154109472?style=flat-square"/></a>
</p>


<p align="center">
  <a href="https://sfu-db.github.io/dataprep/">Documentation</a>
  |
  <a href="https://discord.gg/xwbkFNk">Forum</a>
  | 
  <a href="https://groups.google.com/forum/#!forum/dataprep">Mail List</a>
</p>

Dataprep lets you prepare your data using a single library with a few lines of code.

Currently, you can use `dataprep` to:
* Collect data from common data sources (through `dataprep.connector`)
* Do your exploratory data analysis (through `dataprep.eda`)
* ...more modules are coming

## Releases

<div align="center">
  <table>
    <tr>
      <th>Repo</th>
      <th>Version</th>
      <th>Downloads</th>
    </tr>
    <tr>
      <td>PyPI</td>
      <td><a href="https://pypi.org/project/dataprep/"><img src="https://img.shields.io/pypi/v/dataprep?style=flat-square"/></a></td>
      <td><a href="https://pepy.tech/project/dataprep"><img src="https://pepy.tech/badge/dataprep"/></a></td>
    </tr>
    <tr> 
      <td>conda-forge</td>
      <td><a href="https://anaconda.org/conda-forge/dataprep"><img src="https://img.shields.io/conda/vn/conda-forge/dataprep.svg"/></a></td>
      <td><a href="https://anaconda.org/conda-forge/dataprep"><img src="https://img.shields.io/conda/dn/conda-forge/dataprep.svg"/></a></td>
    </tr>
  </table>
</div>


## Installation

```bash
pip install -U dataprep
```

## Examples & Usages

The following examples can give you an impression of what dataprep can do:

* [Documentation: Connector](https://sfu-db.github.io/dataprep/user_guide/connector/connector.html)
* [Documentation: EDA](https://sfu-db.github.io/dataprep/user_guide/eda/introduction.html)
* [EDA Case Study: Titanic](https://sfu-db.github.io/dataprep/user_guide/eda/titanic.html)
* [EDA Case Study: House Price](https://sfu-db.github.io/dataprep/user_guide/eda/house_price.html)

### EDA

There are common tasks during the exploratory data analysis stage, 
like a quick look at the columnar distribution, or understanding the correlations
between columns. 

The EDA module categorizes these EDA tasks into functions helping you finish EDA
tasks with a single function call.

* Want to understand the distributions for each DataFrame column? Use `plot`.

<a href="https://sfu-db.github.io/dataprep/user_guide/eda/plot.html#Get-an-overview-of-the-dataset-with-plot(df)"><img src="https://github.com/sfu-db/dataprep/raw/develop/assets/plot(df).gif"/></a>

* Want to understand the correlation between columns? Use `plot_correlation`.

<a href="https://sfu-db.github.io/dataprep/user_guide/eda/plot_correlation.html#Get-an-overview-of-the-correlations-with-plot_correlation(df)"><img src="https://github.com/sfu-db/dataprep/raw/develop/assets/plot_correlation(df).gif"/></a>

* Or, if you want to understand the impact of the missing values for each column, use `plot_missing`.

<a href="https://sfu-db.github.io/dataprep/user_guide/eda/plot_missing.html#Get-an-overview-of-the-missing-values-with-plot_missing(df)"><img src="https://github.com/sfu-db/dataprep/raw/develop/assets/plot_missing(df).gif"/></a>

You can drill down to get more information by given `plot`, `plot_correlation` and `plot_missing` a column name.: E.g. for `plot_missing`

<a href="https://sfu-db.github.io/dataprep/user_guide/eda/plot_missing.html#Understand-the-impact-of-the-missing-values-in-column-x-with-plot_missing(df,-x)"><img src="https://github.com/sfu-db/dataprep/raw/develop/assets/plot_missing(df, x).gif"/></a>

&nbsp;&nbsp;&nbsp;&nbsp;for numerical column using`plot`:

<a href="https://sfu-db.github.io/dataprep/user_guide/eda/plot.html#Understand-a-column-with-plot(df,-x)"><img src="https://github.com/sfu-db/dataprep/raw/develop/assets/plot(df,x)_num.gif"/></a>

&nbsp;&nbsp;&nbsp;&nbsp;for categorical column using`plot`:

<a href="https://sfu-db.github.io/dataprep/user_guide/eda/plot.html#Understand-a-column-with-plot(df,-x)"><img src="https://github.com/sfu-db/dataprep/raw/develop/assets/plot(df,x)_cat.gif"/></a>

Don't forget to checkout the [examples] folder for detailed demonstration!

### Connector

Connector provides a simple programming interface to collect structured data from different Web APIs (e.g., Twitter API, Yelp Fusion API, Spotify API, DBLP API), making web data collection easy and efficient, without requiring advanced programming skills.


Do you want to leverage the growing number of websites that are opening their data through public APIs?.


Connector is for you!  

Let's check out the several benefits that Connector offers:

* **A unified API:** you can fetch data using one or two lines of code to get data from many websites.

<img src="https://github.com/sfu-db/dataprep/raw/develop/assets/connector_main.gif"/></a>

* **Auto Pagination:** it automatically does the pagination for you so that you can specify the desired count of the returned results without even considering the count-per-request restriction from the API.

<img src="https://github.com/sfu-db/dataprep/raw/develop/assets/connector_pagination.gif"/></a>

* **Smart API request strategy:** it can issue API requests in parallel while respecting the rate limit policy.

<img src="https://github.com/sfu-db/dataprep/raw/develop/assets/connector_concurrency.gif"/></a>


Through <strong><em>configuration files</em></strong>, Connector specifies how to connect with each Web API for data gathering. If you want to connect with any of the APIs mentioned in the table below, with one line of code, you can get the most up-to-date version of the config file from our codebase and use it right away! 
 
Web API |  Auth Method  | Connector Config File(s) | Description |
|---|---|---|---|
| [Twitter](https://developer.twitter.com/en)  | `OAuth2` |  [Twitter config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/twitter) |  API endpoint for Tweets information retrieval. |
| [Spotify](https://developer.spotify.com/)  | `OAuth2` |  [Spotify config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/spotify) |  Comprehensive API for retrieving albums, artists, and tracks metadata. |
| [Yelp](https://www.yelp.com/developers)  | `Bearer Token` |  [Yelp config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/yelp) |  Leading API to access restaurant information by location.  |
| [DBLP](https://dblp.org/faq/13501473.html) | No |  [DBLP config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/dblp) |   Open bibliographic API for computer science publications.  |
| [Youtube](https://developers.google.com/youtube)  | `API Key` |  [Youtube config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/youtube) |  API for retrieving Youtube's content information.  |
| [Finnhub](https://finnhub.io/)  | `API Key` |  [Finnhub config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/finnhub) |   Comprehensive API for financial, market, and economic data.  |
| [Musixmatch](https://developer.musixmatch.com/)  | `API Key` |  [Musixmatch config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/musixmatch) |  Leading API for searching music lyrics.  |
| [OpenWeatherMap](https://openweathermap.org/api)  | `API Key` |  [OpenWeatherMap config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/openweathermap) |  API for retrieving current and historical weather data. |
| [Spoonacular](https://spoonacular.com/food-api)  | `API Key` |  [Spoonacular config file(s)](https://github.com/sfu-db/DataConnectorConfigs/tree/develop/spoonacular) |  Recipe, food, and nutritional information API.  |

If you want to connect with a different web API, Connector is designed to be easy to extend. You can write a simple config file describing the API's main attributes like the URL, query parameters, authentication and authorization method, pagination, etc.  

In the following link, you can see detailed examples of how to use Connector for retrieving data from DBLP, Spotify, Yelp, and other sites, without taking an in-depth look into these websites documentation!: [Examples.](https://github.com/sfu-db/dataprep/tree/develop/examples)

## Contribute

There are many ways to contribute to Dataprep.

* Submit bugs and help us verify fixes as they are checked in.
* Review the source code changes.
* Engage with other Dataprep users and developers on StackOverflow.
* Help each other in the [Dataprep Community Discord](https://discord.gg/xwbkFNk) and [Mail list & Forum].
* [![Twitter]](https://twitter.com/sfu_db)
* Contribute bug fixes.
* Providing use cases and writing down your user experience.

Please take a look at our [wiki] for development documentations!


[Build Status]: https://img.shields.io/circleci/build/github/sfu-db/dataprep/master?style=flat-square&token=f68e38757f5c98771f46d1c7e700f285a0b9784d
[Mail list & Forum]: https://groups.google.com/forum/#!forum/dataprep
[wiki]: https://github.com/sfu-db/dataprep/wiki
[examples]: https://github.com/sfu-db/dataprep/tree/master/examples
[Twitter]: https://img.shields.io/twitter/follow/sfu_db?style=social

## Acknowledgement

  Some functionalities of DataPrep are inspired by the following packages.
  
- [Pandas Profiling](https://github.com/pandas-profiling/pandas-profiling)

  Inspired the report functionality and insights provided in DataPrep.eda.

- [missingno](https://github.com/ResidentMario/missingno) 

  Inspired the missing value analysis in DataPrep.eda.
