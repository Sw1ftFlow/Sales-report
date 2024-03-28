# Sales-report
PowerBI report that is performance optimized and made for ipad users. 

# Requirements
The report needs to be fast and no visual should have a load time longer than 1000 ms. The report is used by many sales people at once, each from different regions where internet connection sometimes may be weak. 

Since they all use Ipads or Iphones the report works slower on these devices than on a desktop because of the ios operating system does not run PowerBI as well as Windows for various reasons. 

The report is used by sales people out in the field to get a better understanding of the sales in their district and particular stores. 

# Pages and visuals
The canvas size is optimized for Ipads and there look the way it is. I wanted to fit all information on each page so the user never have to scroll. 
When creating the report I was very limited with the amount of visual elements I could use because each new element mean more rendering and a longer load time. 

Page 1. Here the user can pre-filter the report to reduce the data size by loaded by slicing the data on their district or store.

Page 2. Show sales on a district level. Large tables are only showing top 10 initially and can be expanded by using the toggle buttons. This greatly also reduces the initial data load. 

Page 3. Shows sales on store level. Again, large tables show top 10 and can be expanded by using toggle buttons. 

# Data Model & Power Query
The data model is a normal snowflake schema and most of the data is transformed and loaded via custom sql queries apart from some transformations in a few tables. Incremental refresh should be implemented on the fact table and all data wrangling should be pushed upstream to report views but the old architecture did not support it hence it is not implemented in this report. 

# Row level security
Row level security is applied to the Store and Product table  
