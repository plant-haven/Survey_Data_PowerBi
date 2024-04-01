# Data Professional Survey Visualization with PowerBi
This project utilizes a survey dataset provided by Alex the Analyst.
The original file is Power BI - Final Project.xlsx.

## Steps
Loaded Excel dataset in power query

Removed columns that are blank and not necessary: Browser, OS, City, Country, Referrer

Split the columns:

I split the columns 'Q1 - Which Title Best Fits your Current Role?' and 'Q4 - What Industry do you work in?' by delimiter '(' so the roles and industries that were typed in under the '(Other)' response only contain 'Other' instead of the rest of the text. 
I also split the column 'Q5 - Favorite Programming Language' by delimiter ':' so the programming languages that were typed in under the 'Other:' response only contain 'Other' instead of the rest of the text typed in.

This results in fewer options/filters which will clean up the data.

I copied column 'Q3 - Current Yearly Salary (in USD)' and split it by digit to non-digit. 
Result:

![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/99fd8925-63b5-4229-96b1-00c3a0eeb949)

I removed the third column.
I replaced all the values for the second column with 'k' to '' and '-' to ''. 
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/3e91305a-5ccb-4164-8632-53da9963fe97)
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/32bd0036-8397-420e-a9aa-ae55e04a5f08)

One of the survey's current salary options was 225+ so when I split the column by digit to non-digit, this resulted in the first copy having 225 and the second copy having '+'. 
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/b8cebbba-e410-4ec2-9974-ab2194230f7f)

The 225 needs to be in the second copy to be able to take the average so I replaced '+' with '225'.

I changed the first and second copy columns' type into whole numbers because they were text. Then, I added a custom column called 'Average Salary' which gets the average salary using the first copy column and the second.

![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/b455a520-4cc6-4dfa-8145-0450de3c03d4)

I deleted both copies because they are no longer needed now that there is an 'Average Salary' column. I then moved the column to be after the 'Q3 - Current Yearly Salary (in USD)' column.

I split the columns 'Q11 - Which Country do you live in?' by delimiter '(' 

Then I begin on the visualization

The first part of the dashboard is a card of the distinct count of unique IDs with the label/title 'Count of Survey Takers'.
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/8ae08bec-9c31-4147-b607-f1dd7d38ad4e)

The second part of the dashboard is another card of the average age of the survey takers with the label/title 'Average Age of Survey Taker'

![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/6272a4e6-f9ba-4326-8c9d-edc4e2d37dad)

The 1st visualization is a stacked bar chart that displays the average salary based on the role.
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/a78e8635-413b-4010-a564-ceacee6c18d0)

The 2nd visualization is a stacked column chart that displays the count of each favorite programming language with all of the unique IDs included.

![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/abcb9259-96b1-4e4b-ac66-8421b2d6c512)

The 3rd visualization includes a treemap of each distinct country the survey takers live in. I can click on any country and the other visualizations will filter themselves based on the country chosen. 
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/9c50a45c-c92f-43de-8c86-1d9e86770966)

The 4th and 5th visualizations are gauges that display the average rating of 1-10 for happiness with work/life balance and salary.
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/d515bebb-fa84-4e36-8505-9cc3d62aacf0)

The 6th visualization is a donut chart that shows the count of each option of the difficulty of breaking into data. 
![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/7f7b245e-cf2c-4985-9480-a174e125dfa6)

## Result

![image](https://github.com/plant-haven/Survey_Data_PowerBi/assets/94200274/4133dcce-53ab-420c-b7cb-86d5ef6bbcd2)


