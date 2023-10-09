# Vacation-vs-School

## Introduction
---
As a university student, the transition between the _Vacation_ time and the _School_ brings about major changes in how I spend my time. With an increased workload and new goals to achieve, the time I spend on various activities changes.
On a personal level, I am interested in understanding how my days have actually changed from before and after school, quantifying how much productive activities have increased, whether procrastination has decreased, and whether the change of period affects other factors such as sleep or time spent eating.


## Data
---
I personally collected the data in the past month. Each record is composed of the following variables:
- Date
- Starting Time
- Title of the Action
- Category, between
	1. Productivity
	2. Passive (procrastination)
	3. Food
	4. Sleeping
	5. Travelling
	6. Other

I used two different methods to collect the data.
In the first few days, I simply collected the data in the Google Keep app. Then, I transferred the data to Google Sheets, from where I created a simple Appsheet application based on that same spreadsheet.


## Analyzing the Data
---
### On Google Sheets
A calculated variable that will simplify the analysis is the `Duration` of each individual action. To calculate it, I first extracted a column called `Minutes`
```excel
=HOUR(SUBSTITUTE(C2,":","."))*60+MINUTE(SUBSTITUTE(C2,":","."))+1440*(DAY(B2)-16)
```
where:
- column B: Date
- column C: Hour
Then, the `Duration` column is created by subtracting the current `Minutes` value from the next one.
```excel
=F3-F2
```
where F is the column `Minutes`.

### On Google Colab


## Results
---

## Conclusions
---