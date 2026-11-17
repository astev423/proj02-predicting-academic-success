# Project 02 Proposal: Predicting Academic Success in California Schools

**Team members:** Alexander Stevens

See the [Project 02 instructions](https://data385.netlify.app/project/proj02_wholegame) for what goes in each section. Bullet points are great. Put any images in an `img/` folder.

## 1. Problem statement

_Who has the problem, what decision or need it involves, why it matters, and what you expect to find._

- I want to help schools and students by ensuring students are as academically successful as possible. This is a problem that affects school faculty and students. Solving this problem requires looking at data to determine what correlates with negative academic outcomes and how faculty and students can change their ways to minimize those negative outcomes. This problem matters a lot for students since academic success is strongly correlated with success in life and it matters for school faculty as their funding and revenue often depends on how many students they have and how well their students do.
- Through examining this problem I expect to find academic success is dependent on many variables rather than just a few. I suspect there will be a few obvious factors like not attending class to lead to worse outcomes, but I also suspect there will be a few things I find surprising in the data.


## 2. Research question

_A clear association between a response and at least one predictor variable._

- I want to examine how factors such as absenteeism, school district, staff count, and economic conditions affect the academic success of students, such as their assessment scores and graduation rates.

## 3. Data acquisition

_In 1-2 sentences, describe the data you intend to collect and how you will get it._

- I intend to use educational data records collected by the California Department of Education. On that site they have many datasets of several formats (csv, XLSX, etc) and each dataset corresponds to a particular year and topic such as assessment scores, foster youth, and graduation rates.
  
### a. Confirm viability

_Scraping: summarize the "Before You Scrape" checklist. Downloading: citation, link to the documentation, and how the data were originally collected. Collecting it yourself: how you are collecting it and where you are storing it._

- I am using data from the [California Department of Education's website](https://www.cde.ca.gov/ds/ad/downloadabledata.asp). This data is collected by individual schools then reported to the Department of Education.

### b. Variables of interest

_If you do not have the data yet, list the variables you plan to collect and the exact question text. Include 1) the variable name, 2) data type 3) description. Use bullet points._

| Variable name | Description | Quantitative or Qualitative |
| :--- | :---: | ---: |
| District Code	 | A unique five digit code for the district | Quantitative |
| County Name | Name of California county |  Quantitative |
| School Code | A unique seven digit code for the school. |  Quantitative |
| Chronic Absenteeism Rate | Rate of students absent more than 10% of school days |  Quantitative |
| Percentage Below Proficient | Percent of students with test scores below proficient |  Quantitative |
| Percent (%) Eligible Free (TK/K-12) | The percent of students eligible for free meals |  Quantitative |
| Regular HS Diploma Graduates (Rate) | The percent of students who received a standard diploma |  Quantitative |
| TOTAL | Total fluent-English-proficient (FEP) students |  Quantitative |

## 4. Data example

_Scraping: a URL and an annotated screenshot. Downloading: a link to your rendered `data_management.pdf` with `glimpse()`. Collecting: a screenshot of one example row._

[Link to data management pdf](https://github.com/astev423/proj02-predicting-academic-success/blob/main/data_management.pdf)

## 5. EDA

_The techniques and functions you plan to use to import, wrangle, visualize, and explore the data, and why each is needed._

- I will need to use functions to read the various file formats like read_csv() and read_excel(). Since the data is spread into different sheets I will need to use different joins, such as left_join(), to gather a complete dataframe, then save that with write_csv().
- I expect to use mutate() and case_when() to make values better suited for graphing, such as changing percentages to numerical values. 
- I expect to use filter() and select() to hone in on the exact rows and columns I need and then summarize() to gather sums, means, IQRs, etc.
- I expect to use a lot of bar and column plots as there is a lot of categorical and numerical data and I find these plots are great at visualizing data. I will also use box plots to represent the range of different grades for a given categorical group.


## 6. Modeling

_The models you plan to use, your response and predictor variables, and why the models fit your research question._

- I plan to use simple linear models and multiple linear regression as they can do a great job of predicting how academic outcomes are affected as one or more variable changes such as English proficiency. My response variables are academic outcomes such as rate of students below proficiency for assessments, drop out rate, and graduation rates. My predictor variables will be variables such as school district, chronic absenteeism rate, percent of students receiving free meals, and English proficiency rate.

## 7. Communicate

_How you plan to present your results (website, poster, or short slide presentation)._

- I will communicate my results using a slide presentation with graphs and numeric summary results.

## 8. LLM disclaimer

_Whether and how you will use AI tools: the specific tool, its use, and your data protection methods. If you won't use any, say so._

- I plan to use LLMs to help come up with interesting ideas to explore using my data and to debug any errors I encounter with R. The LLM I plan to use is ChatGPT. This data is already public information and doesn’t contain any highly identifiable info such as name, birth date, or zip code, but I will still avoid pasting information from the dataset into ChatGPT to ensure I follow best practices.

