# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - SANJAI L

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:
![image](https://github.com/user-attachments/assets/69649e94-ca2b-4355-8443-7c9125d0482f)


## Entities and Attributes:

Student: Register Number, Name, Date of Birth, Email, Mobile Number, Department ID

Course: Course Number, Course Name, Number of Credits, Department ID, Faculty ID, Prerequisite Course Number

Faculty: Staff ID, Name, Email, Mobile Number

Department: Department ID, Department Name

Enrollment: Register Number, Course Number


## Relationships and Constraints:
Belongs_To (Cardinality, Participation)
Enrolled_In (Cardinality, Participation)
Offered_By (Cardinality, Participation)
Handled_By (Cardinality, Participation)
Has_Prerequisite (Cardinality, Participation)



## Extension (Prerequisite / Billing):
In the ER diagram, prerequisites are modeled using a recursive relationship on the Course entity. This means that a course can reference another course as its prerequisite, creating a self-relationship. Each course has an optional attribute called Prerequisite Course Number, which points to the Course Number of another course that must be completed beforehand. This setup allows the system to track course dependencies and ensure that students enroll in courses in the correct sequence. The relationship is typically many-to-one, as multiple courses can share the same prerequisite, but each course has at most one prerequisite.


## Design Choices:
The entities—**Student**, **Course**, **Faculty**, and **Department**—were chosen because they represent the core components of a university system. Each plays a distinct role: students enroll in courses, courses are offered and handled by faculty, and departments organize both students and courses. The **Enrollment** relationship was necessary to handle the many-to-many interaction between students and courses. The **Prerequisite** relationship was modeled recursively within the Course entity to reflect real-world academic requirements. Assumptions made include that each student belongs to only one department, each course is handled by one faculty member, and not all courses require prerequisites, allowing for optional relationships. These choices aim to reflect typical university structures while keeping the model clear and normalized.


## RESULT
Thus the ER diagram for the university database is successfully developed.
