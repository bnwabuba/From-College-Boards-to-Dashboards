# From-College-Boards-to-Dashboards
Turning Raw Student Data Into Actionable Insights for a Community College Using Amazon QuickSight &amp; Amazon Q

##Project Overview

This project simulates a real-world consulting engagement with a U.S. community college seeking better visibility into its student population, enrollment patterns, and academic trends.

The college leadership currently depends heavily on static reports from various departments—admissions, academic affairs, and student services. These reports are fragmented,  slow to update, and not optimized for decision-making.

My job: <br>
Transform these disconnected sources into an interactive, intelligence-driven analytics dashboard using Amazon QuickSight and conversational analytics through Amazon Q Topics.

The result: <br>
A centralized, dynamic, and AI-enabled insights portal that helps administrators make data-driven decisions about recruitment, resource allocation, and student success.

##Key Problem

College leadership lacked:

- A unified view of student demographics

- Insights on program popularity & student progression

- Easy ways to ask natural-language questions like “Which instructors received the highest evaluations?” or “How many sophomores enrolled this term?”

Manually compiling answers took hours.
This project solves that with automated dashboards + Q-powered analytics.

 ##Project Objectives

1. Clean & Prepare Dataset (student records, evaluation data, demographics)

2. Standardize Business Terms (rename fields like HomeOfOrigin → NationalOrigin)

3. Create Calculated Fields (e.g., Student Type)

4. Develop an Interactive Dashboard in Amazon QuickSight

5. Build an AI-powered Topic using Amazon Q

6. Enable Verified Questions for trusted insights

7. Deliver 1-click stories inside QuickSight for leadership meetings

 ##Technologies Used
Tool	                           |                                     Purpose              |
|-------------------------------------|----------------------------------------------------------|
|Amazon QuickSight	             |                   Data modeling, visualization, storytelling |
|Amazon Q (Topics)	             |                   Natural language analytics & verified answers|
|AWS IAM Identity Center	       |                   User and group access management|
|Excel / CSV	                   |                  Base dataset preparation|

Storytelling: The Journey From Raw Data to Data Insights  <br>

1️⃣ Importing & Understanding the Dataset

The dataset included:

- Student ID, Name, Gender, Age

- Program of Study

- Enrollment Term

- Academic Standing

- Instructor Ratings

- Student Classification

- HomeOfOrigin (renamed)

Before building dashboards, I transformed business language to reflect how real colleges categorize students.

2️⃣ Data Modeling & Field Standardization

Examples of key transformations:

Original Field	                    |                  Updated Field	              |                           Reason    |
|-------------------------------------|------------------------------|---------------------------------------------------------|
|HomeOfOrigin	                       |    NationalOrigin	                  |             Clearer meaning, globally recognized |
|StartTerm	                          |    EnrollmentTerm	                  |            Matches higher-ed conventions |
|EvalScore	                          |   InstructorEvaluationScore	        |            Better analytics naming  |

3️⃣ Calculated Fields

 Student Type
Used to better segment the student body (Freshman, Sophomore, Junior, Senior, Graduate).

Formula example (QuickSight):

ifelse(  <br>
   {Credits} < 30, "Freshman", <br>
   {Credits} < 60, "Sophomore",  <br>
   {Credits} < 90, "Junior",   <br>
   {Credits} < 120, "Senior",   <br>
   "Graduate"       <br>
)  <br>

4️⃣ Building the Dashboard
Main Insights Panels:

A. Enrollment Overview

- Total active students

- Year-over-year enrollment growth

- Breakdown by student type

B. Gender & Origin Demographics

- Male vs Female distribution

- Top home origins / nationalities

C. Instructor Evaluation Trends

- Top instructors by average score

- Courses with highest/lowest satisfaction

D. Academic Standing

- At-risk vs high-performing students

- Program-level performance

📌 Screenshots go here:
![Dashboard Overview](From-College-Boards-to-Dashboards/dashboard_overview.png)

5️⃣ Adding Amazon Q Topics (Natural Language Analytics)

I created a Topic named:

📌 Regional Community College Student Data

Then configured:

- Field synonyms for user-friendly queries

- Verified Questions, such as: “Which instructors got the best average evaluations?” , “How many freshmen enrolled this term?”

This allows leadership to ask questions without needing SQL or BI skills.

![Verified Questions](From-College-Boards-to-Dashboards/Topics.png)

6️⃣ Creating a Data Story (Narrative Insight)

I added a pie chart showing student type distribution:

Student Type	 |    Count	   |      Percentage |
|-------------|-------------|------------------|
Freshman	      |   180	      |       18%  |
Sophomore	     |    137	     |      14%  |
Junior	        |   229	      |       23%  |
Senior	       |    192	      |       19%  |
Graduate	      |   262	      |       26%  |

![Pie Chart](From-College-Boards-to-Dashboards/Pie Chart.png)

 Story Block Added: <br>

The student population shows a balanced academic distribution with a healthy progression pipeline. Graduate students form the largest segment at 26%, indicating strong interest in continuing education programs. Juniors and Seniors collectively make up 42% of the population, demonstrating positive retention toward upper-level standing. Meanwhile, Freshmen and Sophomores represent 32%, showing steady new student inflow.


 Final Deliverables <br>
✔️ Interactive QuickSight Dashboard  <br>
✔️ Amazon Q Topic with Verified Questions  <br>
✔️ Cleaned & Standardized Datasets  <br>
✔️ Data Story for leadership presentation  <br>


  ## Impact

This project demonstrates the power of cloud-native BI + AI in education:

- Leadership gains instant answers through Q-powered queries

- Dashboards offer continuous, up-to-date visibility

- Data stories transform analytics into clear executive communication

- Improves recruitment strategy, resource allocation & student success planning

  ## Future Enhancements

- Add machine learning predictions (retention risk scoring)

- Automate data ingestion with AWS Glue

- Add instructor performance over time with anomaly detection

- Enable row-level security for department-based access


👤 Author

**Blessing Nwabuba**
Data Analyst • BI Developer • AWS Enthusiast <br>
📍 Lagos, Nigeria  <br>
🔗 LinkedIn: [https://www.linkedin.com/in/blessing-nwabuba/]
