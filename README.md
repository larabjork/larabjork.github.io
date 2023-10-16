![A woman with curly brown hair is smiling at the camera](/assets/lara_headshot.jpg)

# From Data User to Data Analyst
I'm a former grant writer who has always been interested in how to reliably track nonprofit organizations' impact. A running theme in my grant-seeking life: Longing to be able to look up the latest stats on our performance, with reports available at the click of a button.

Instead, I would often have to email a colleague (or more often, colleagues) who had many other responsibilities on top of tracking key indicators. I got used to hearing that they were in the process of updating the spreadsheet, and could they get back to me next week, and would last quarter's results be okay? Sigh.

After I wrote my final grant proposal, I started building my tech skills. When I discovered data analytics, I was home. Tools to clean up messy data? Graphs and charts that could get to the point more quickly than any paragraph? Dashboards, connected to data sources, with up-to-the-minute information? Yes, please!

I've always been a subject matter generalist, and that's put me in a good position to take the perspective of an interested but nonexpert stakeholder. Even for issues that I'm passionate about, like ending homelessness and protecting the environment, I bring that viewpoint to data visualizations and written analyses.

When I'm not deep in data, you can find me walking in my neighborhood taking pictures, knitting yarn that I inherited from my grandmothers, and baking bread and cookies.

# Project Work: ETL for East African Entrepreneurs
In February 2023, I undertook a short-term contract with [Inkomoko](https://www.inkomoko.com/) (approximate pronunciation: "in-HO-mo-ko"), which provides impact investing and business advice to entrepreneurs in East Africa.

## Scope of Work
*Goal:* Executive leadership needed an accurate, up-to-date dashboard  of the organization's impact over time. Work was already underway on a Power BI dashboard.

*My Initial Task:* Many of the formulas to present organizational impact metrics had already been developed. My task(or so I thought) was to finish up the remaining formulas and create associated visualizations.

## Challenge: Tangled Data Model
Inkomoko conducts baseline and endline surveys with a sample of its clients in each location. Data flowed from the survey tool (Kobo Toolbox) to a MySQL database and then to Power BI.

However, there was no restructuring of the data from Kobo Toolbox to MySQL. Each survey was stored as a separate table and exported to Power BI, resulting in 98 tables for the years I was focused on (2017-2021). Although the surveys captured related information, there was a wide variety in how related columns were named. On the Power BI side, there were also a large number of irrelevant columns that were still imported.

The data model didn't support much-needed functionality of being able to filter (or in Power BI terms, "slice") by subcategories of clients like women, refugees & displaced persons, and youth.

After attempting to work within this structure, I had an unstoppable argument for a better way: We hit the maximum number of columns allowed in Power BI at 16,000, even though we had more data from 2022 surveys to include.

Visually, the dashboard design was also in need of a refresh.

## Results
*New data model:* Once I had organizational buy-in, I developed a streamlined data model and embarked on transforming the data to fit it. The new data model has 3 tables with 40 columns, and it supports filtering by country, year, program, and demographic group.

Key elements of the new model:
* Combining all baseline surveys into one consolidated table (rather than 49 separate tables); same for endline information
* Including only necessary columns within these two consolidated tables

Additional data transformation was also needed:
* Filtering out data for inactive businesses and for "control group" members
* Standardizing values and data formats (for example, some surveys had recorded "male" or female", while others used 0 for male and 1 for female)

*Design:* The Strategic Operations Consultant, who supervised my work, sketched out a new dashobard layout, and I completed its implementation.

## Hand-off
While I was keeping this project moving, Inkomoko created and hired a 3-person data team. Staff members in these new roles took over where I left off, with additional data from 2022 onward as well as older data (2012-2016). In addiiton to sharing the Github repository, I also provided them with a written list of work performed to date and tasks remaining, which we reviewed together.

