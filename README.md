# Data Wrangling Basics in R

This repo contains files for an in-class activity (class activity 1)
introducing the class to data wrangling functions from the `dplyr` and `tidyr`
packages.

HUDK 4050 is the first of three core courses in the Learning Analytics MS at
Teachers College, Columbia University focusing on the thinking, methods, and
conventions in data science. Particular attention is given to the fields of
Educational Data Mining and Learning Analytics. Refer to the
[Syllabus](https://github.com/timothyLeeXQ/HUDK-4050-Syllabus) (forked from
the [main repo](https://github.com/core-methods-in-edm/syllabus) which may
contain updates for future class iterations) for more information on HUDK 4050.

Other classes in the series are:
* [HUDK 4051: Learning Analytics:
 Process and Theory](https://github.com/timothyLeeXQ/HUDK-4051-Syllabus) ([Main
 repo](https://github.com/la-process-and-theory/syllabus))
* HUDK 5053: Feature Engineering Studio (Starting in May 2020.
 [Main repo](https://github.com/feature-engineering-studio/syllabus))

## Instructor Notes

### Data Manipulation

In this repository you will find data describing Swirl activity from the class so far this semester. Please connect RStudio to this repository.

#### Instructions

1. Open a new R Markdown file, please write and run all your commands from within the R Markdown document  
2. Delete the contents of the Markdown file and insert a new code block
3. Load the libraries  `tidyr` and `dplyr`
4. Create a data frame from the `swirl-data.csv` file called `DF1`. The variables are:
  - `course_name` - the name of the R course the student attempted  
  - `lesson_name` - the lesson name  
 - `question_number` - the question number attempted
 - `correct` - whether the question was answered correctly  
 - `attempt` - how many times the student attempted the question  
 - `skipped` - whether the student skipped the question  
 - `datetime` - the date and time the student attempted the question  
 - `hash` - anonymised student ID  
5. Create a new data frame that only includes the variables `hash`, `lesson_name` and `attempt` called `DF2`
6. Use the `group_by` function to create a data frame that sums all the attempts for each `hash` by each `lesson_name` called `DF3`
7. On a scrap piece of paper draw what you think `DF3` would look like if all the lesson names were column names
8. Convert `DF3` to this format  
9. Create a new data frame from `DF1` called `DF4` that only includes the variables `hash`, `lesson_name` and `correct`
10. Convert the `correct` variable so that `TRUE` is coded as the **number** `1` and `FALSE` is coded as `0`  
11. Create a new data frame called `DF5` that provides a mean score for each student on each course
12. **Extra credit** Convert the `datetime` variable into month-day-year format and create a new data frame (`DF6`) that shows the average correct for each day
