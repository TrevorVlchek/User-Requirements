# **User-Requirements Document for Volunteer Management System**
 **Version 1.3 approved**
**Prepared by Trevor Vlchek**
**Thompson Rivers University**
**9/25/2022**

---
**Table of Contents**
| Content |
| ------------- |
| [1.   User Classes] (#U_C) |
| [2.   Actors] (#A) |
| [3.   Main Use Cases] (#M_U_C) |
| 3.1.   Use Case List |
| 3.2.   Use Case Diagram |
| 3.3.   Use Case: Create New Volunteer |
| 3.4.   Use Case: Approve new Volunteer |
| 3.5    Use Case: Generate Daily Report |

**Revision History**


|**Name**|**Date**|**Reason For Changes**|**Version**|
| -----: | -----: | -------------------: | --------: |
|Trevor Vlchek|9/25/2022|Filled in user requirement document|1.3|


<h2 id="U_C">1. User Classes</h2>

| User | User Class | Description |
| ---: | ---------: | ----------: |
| Volunteer | Direct, Favored | These persons will have passed their background check and be available for volunteer services. They will enter their available hours into the VMS for the administrators to view and assign to a senior. Once they have completed the assigned task, they will enter into the VMS a short description of the duties performed and the outcome. |
| Administrators | Direct, Favored | Administrators will use the system to review available volunteers and seniors needing assistance. They will be able to assign available volunteers to upcoming cases and review the outcomes of completed volunteer duties. |
| Seniors | Direct, Favored | Once registered with the city, seniors will be able to submit requests for assistance directly to the VMS or have their request entered through an administrator. |
| Mayoral Office | Direct, Favored | The mayoral office will be able to access all the features of the administrators and see some data logging as well. |
| Business Owners | Indirect, Favored | Business owners will not interact with the system directly but will benefit from its success in the form of increased activity in the downtown area |
| Background Check Administrators| Indirect, Ignored | Background check administrators will need to submit background check pass/fail results to the VMS |
| Volunteers who do not pass background check | Disfavored, Direct | These individuals are not currently a part of the group being serviced by the VMS. Currently the system is only providing help to seniors, not anyone who wants help around the house |
| Students | Disfavored Indirect | In future, the VMS may be expanded to help provide students with additional tutoring services. In this case, the students requiring help would be matched with qualified tutors |

<h2 id="A">2. Actors</h2>

**SPCC Employee:** An employee at senior people care center who will be in charge of helping create profiles for senior people.

**Senior peer:** A volunteer who is tasked with phoning senior people to give social support, reminders, and check up on their mental status. They also report any health issues to the system.

**Student peer:** A subset of volunteers who are matched with a student

**SPCC Employee:** Employee working at the SPCC who is tasked with creating a profile for the VMS from phone conversations.

**Volunteer:** A philanthropic person who wants to help students or the elderly through donating their time

**Administrator:** A person who is in charge of submitting volunteer profiles for background checks and verifying the validity of educational certificates.

**School Administrator:** A school employee who requests volunteers to teach students

**Background Check System:**  A government system to perform background checks on volunteers using police officer

**Mayors Office:** The people who will be evaluating the forecasts and volunteers data

**Senior:**  An old person in need of volunteer help for reminders, loneliness, and other age related issues.

<h2 id="M_U_C">3. Main Use Cases</h2>

## **3.1 Use Case List**

| Use Case | Description | Actors|
| -------: | ----------: | ----: |
| Create a senior profile| The senior person phones spcc employee to create a profile so the senior can get volunteer help | Primary: SPCC employee, Secondary: Senior |
| Edit senior profile | The senior person phones spcc employee to edit their information | Primary: SPCC employee, Secondary: Senior |
| Recommend volunteer opportunity | The system evaluates the volunteers profile and recommends potential volunteer opportunities | Primary: Volunteer Secondary: Student-peer, and senior-peer |
| Create volunteer profile | A potential volunteer enters their information to create a profile into the system | Primary: Volunteer Secondary: Administrator |
| Edit volunteer profile | The volunteer changes their details or cancels their eligibility as a volunteer | Primary: Volunteer, Student-peer, senior-peer |
| Record senior people data | The senior peer records information about the senior person to monitor their health | Primary: Senior-peer |
| Edit senior people data | The senior peer edits the senior person data | Primary: Senior-peer |
| Report forecast | The data on the supply and demand for the next week with respect to volunteers | Primary: Mayor's office Secondary: Administrator |
| Track volunteer engagement | The volunteer data regarding how many people are signing up, quitting. | Primary:Administrator Secondary: Volunteer, student-peer, and senior-peer |
| Report volunteer issues | When a volunteer is acting poorly the system warns the administrator | Primary: Administrator Secondary: Volunteer |
| Approve new volunteer | The volunteer must get a background check and if they are dealing with students their teaching certificate must be reviewed | Primary:Administrator, and BCS |
| Request volunteer | When students need help with their studies the school administrator submits a request to get a student peer | Primary: School administrator Secondary: Student-peer |

## **3.2 Use Case Diagram**


## **3.3 Use Case: Create New Volunteer**

| use-case field | Description |
| -------------: | ----------: | 
| **Use case name** | UC1: Create New Volunteer |
| **Scope** | Volunteer Management System (VMS) |
| **Level** | Adds a new volunteer to the registry andservice more seniors |
| **Actors** | Volunteers, Administrators |
| **Stackeholders and interests** | Volunteers, Administrators, Seniors |
| Preconditions** | Volunteers must have passed the background check |
| **Termination Outcome** | Successful outcome: Volunteer is added to the registry and can then be assigned to seniors, Seniors receive help. Unsuccessful Outcome: Volunteer did not have any available hours that coincided with when seniors want assistance |
| **Condition affecting termination outcomne** | The volunteer must have hours available for volunteering that are within the time frames seniors want help |
| **use case description** | Volunteers will receive word that they have passed the background check and can register. They will then enter their personal information. |
| **Use case associations** | Assigning a volunteer to a senior, Recording a successful volunteer event |
| Special requirements** | Volunteers must be willing to sign up, there must be interest in the program and the background check system must be functioning |
| **Technology and Data Variation List** | Name, Date of Birth, Phone number, email. | 
| **Frequency of Occurrence** | With roughly 10-15k cases per year needing assistance, and volunteers being unlikely to be able to help with more than 3 cases a week. |

## **3.4 Use Case: Approve New Volunteer**

| Use Case | Comment |
| -------: | ------: |
| Name | UC2: Approve New Volunteers |
| Scope | 1.VMS 2. Background Checking System |
| Level | 1.User-Goal Level |
| Primary Actor | 1. Administrators |
| Stakeholders and Interest | 1.Administrators 2.Volunteer 3.Mayor 4.Ministry of Health 5.Patients |
| Preconditions | 1.Administrators initial screening is approved 2. Administrators successfully submit profiles for background check 2.Background checking system identifies volunteer |
| Success Guarantee | 1.Volunteers are verified | 
| Main Success Scenario | 1.Volunteer submits profile 2. Administrators receive profile and verify it for screening 3.Administrators verify educational certificate if they will be tutoring 4. Administrators send volunteer profile for background check 5.Volunteers background check is approved and is sent back to VMS |
| Extensions | 1.Volunteers profile submissions fails a)VMS denies profile and sends error message and code 2.Volunteer tries to submit profile when he already has a existing profile a) Display error message “User already has a existing profile” b) ask the user if the want to update their profile or overwrite it 3.Volunteer wants to update profile |
| Special Requirements | 1.Picture of user on profile so it's easier to verify the identity of user |
| Technology and Data Variations List | 1.VMS recognizes volunteers ID |
| Frequency of Occurrence | 1.While the BCS should be able to handle 1k profiles per hour there is an manual step that will slow the time down 2. Also the manual step can only be performed during working hours |

## **3.5 Use Case: generate Daily Report**

| Use Case | Comment |
| -------: | ------: |
| Name | UC3: Generate Daily Reports | 
| Scope | 1.VMS |
| Level | 1.User-Goal Level |
| primary Actor | 1.Administrators |
| Stakeholders and Interest | 1.Administrators 2.Volunteer 3.Mayor 4.Government 5.Patients |
| Preconditions | 1.Volunteers are approved 2.Patients request for volunteer need is received 3.Request from school administrators who need tutors |
| Success Guarantee | 1.Report of patients in need 2.Report of tutors in need 3.Forecast of patients for next week |
| Main Success Scenario | 1. Patients send request to VMS for volunteer service 2.VMS records request 3.VMS determines the priority of the case 4.VMS shows forecast of patients and schools in need |
| Extensions | 1.Show higher priority patients 2.The ability to manage volunteers so that they can be resigned to higher priority cases 3.Tutors and regular volunteers should be distinguished 4.Tutors should be prioritized to schools |
| Special Requirements | 1.Patients should easily be able to request volunteers either digitally(SPCC) or through a worker |
| Technology and Data Variations List | 1.VMS recognizes volunteers ID 2.Forecast of reports should be easy to ready and simple |
| Frequency of Occurrence | 1.Most requests from patients should be consistent however the request for tutors will likely be greater during the school year with a decline in the summer. |















