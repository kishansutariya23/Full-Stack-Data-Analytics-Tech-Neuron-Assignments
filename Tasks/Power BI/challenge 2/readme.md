# Get the data from Snowflake to Power BI



SNOWFLAKE
===
Note:- you can create your own table based on the data you have for that table.
1. open worksheet in snowflake and paste the below code/query.

         USE  "KS23_DEMODATABASE";

         CREATE OR REPLACE TABLE KS23_HEALTHCARE(
             Patientid VARCHAR(15),
             gender CHAR(5),
             age VARCHAR(5),
             hypertension CHAR(20),
             heart_disease CHAR(20),
             ever_married CHAR(30),
             work_type VARCHAR(60),
             Residence_type CHAR(30),
             avg_glucode_level VARCHAR(20),
             bmi VARCHAR(20),
             smoking_status VARCHAR(20),
             stroke CHAR(20)
         );

         select * from KS23_HEALTHCARE;
 

2. select all and click on run button.

3. Load the data(csv/excel) in the snowflake
    - click Databases and select your database name where you have created the table mine is ["KS23_DEMODATABASE]
    - select the table mine table name is [KS23_HEALTHCARE]
    - click on load then select the warehouse name-->next--->upload the excel/csv file---> then choose the file format or create it then load.
4. now once run below query inside the worksheet to see the data is loaded or not
        
        select * from KS23_HEALTHCARE;



Power BI
===
1. Click on *Get data* in **Home** Tab and from there select **Snowflake** or search for **Snowflake**.
2. Now give the server name as :- [cr12345.ca-central-1.aws.snowflakecomputing.com]
    - any thing between https:// & till .com in the URL of classic snowflake account is your server name.
    [https://cr12345.ca-central-1.aws.snowflakecomputing.com/oauth/authorize?.........]
3. Give the **Warehouse** name where the data is stored.
4. It will ask the User ID & Password give it and you will be login in snowflake inside Power BI.
5. Now select the data i mean table which you want to load inside Power BI. and if your data is live data, means it gets updated periodically then select accordingly in pop-up message *Connection Settings*(DirectQuery or Import) from Power BI, so that data is up-to-data.
    - in industry we use DirectQuery as it means data is updated periodically
6. Your data is loaded and you can see the table in **Fields** tab in right side in power BI.

7. Make sure you have data in snowflake for that run the * query with limit 5 for conformation.

------
Below is my chart made in Power BI for the data which was present in SNOWFLAKE then loaded in POWER BI.

