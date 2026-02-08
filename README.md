plsql_window_functions_29181_Uwase-Rubagumya-Jose

### 1. PROBLEM DEFINITION (Step 1)

1. Business Context:
"I am building a hospital management system designed to help healthcare administrators in Rwanda track patient admissions, doctor assignments, and medical billing across different departments in hospitals located in Kigali and Butare."
2. Data Challenge:
"Currently, it is difficult to identify which departments are generating the most revenue and which doctors are handling the highest patient loads. We need a way to link patient billing records back to specific departments and track how patient volumes and revenue change month-to-month."
3. Expected Outcome:
"By the end of this analysis, I expect to have a clear list of our highest-revenue departments and a better understanding of which patients are frequent visitors so we can provide them with personalized care programs and follow-up services.

### 2. Success Criteria (Step 2)

The project is considered successful if it achieves the following five measurable goals:

Top 5 Departments per Hospital using RANK()
Identifies the five best-performing departments based on revenue or patient volume to support performance comparison and decision-making.

Running Monthly Revenue Totals using SUM() OVER()
Tracks cumulative revenue over time to show financial growth trends and monthly performance.

Month-over-Month Patient Growth using LAG()
Compares current and previous month patient counts to measure increases or decreases in hospital visits.

Patient Segmentation into Quartiles using NTILE(4)
Groups patients into four segments based on activity or spending to enable targeted analysis and services.

Three-Month Moving Averages for Patient Admissions using AVG() OVER()
Smooths short-term fluctuations in admissions to reveal long-term trends for better planning.

## 3. Database Schema & ER Diagram (Step 3)
<img width="1246" height="312" alt="ERD Diagram" src="https://github.com/user-attachments/assets/5d74c7bc-0b1f-4baf-8597-5bba0b443ba7" />

## Step 4: Part A — SQL JOINs Implementation
1. INNER JOIN
 
<img width="442" height="170" alt="inner join billing" src="https://github.com/user-attachments/assets/9bfb3c50-02ae-4115-b495-666f546e7b82" />

2. LEFT JOIN
 
 <img width="404" height="143" alt="left join" src="https://github.com/user-attachments/assets/c96aaae7-e218-4625-9141-78c632a62f57" />
 
3. RIGHT JOIN
 
 <img width="377" height="147" alt="right join" src="https://github.com/user-attachments/assets/c1dcabaf-5e7b-44e7-b734-03f19e56c7bd" />
 
4. FULL OUTER JOIN
   
 <img width="462" height="231" alt="full join" src="https://github.com/user-attachments/assets/2df678b3-c49d-4817-906f-bfe6e96a03da" />
 
5. SELF JOIN

 <img width="473" height="224" alt="self join" src="https://github.com/user-attachments/assets/fd924181-b8e7-4696-a059-08e01218c071" />

## Step 5: Part B — Window Functions Implementation

1. Ranking Functions
   
   <img width="693" height="331" alt="Ranking Functions" src="https://github.com/user-attachments/assets/b1598889-c5a0-49eb-9cf1-e2a0915b6e90" />

 2. Aggregate Window Functions

      <img width="857" height="383" alt="Aggregate Window Functions " src="https://github.com/user-attachments/assets/3f2b1038-d11c-474d-8f63-9f6bef4af97e" />

 3. Navigation Functions

         
<img width="730" height="297" alt="Navigation Functions" src="https://github.com/user-attachments/assets/915714ae-18e1-44ae-a884-fab7f8ea110f" />

4. Distribution Functions

   
<img width="677" height="301" alt="Distribution Functions " src="https://github.com/user-attachments/assets/8b60f1a1-e998-47ce-b44f-8355d742aa4c" />


## Step 7: Results Analysis
1️⃣ Descriptive Analysis — What happened?

Most patients have billing records, but one patient has not been billed and one is not assigned to any department. A small number of patients contribute the highest revenue, and some departments are actively used while others have no patients. Overall billing amounts increase over time.

2️⃣ Diagnostic Analysis — Why did it happen?

Missing billing and department assignments may be due to incomplete data entry or patients not yet receiving services. High revenue from a few patients is likely caused by higher service usage or more expensive treatments. Uneven department usage reflects differences in patient demand.

3️⃣ Prescriptive Analysis — What should be done next?

The hospital should follow up on patients without billing or department assignments, improve data recording processes, and review underutilized departments. Management should also focus on retaining high-value patients and monitoring billing trends regularly.


## Step 8: References

DOCTORS AND YOUTUBE








