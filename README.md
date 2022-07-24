# Pewlett-Hackard-Analysis

### Overview of the analysis
Pewlett Hackard is anticipating a massive changeover in their personnel due to an expected wave of retirees. To help prepare for this "silver tsunami," I used SQL to determine the number of employees that may be retiring per job title, and to help identify candidates to serve as mentors for their replacements.

### Results
- There are over 70,000 employees who are about to retire

![image](https://user-images.githubusercontent.com/107162310/180629763-3c518a43-1e1c-4689-aa53-7d31a8d2a0f3.png)

- Senior Engineers & Senior Staff are the job titles that are going to be most impacted by the "silver tsunami," each with over 2.5 times as many expected retirements as the next nearest job title

![image](https://user-images.githubusercontent.com/107162310/180629329-9a5c0d3a-9a16-4743-bdb7-3b6e0f7cc319.png)

- The 50,842 employees with a senior job title retiring soon account for over 70% of the total expected retirees.

![image](https://user-images.githubusercontent.com/107162310/180630655-343f19e9-5dd9-4c89-b5f4-bf853ea68438.png)

- There are only about 1,500 employees that fit the criteria for the mentorship program.

![image](https://user-images.githubusercontent.com/107162310/180630742-dc21f39d-3d3b-432d-9e23-91085ed8d2dd.png)

### Summary
* How many roles will need to be filled as the "silver tsunami" begins to make an impact?

72,458 employees are expected to retire in the "silver tsunami." An additional query of the employees table helps put that number into context:

![image](https://user-images.githubusercontent.com/107162310/180655030-4bd4e8b0-3f23-4ebb-8e36-a956da3f7e23.png)

The company currently employs 300,024 people, so nearly 1/4 of its staff are expected to exit.

* Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

There are not nearly enough qualified, retirement-ready employees ready to mentor. Without loosening the requirements to become a mentor, each mentor would have to oversee approximately 46 mentees (assuming every retirement is replaced on a 1:1 ratio).

From this analysis, we know how many employees are expected to retire, their current job titles, and the number of possible mentors ready to help train their replacements. For more context, an additional query can be run to discover which departments might be most impacted by the "silver tsunami". First to establish a new table with the employee numbers, department numbers, and department names of all the expected retirees:

![image](https://user-images.githubusercontent.com/107162310/180660202-00d05103-e907-420f-9236-af5140a8bab4.png)

And then, I selected a count on the employee numbers grouped by department name, and ordered in descending order:

![image](https://user-images.githubusercontent.com/107162310/180660218-46e236ae-230e-4580-8f99-1d143d294c6a.png)

From this table, we know that the Development and Production departments will lose the most employees to the "silver tsunami," and by wide margins. In turn, the company may want to prioritize the hiring and/or mentoring for these departments.

