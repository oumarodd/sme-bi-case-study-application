# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The goal of exercises in case study is for learners to apply what was learned in the previous courses to new problems or situations. This is best pedagogical practice for retaining and building skills.
- We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/case-study-analyzing-customer-churn-in-tableau/exploratory-analysis-1?ex=4) from the Case Study: Analyzing Customer Churn in Tableau. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners in **case studies**.

## 1st VM Exercise

#### Dataset

- [ ] Add datasets used to the `datasets/` folder

#### Files

- [ ] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix`, depending if you are auditioning for a Tableau or Power BI course.
- [ ] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix`

#### Learning Objective

*One measurable learning objective that this exercise assesses*



#### Context




In this exercise, we will do some data cleaning and make sure that our date formats correctly in Tableau. This exercise is important since date is the single most important unit of time when doing analysis and if not formatted correctly, then no trends analysis can take place. Wrong formatting of date will not be enable us to do day, month, day of the week analysis on Tableau. Given different timezones around the world, we also have to ensure that the data is in the correct timezone, if dealing with time instances.

#### Steps to be executed by the student (max 6)


Step 1 :Import the datasource and explore the date fields.On careful examination, one can see that the date field is in 5 digit numerical form eg. 48413. We will convert to the standard date format by creating separate fields for day,month and year and then concatenating them to recreate the date field


Step 2: Create calculated field with ‘2013’ and name it Year and convert to integer
Ans: Year = int(2013)
Step 3 Create a calculated field for the day by using the datepart formula
Ans ::Day = DATEPART('day',[Date])
Step 4: Create a calculated field for the month by using the datepart formula
Ans: Month = DATEPART(month,[Date])
Step 5: Use makedate formula to combine Year, Month, Day to create Date column and rename it :UpdatedDate
Ans:MAKEDATE([Year],[Month],[day])


#### Exercise question:

Bring the new date column (UpdatedDate) into the Rows section and click on the pill to expand it to Day of Week. When was the 16th of July 2013? Tuesday

#### End goal:

<img width="1159" alt="image" src="https://user-images.githubusercontent.com/17188971/206798339-f85ae0bf-c284-4aab-829b-b04d556edd58.png">

## Finalized Workbook

#### Files
You can upload your final workbook in the exercises folder as `ex-final-sol.twbx` or `ex-final-sol.pbix`.

#### Explanation & Description
By building the visualization, the learner will be able to learn how to first use parameters as filters. Then learner will be able to note which day of week has the highest volume of calls, which day of week has most amount of abandoned calls.
#### End goal:

*Add an image of the final visualization here.*
