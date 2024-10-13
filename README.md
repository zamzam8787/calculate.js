## Student Information

- *Name*: Zamzam Abdullahi Abdi
- *Class ID*: C1210047
- *Class Name*: CA211

---



Calculate Total Target Function
Description
This project contains a function calculateTotalTarget that calculates the total monthly target based on the total annual target, taking into account only working days in the date range specified, excluding Fridays. The function is useful for organizations or individuals who want to distribute an annual target evenly across months, but only considering working days excluding Fridays.

Functionality
The function takes three inputs:

startDate: The start date of the period to calculate the target (in YYYY-MM-DD format).
endDate: The end date of the period to calculate the target (in YYYY-MM-DD format).
totalAnnualTarget: The total annual target to be distributed evenly across months.
The function:

Iterates through all the days within the specified date range.
Excludes Fridays from the calculation of working days.
Distributes the total annual target evenly across the 12 months.
Outputs the number of working days excluding Fridays for each month and the corresponding monthly target for the months that have working days.
Usage
Function Signature
javascript
Copy code
function calculateTotalTarget(startDate, endDate, totalAnnualTarget)
Example
javascript
Copy code
console.log(calculateTotalTarget('2024-01-01', '2024-03-31', 5220));
Output
json
Copy code
{
  "daysWorkedExcludingFridays": [
    22,
    20,
    21
  ],
  "monthlyTargets": [
    435,
    435,
    435
  ],
  "totalTarget": 5220
}
How it works
Input Parsing: The function begins by converting the input startDate and endDate into Date objects.
Date Iteration: It loops through each day in the specified date range and checks if the day is not a Friday (day 5 in JavaScript's Date.getDay() method). If it's not a Friday, the day is counted for that month.
Target Distribution: The total annual target is divided evenly across all 12 months. If a month has any working days, the target for that month is assigned.
Result: The function returns a JSON object that shows:
The number of days worked (excluding Fridays) in each month.
The monthly target for each month with working days.
The total target, which is the sum of the monthly targets.
Assumptions
The function assumes that the totalAnnualTarget is evenly distributed across all months, regardless of the number of days worked in each month.
Only working days excluding Fridays are considered.
Limitations
The function does not consider public holidays or any other non-working days apart from Fridays.
The annual target is evenly divided across the months without adjusting for the actual number of working days in each month.
Running the Code
To run the code, follow these steps:

Clone the repository from GitHub:
bash
Copy code
git clone <your-repo-url>
Navigate to the project folder:
bash
Copy code
cd project-folder
Open the file in a text editor or run it using Node.js:
bash
Copy code
node filename.js
Repository Link
Add your GitHub repository link here once you upload the project.

This README.md provides a clear description of the project, how the function works, example usage, assumptions, limitations, and instructions on how to run the code.






