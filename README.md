# Hedwig-Overloaded 🦉
**A lightweight, privacy-focused grade sharing web app hosted on GitHub Pages.**

---

## 🌐 Hosting Platform
This project is hosted on **GitHub Pages** for ease of deployment and access.

---

## 📊 Data Input

### 🔹 CSV File
- Format: `course_name.csv`
- Source: Google Sheets (public or protected link stored in an environment variable)
- Role: Stores the actual student grades

### 🔹 Markdown Breakdown
- Path: `./BREAKDOWN/course_name.md`
- Purpose: Specifies the column breakdown and grading structure for a course
- Format: Hierarchical list matching CSV column names

#### 📝 Example Structure:
```markdown
Serial
Student Id
Name
Email
Passkey
Marks
  - Attendance - 5
  - Quiz[T] - 10
    - Q1 - 10
    - Q2 - 10
    - Q3 - 10
    - Q4 - 10
    - Q5 - 10
    - Q6 - 10
  - Assignment[T] - 15
    - A1 - 15
    - A2 - 15
    - A3 - 15
    - A4 - 15
    - A5 - 15
    - A6 - 15
  - Mid - 20
    - MID_CO1 - ?
    - MID_CO2 - ?
    - MID_CO3 - ?
  - Final - 30
    - FINAL_CO1 - ?
    - FINAL_CO2 - ?
    - FINAL_CO3 - ?
  - Lab - 20
  - Total - 100
  - Grade
```
⸻

🔐 Student Workflow
	1.	Student navigates to the login page.
	2.	Selects a course from a dropdown or list.
	3.	Enters their:
	•	Student ID
	•	Passkey
	4.	If validated, the dashboard shows:
	•	Student ID
	•	Name
	•	Email
	•	Passkey
	•	Grades, structured in collapsible hierarchies.


🖥️ UI Requirements
	•	Modern, minimalist, and responsive design.
	•	Collapsible grade hierarchy:
	•	For example: Clicking Quiz[T] - 10 reveals Q1 through Q6 marks.
	•	Clearly delineated sections:
	•	Identity Info (top)
	•	Grade Breakdown (below)

📚 Example UI Hierarchy:

Marks
├── Attendance - 5
├── Quiz[T] - 10
│   ├── Q1 - 10
│   ├── Q2 - 10
│   └── ...
├── Assignment[T] - 15
│   └── A1 to A6
├── Mid - 20
│   ├── MID_CO1
│   └── ...
├── Final - 30
│   └── FINAL_CO1 to CO3
├── Lab - 20
├── Total - 100
└── Grade



🧩 Tech Stack Suggestions (optional)
	•	Frontend: React/Vue with collapsible UI components
	•	Backend/Parsing: Python-flask-based CSV + Markdown parser (static site generation)
	•	Deployment: GitHub Actions for automated push-to-Pages on commit
