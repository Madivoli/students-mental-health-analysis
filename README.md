## ANALYSING STUDENTS' MENTAL HEALTH 

**PROJECT OVERVIEW:**

Does going to university in a different country affect your mental health? A Japanese international university surveyed its students in 2018 and found that international students have a higher risk of mental health difficulties than the general population, and that social connectedness (belonging to a social group) and acculturative stress (stress associated with joining a new culture) are predictive of depression. The project aims to explore 286 student records using MySQL to determine if a similar conclusion can be drawn for international students and whether the length of stay is a contributing factor.

---
**DATA DICTIONARY**

The data contains the following columns:

| Field Name    | Description                                      |
| ------------- | ------------------------------------------------ |
| `inter_dom`     | Types of students (international or domestic)   |
| `japanese_cate` | Japanese language proficiency                    |
| `english_cate`  | English language proficiency                     |
| `academic`      | Current academic level (undergraduate or graduate) |
| `age`           | Current age of student                           |
| `stay`          | Current length of stay in years                  |
| `todep`         | Total score of depression (PHQ-9 test)           |
| `tosc`          | Total score of social connectedness (SCS test)   |
| `toas`          | Total score of acculturative stress (ASISS test) |

---
---
## EXPLORATORY DATA ANALYSIS

**Descriptive Statistics:**

The analysis revealed **an average age of 22 years for both genders**, with **a higher number of females (70) compared to males (57)**. Additionally, there were **disparities in various scores between the genders**. For instance, males exhibited greater social connectedness, scoring 38 compared to females' score of 37, suggesting that **a larger proportion of males belong to social groups**. Conversely, females outperformed males in Auditory Processing Disorder (APD) scores, receiving a score of 1057 compared to 956 for males. This suggests that **females may encounter greater difficulty in understanding speech, particularly in noisy environments, which can result in challenges with language comprehension, reading, and following directions.**

<img width="1500" height="150" alt="image" src="https://github.com/user-attachments/assets/e4ad2325-9fd9-49ae-94f5-aa74bf31e351" />

The analysis indicates that, on average, **students remain enrolled at the university for approximately 2.15 years**, with **a minimum duration of 1 year** and a **maximum of 10 years**. The **standard deviation of about 1.33** suggests that **there is fairly consistent variability in the length of stay among students**.

<img width="1500" height="94" alt="image" src="https://github.com/user-attachments/assets/b7253f18-669e-4961-bca5-90707157797d" />

---
**Frequency distributions:**

To gain a clearer understanding of the age and APD (Auditory Processing Disorder) distribution within the dataset, **age values were segmented into specific age groups or bins**. The analysis revealed that the **age group 20-24 had the highest distribution across both genders, with 41 females and 34 males**. Conversely, the **age group 30-34 showed the lowest distribution for both genders**.
		
<img width="1037" height="452" alt="image" src="https://github.com/user-attachments/assets/b94dab3b-48cf-4e3f-ac39-bfdb67ad643d" />


Further analysis focused on **the distribution of APD scores among females**. It indicated that **those in the 20-24 age group were the most significantly affected by APD**, followed by individuals in the 15-19 age group. **Females in the 30-34 age group were identified as the least affected**. The analysis suggests that **further diagnosis and treatment should be conducted by an audiologist**, using specialized tests to evaluate the brain's ability to process sound rather than merely detect it. This approach combines test results with information provided by teachers or parents.

<img width="1517" height="602" alt="image" src="https://github.com/user-attachments/assets/0e97d9ac-9512-4b61-af56-c5482198ade4" />

**International students in the 20-24 age group constituted the largest population**, followed by both domestic and international students aged 15-19, each with 21 students. Conversely, **international students in the 25-29 age group were the least represented in the sample data**. Based on these findings, **we can conclude that the majority of students at the Japanese University were from abroad**.

<img width="1500" height="847" alt="image" src="https://github.com/user-attachments/assets/72fc6280-4b2d-4ca4-941d-fac9c0fd3dc8" />

Based on the analysis, **there are 247 undergraduate students and 21 graduate students**. This implies that the **majority of students who participated in the study were undergraduate students**.	

<img width="1502" height="617" alt="image" src="https://github.com/user-attachments/assets/0b94998c-3268-475c-8057-a8147c7b3aff" />

---
---
## INFERENTIAL STATISTICS

**Correlation between students' status and depression and between gender and depression:**

<img width="1500" height="100" alt="image" src="https://github.com/user-attachments/assets/60712f10-0934-44a2-94c4-5821e978f122" />
	

**Interpretation:**

Depression and students' (international or domestic) status:

**Coefficient: -0.172646634**

The coefficient suggests **a weak negative relationship**, implying that **there is a linear relationship between a student's status as either international or domestic and their depression score**, though its weak. Thus, **international students are more inclined to fall into depression than domestic students.**


Depression and gender:

**Correlation Coefficient: -0.046209021**

This value signifies **a very weak negative correlation.** Since the coefficient is close to zero, **there is no linear relationship between a student's gender and their depression score**. The negative sign suggests that, **on average, males may have slightly lower depression scores than females**. However, **this difference is minimal.**

---
**Correlation between depression and social connectedness and between depression and acculturative stress**
<img width="1500" height="94" alt="image" src="https://github.com/user-attachments/assets/3ff1af94-d96c-419c-82e2-43bb35ba1f7e" />

**Interpretation:**

Depression and social connectedness:

**Correlation coefficient: -0.613994843**

A **moderately strong negative relationship** exists between depression and social connectedness.  A negative correlation indicates that **as one variable increases, the other typically decreases**. Thus, **as students’ social connectedness (tosc) increases, their depression scores (todep) tend to decline.** These findings align with established psychological theories and research, which **frequently associate stronger social support and connections with lower levels of depression.**

Depression and acculturative stress:

**Correlation coefficient: 0.338242927**

There is **a weak, moderate positive correlation between depression and acculturative stress.** A positive correlation indicates that as one variable increases, the other also tends to increase. Consequently, **as a student's acculturative stress (toas) rises, their depression score (todep) also tends to increase.** This finding aligns with existing psychological research, which **frequently identifies the stress associated with adapting to a new culture as a risk factor for mental health issues such as depression.**


---
**Correlation between depression and length of stay, between length of stay and social connectedness, and between length of stay and acculturative stress**

<img width="1500" height="94" alt="image" src="https://github.com/user-attachments/assets/8af40f44-2a81-42b2-a408-d978a9f30d50" />


**Interpretation:**

Depression and length of stay:

A **weak positive correlation exists between depression and length of stay (r = 0.10094167)**, indicating that **as a student's duration of stay increases, there is minimal change in their level of depression.** 


Length of stay and social connectedness:

There is **a  weak negative relationship between length of stay and social connectedness (r = -0.0405)**, suggesting that **the duration of stay has little to no effect on social connectedness.**


Length of stay and acculturative stress:

There is **a weak positive correlation between length of stay and acculturative stress (r = 0.0040)**, implying nearly **no linear relationship between these two variables.**

---

**CONCLUSION**

**In summary, the correlation analysis reveals that neither a student's international/domestic status nor their gender demonstrates a significant linear relationship with their depression score**.

**To gain deeper insights into these relationships, further exploration using more advanced statistical techniques, such as ANOVA or regression, could be beneficial**.
