Download Link: https://assignmentchef.com/product/solved-csci-1100-computer-science-1-homework-7-dictionaries
<br>
<h1>Problem Description</h1>

Write a program that reads in a year in the interval 1956 through 2015 inclusive (you may assume this input is correct) and finds the data for every month in this year to print out the following information:

Top 3 months and associated values for:

<ul>

 <li>highest maximum temperature (EMXT)</li>

 <li>lowest minimum temperature (EMNT)</li>

 <li>highest number of days with maximum temperature above 90 (DT90) <strong>– </strong>highest number of days with maximum temperature below 32 (DX32)</li>

 <li>highest total precipitation (TPCP)</li>

 <li>lowest total precipitation (TPCP)</li>

 <li>highest snow depth (TSNW)</li>

 <li>lowest snow depth (TSNW)</li>

</ul>

All values should be printed as floats with one decimal point {:.1f}.

If there are three or fewer valid values, then print that there is not enough data. (For example, snow depth in 1956.)

Ties should be broken using the month. For maximum values such as highest maximum temperature, the tie-breaking month will be sorted in descending order from 12 down to 1 and for minimum values such as lowest minimum temperature the tie-breaking month will be sorted in ascending order from 1 up to 12. Note that if you store your value/month pairs as a list of tuples or a list of lists, this is the default sort behavior and you will not have to do any additional work to get the sort order correct. See the example for snow depth in 2014 at the end of this write up for an example of the expected ordering.

Average of mean temperature across different months in the year (MNTM)

<ul>

 <li>Overall average (average of all months for the chosen year for MNTM)</li>

 <li>Average for the first 6 months of the year (MNTM)</li>

 <li>Average for the last 6 months of the year (MNTM)</li>

</ul>

If there are three or fewer valid data values for any one of these then print Not enough data.

A histogram of overall average temperatures in 3 month intervals, i.e. months 1-3, 4-6, 7-9, and 10-12. If there are fewer than two months in an interval, then print Not enough data. A histogram prints a single * for each value in the average, excluding partial values. For example, 54 *’s will be output for an average temperature of 54.7.

<h1>Expected output</h1>

Below you can see the expected functioning of this program with the file we gave you (note: we might change the file in the homework submission server): For the year 2014

Enter a year (1956-2015) =&gt; 2014

2014

Temperatures

———————————————————————-

Highest max value =&gt; 7: 92.0, 6: 91.0, 9: 90.0

Lowest min value =&gt; 1: -9.0, 2: -7.0, 3: 1.0

Highest days with max &gt;= 90 =&gt; 7: 3.0, 9: 2.0, 6: 1.0

Highest days with max &lt;= 32 =&gt; 2: 20.0, 1: 18.0, 3: 9.0

Precipitation

———————————————————————-

Highest total =&gt; 7: 5.8, 6: 5.6, 12: 5.0

Lowest total =&gt; 9: 0.9, 4: 1.9, 11: 2.1

Highest snow depth =&gt; 2: 24.6, 1: 12.6, 12: 5.8

Lowest snow depth =&gt; 5: 0.0, 6: 0.0, 7: 0.0

Average temperatures

———————————————————————-

Overall: 48.3

First 6 months: 40.9

Last 6 months: 55.7

Temperature histograms

———————————————————————-

01-03: ***********************

04-06: **********************************************************

07-09: *********************************************************************

10-12: ******************************************

For the year 1956

Enter a year (1956-2015) =&gt; 1956

1956

Temperatures

———————————————————————-

Highest max value =&gt; 8: 92.0, 9: 88.0, 10: 83.0

Lowest min value =&gt; 12: 5.0, 11: 15.0, 10: 27.0

Highest days with max &gt;= 90 =&gt; 8: 3.0, 12: 0.0, 11: 0.0

Highest days with max &lt;= 32 =&gt; 12: 4.0, 11: 2.0, 10: 0.0

Precipitation

———————————————————————-

Highest total =&gt; 9: 5.0, 11: 2.4, 12: 2.3

Lowest total =&gt; 8: 1.1, 10: 1.4, 12: 2.3

Highest snow depth =&gt; Not enough data

Lowest snow depth =&gt; Not enough data

Average temperatures

———————————————————————-

Overall: 42.3

First 6 months: Not enough data

Last 6 months: 42.3

Temperature histograms

———————————————————————-

01-03: Not enough data

04-06: Not enough data

07-09: ******************************************

10-12: *****************************************

<strong>Hints: </strong>(1) There are 70 ‘-‘s in every dashed line. (2) Investigate use of the rjust string method to print things like the 01 month string.

<h1>Suggestions</h1>

It appears that there are many things to compute, but it is actually the same thing for many different keys of the same list of dictionaries. The trick is to figure out what functions are needed and how they can be used over and over again to do closely related things by changing the function call parameters. You might write functions to do a number of things:

Gather values from data for a key and a year. (Note that data should be passed as a parameter.) Return these values in a list or a dictionary

Compute various statistics from these gathered values.

Compute and output average temperatures. Can this be called three times?

Compute and output a histogram. Can this be called four times?

Anything else? Some combination of the above?

If you are thoughtful and thorough in thinking through your use of functions you might find yourself only writing 100 lines of Python code or even fewer to solve this problem.