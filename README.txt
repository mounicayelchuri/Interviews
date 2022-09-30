Task:
Provide a script to collect Google Trends weekly, daily and hourly data with the keyword ‘bitcoin’ since 2015-01-01 and save results in csv or json file

Language of implementation : Python

Files included :
3 csv files(hourly data, daily data & weekly data).
1 jupyter notebook
1 Readme file

Approach :
1.Use pytrends api to get the data.
    pytrends.get_historical_interest(kw_list, year_start=year, month_start=1, day_start=1, hour_start=0, year_end=year, month_end=12, day_end=31, hour_end=0, cat=0, sleep=0)
2.Extract the data from January,2015 to a dataframe.
3.Create new attributes like year, month, day,hour, week from date.
4.Group data based on year, month, day and get the sum of counts to get daily data.
5.Group data based on year, month, day, week and get the sum of counts to get weekly data.


Time taken :
Initially it took time to understand the api and get some data out of it.

Issues faced:
Even though approach looks fine but I was not able to get complete data.
I got only 15k rows which ideally has to be around 60k.
As I was getting less number of rows, I tried adjusting sleep time to 5 secs to check if it may return more number of rows.
Reason for getting less data is I have crossed the rate limit (allowed number of requests).So, I couldn't proceed further to fix the issue.
Tried with approach suggested in https://stackoverflow.com/questions/50571317/pytrends-the-request-failed-google-returned-a-response-with-code-429
but it didnot work for me. Receiving the same 429 error again.

way to run code:
Providing jupyter notebook . Run every cell to get the output.



