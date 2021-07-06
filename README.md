# DBMS-webapp
An online hospital management system
Functionalities:
Section - 1: Domain description
This is an application for managing the following information belonging to a diagnostic hospital. The plan is to build a hospital records database having the following specifications:
•	The hospital has a total of 30 attending doctors (out of which none or all may be available at any given time). The hospital does not house patients. It only diagnoses and tests them, after which it gives them their test reports.
•	Each doctor can attend to a maximum of 3 patients (provided he is in the hospital – each doctor has, associated with him/her, an in-time and an out-time).
•	Every and any doctor comes in after 8 in the morning (when the hospital opens) and leaves before 8 in the evening(when the hospital closes). As mentioned, the in-time and out-time of each doctor (where the in-time is after 8 am and the out-time is before 8 pm) is given well in advance. Doctors can change these times as per their convenience, but this change will be reflected starting from the next day.
•	Each patient can consult with one and only one doctor.
•	 Other medical personnel like nurses stay in the hospital at all times and we assume that there are a sufficient number of nurses available for any purpose at a given time. (In other words, there is no functionality associated with them. Only, their records are stored).
•	There are multiple tests that can be availed by the patients of the hospital.
•	Each hospital employee has an id (unique), name, salary/workinghr (has basic and DA components), in-time and out-time (for doctors only), role (doctor/nurse etc), id’s of patients they are attending to and a rating.
•	Each patient has an id (unique), name, mobile_number, complaint, date_of_checkup,diagnosis, doc_notes, cost_of_treatment, id_of_attending_doctor, list_of_tests_prescribed.
•	There is an additional tests table which has the name_of_test, id (unique), cost_of_test.

Section 2 : Constraints 
•	A doctor can attend to at most 3 patients at a given time.
•	The hospital does not house patients. Based on the patient complaint, a doctor at the hospital prescribes a battery of tests, views the reports, diagnoses the patient, prescribes medicine, charges the patient and sends them home.
•	Each patient can only have one attending doctor.
•	A patient record is created only when there is an available doctor at the time. Else, the patient is sent home.
•	Passwords must contain **** only.
•	Any employee cannot be older than 70 and younger than 25.
•	Names should not contain numbers/special characters.
•	The mobile numbers should have exactly 10 digits.
•	The rating of an employee is between 1.0 and 5.0

Section – 3: Functionality supported
	A GUI interface is provided to insert data into the patient, employee and tests tables. An interface for checking whether a doctor is available or not is also present (along with a feature to filter doctors by their rating ie. Patients can choose to opt for a doctor having a rating in a specific range : like 2.3-4.5). A report generation interface is provided for: 
	Generating a report having the list of tests a patient has undergone, their corresponding costs and a grand total. 
	Generating a list of all available doctors at any point of time
	Generating a report containing the total amount paid by each customer. 
	Generating a report containing an id and name of each doctor and the number of hours they worked that day along with the salary payable to them.
	Generating all employee’s data
	Generating all patient’s data
	Generating all patients’ data a given doctor has attended to.



Section – 4 : GUI Layout/ Navigation and purpose
	One GUI window for connecting the user to the application. We can connect as a new patient (which also simultaneously checks for the availability of a suitable doctor) or as an admin or as an employee. 
The GUI corresponding to newpatient facilitates the entry of patient data and his preference of doctor (a number between 1 and 5 indicating the rating of the doctor he would prefer).
The GUI corresponding to admin has a login screen to begin with and from there, the admin can access and update data corresponding to any employee and patient and generate relevant reports as mentioned above in section – 3.
The GUI corresponding to employee has a login screen to begin with and from there, an employee who is NOT A DOCTOR can access (but not modify) their records and an employee WHO IS A DOCTOR can access (but not modify) their records but can update relevant patient attributes.
