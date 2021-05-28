# Covid-19-
<<<<<<< HEAD
# Covid-19-Preprocessed-Dataset
Latest Covid-19 Dataset

Coronavirus disease 2019 (COVID-19) time series listing confirmed cases, reported deaths and reported recoveries. Data is disaggregated by country (and sometimes subregion). Coronavirus disease (COVID-19) is caused by the [Severe acute respiratory syndrome Coronavirus 2 (SARS-CoV-2)][sars2] and has had a worldwide effect. On March 11 2020, the World Health Organization (WHO) declared it a pandemic, pointing to the over 118,000 cases of the coronavirus illness in over 110 countries and territories around the world at the time.

[covid]: https://en.wikipedia.org/wiki/Coronavirus_disease_2019
[sars2]: https://en.wikipedia.org/wiki/Severe_acute_respiratory_syndrome_coronavirus_2

This dataset includes time series data tracking the number of people affected by COVID-19 worldwide, including:

* confirmed tested cases of Coronavirus infection
* the number of people who have reportedly died while sick with Coronavirus
* the number of people who have reportedly recovered from it

# Sample Code

This is sample code by using you can get started working with this dataset.
!pip install plotly
import plotly.express as px
import plotly.graph_objects as go
import pandas as pd
df=pd.read_csv('covid19/preprocessed/covid_19_data_cleaned.csv', parse_dates=['Date'])
country_daywise=pd.read_csv('covid19/preprocessed/country_daywise.csv', parse_dates=['Date'])
countrywise=pd.read_csv('covid19/preprocessed/countrywise.csv')
daywise=pd.read_csv('covid19/preprocessed/daywise.csv', parse_dates=['Date'])
fig=go.Figure()
fig.add_trace(go.Scatter(x=Confirmed['Date'],y=Confirmed['Confirmed'],mode='lines+markers', name='Confirmed',line=dict(color='red')))
fig.add_trace(go.Scatter(x=Deaths['Date'],y=Deaths['Deaths'],mode='lines+markers', name='Deaths',line=dict(color='black')))
fig.add_trace(go.Scatter(x=Recovered['Date'],y=Recovered['Recovered'],mode='lines+markers', name='Recovered',line=dict(color='green')))
fig.add_trace(go.Scatter(x=Active['Date'],y=Active['Active'],mode='lines+markers', name='Active',line=dict(color='blue')))
fig.update_layout(title='Worldwide Covid-19 Cases',xaxis_tickfont_size=14,yaxis=dict(title='Number of cases'))fig=go.Figure()
fig.add_trace(go.Scatter(x=Confirmed['Date'],y=Confirmed['Confirmed'],mode='lines+markers', name='Confirmed',line=dict(color='red')))
fig.add_trace(go.Scatter(x=Deaths['Date'],y=Deaths['Deaths'],mode='lines+markers', name='Deaths',line=dict(color='black')))
fig.add_trace(go.Scatter(x=Recovered['Date'],y=Recovered['Recovered'],mode='lines+markers', name='Recovered',line=dict(color='green')))
fig.add_trace(go.Scatter(x=Active['Date'],y=Active['Active'],mode='lines+markers', name='Active',line=dict(color='blue')))
fig.update_layout(title='Worldwide Covid-19 Cases',xaxis_tickfont_size=14,yaxis=dict(title='Number of cases'))
