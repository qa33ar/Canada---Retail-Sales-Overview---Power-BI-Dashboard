## Canada---Retail-Sales-Overview---Power-BI--Dashboard
# Courteous request! Whenever anyone views or downloads any of my work, kindly spare a minute to give a few words so I can improve my work.#

Retail sales amounts of Canadian provinces and territories over 9 recent years are visualized in
Power BI Dashboard. 

## 📊 Project Overview

This project presents an interactive **Power BI business analysis
dashboard** for *Retail Sales of Canadian Provinces and Territories.

The purpose of the project is to demonstrate how a Power BI dashboard can answer business 
questions which reveal meaningful insights for stake holders and generally interested public.

Rather than focusing only on creating attractive visuals, the dashboard
was built around practical business questions as follows:
1. How have total retail sales trended monthly/yearly from 2017 to mid-2026, and is there
   a visible seasonal pattern?
2. How does e-commerce retail sales compare to total retail sales over time — is e-commerce's
   share growing?
3. Which provinces/regions have the highest and lowest retail sales, and how does that ranking
   hold up over time?
4. Are there specific periods (e.g., 2020) where sales patterns broke from the norm, and how
   visible is that in adjusted vs. unadjusted data?
5. What's the most recent month's performance compared to the same month a year prior (true YoY,
   not cycle-over-cycle this time — you have real monthly data now)?

   ------------------------------------------------------------------------

## 🛠️ Tools & Technologies

-   **Power BI**
-   **DAX**
-   **Power Query**
-   **Excel / CSV data**
-   Data modeling and relationships
-   Interactive slicers and dashboard visuals

------------------------------------------------------------------------

## 📁 Dataset
This dataset is sourced from Statistics Canada (StatCan). The original title of the dataset is 
Monthly retail trade sales by province and territory (x 1,000). 
StatCan allows public to download data in different forms and sizes. The dataset is obtained in its
entirety as CSV file and is explored using Transform data tab in Power BI Desktop. It spans over the
period of nine and a half years (January 2017 to June 2026). It consists of 79343 rows and 17 column
in its raw form. There are more regions included in this dataset than just the number of provinces 
and territories in Canada. The examples of such regions are Toronto, Ontario and Edmonton, Alberta 
and Montreal, Quebec. These regions are simply the sub-regions of actual regions.  All the actual 
regions are also the sub-regions of Canada, which is also shown as single region. This makes the total
number of regions and sub-regions equal to 23.

However, the measures and other calculations will be 
applied only on actual regions. The units used for the amount from trade sales are Dollars and the 
associated values are scaled down by 1000 times as given in the title. The data quality levels are 
also labelled using alphabet A to F, A being the most accurate or of excellent quality. 
There are about 30 industry categories and two modes of Sales, namely Total Retail Sales and Retail
e-commerce sales; former being over 99% of all of the sales. Data form also has two categories 
seasonally adjusted and unadjusted. 13 % of sales Values are null and the corresponding cells to
null values are labelled x in the Status column. Column profiling option in Power BI also shows 
that about 9000 cells have x. This means that out of 13% (10319 data points) unavailable data, 
8980 data points are suppressed due to confidentiality reasons.
Details of other StatCan units and columns which are more important only for internal references
are given in a supporting document named ‘STATCAN Format Columns’. Sales column has two 
categories: Total, retail sales and Retail E-commerce sales where E-commerce are less than 1 %.

------------------------------------------------------------------------
# Data Cleaning
The columns explained above are only 7. The rest of the columns in the dataset are not mentioned
above as they were removed from the dataset. The removed columns are useful to understand a grain
of data properly, however, they are not desired in dashboard for analytic purposes. The seven 
columns were renamed to make them more understandable in simple language. 
Data Preparation
All the data types were left as they were. The date column namely Dated is the only of type Date
whereas rest of the columns are of text type. To avoid unnecessary confusion and potential mistakes
of double counting, the sub-regions of provinces were filtered out during the transformation stage.
The provinces and territories plus Canada was kept, in case, if National versus Provinces comparisons
were to be made. The sketch of dashboard is planned based on the questions to be answered.

# 📌 Dashboard Building and its Components
 The decided components of the Dashboard are as follows:
•	Visual 1: A line chart of the Sales_Total Retail Amount versus the Year and Month. The subtitles 
and legend displays details of calculations employed. 
•	Visual 2: A vertical clustered bar chart of Sales Amount by Categories over years. 
•	Visual 3: A horizontal bar chart of the regions over the Region_Total Retail Amount.
•	Four slicers including Year, Industry, Data Form and Sales.
•	3 KPIs: Total Retail Amount, Year over Year and Month over Month.

# 📷 Dashboard Preview

A few snaps from the dashboard are given below:

## Main Dashboard
![Dashboard](main%20dashboard.PNG)

## Seasonally adjusted trend
![Seasonally Adjusted trend](seasonally%20adjusted%20trend.PNG)

## Cannabis Sales
![Cannabis Sales](Cannabis%20salesPNG)

------------------------------------------------------------------------

# 🔎 Answers to the questions asked.

Q1. How have total retail sales trended monthly/yearly from 2017 to mid-2026, and is there a visible
 seasonal pattern?
Visual 1 displays the total retail sales have been gradually rising for the years from 2017 to mid-2026.
 The overall retails has reached to 21.05 billion dollars till June 2026. The sales by individual years
can be seen in Total Retail Sales KPI by applying yearly selections in the year slicer. For example, in
2017, the total retail sales were equal to 1.87 billion, then it kept gradually increasing till the end
 of June 2026.
However, the monthly trend of total retail sales is almost the same each year of the period. Every year,
 the trend consistently remains the same with an exception of April 2020. Generally, the sales begins
slowly from January, then gradually rises in February. After that from March till December, the highs
and lows become very smooth.

Q2. How does e-commerce retail sales compare to total retail sales over time — is e-commerce's share growing?
It can be seen in visual 2 that e-commerce retails are negligible compared to total retail sales over all the
 months. They differ roughly by multi-folds throughout this period. Using Sales slicer, it can also be seen
that, 2025 has the highest e-commerce sales which barely reaches 119 million. On the other hand, the lowest
e-commerce sales are in 2017 that is under 32 million. It, however, has a rising trend over the years. The
 overall trend of both categories of sales can be considered the same, however, the scale of retail sales
amount are dramatically different.

Q3. Which provinces/regions have the highest and the lowest retail sales, and how does that ranking hold up
 over time? 
The ranking is established over all Canadian provinces and territories in visual 3. The highest and the lowest
 retail sales have been very consistent over the given period. Ontario, Quebec and British Colombia are
consistently the top 1, 2 and 3 regions respectively. The overall Ontario’s sales reach about 8 billion
whereas Nunavut represents the lowest rank with 13 million of sales.

Q4. Are there specific periods (e.g., 2020) where sales patterns broke from the norm, and how visible is
 that in adjusted vs. unadjusted data?
As mentioned above, every January and February are slower than the other months which are seasonal trends
as they can be seen consistently throughout the period. However, April 2020 is the most unusual dip in the
 pattern. With the use of Data form slicer, seasonally adjusted filter displays the overall trend more
smoothly. Under this setting, the seasonal dips of January and February are diminished resulting in the
 even more prominent unusual dip around April 2020. 

Q5. What's the most recent month's performance compared to the same month a year prior?
The most recent month would be June of 2026. The comparison of the performances of the most recent month
 and the same month in the prior year can be displayed Total Retail Amount by selecting specific months.
 In the most recent month, the retail sales amount is 235.94 million whereas the retails sales amount in
 the same month prior year is 209.87 million. This reveals 6.22% YoY growth from June 2025 to June 2026.

# Additional Insights
The dashboard is built more than just displaying answers to the questions asked. An important visual that
 has not been discussed yet is Industry slicer. There are about 30 different industries contributing in
 this retail record. Single industry based insights can be revealed using the industry slicer. For example,
 when Beer, wine and liquor industry is selected, valuable information is revealed. The dashboard shows
 that overall 240.6 million retail sales have been made, annually it has grown by 4.06% and British
Colombia beats Quebec in ranking, however, Ontario still holds the rank 1. The overall trend of liquor
industry over time is also very similar to that of all the industry together.
In case of Cannabis industry, the overall trend shows much more prominent rise from 2017 till 2026.
 Alberta beats both British Colombia and Quebec here and becomes second highest retail sales amount
generator.
Dashboard is free to use to explore more insights of the dataset from industry viewpoint or any other
perspective. More detailed document is attached as pdf.


