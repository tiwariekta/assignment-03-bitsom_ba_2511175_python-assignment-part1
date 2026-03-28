# 📊 Student Grade Tracker — Part 1 (Python Basics & Control Flow)

## 📌 Overview

This project is part of a hands-on assignment focused on **core Python concepts** such as control flow, loops, string manipulation, and data processing.

The goal was to simulate real-world scenarios where:

* Data is messy and needs cleaning
* Logic is applied to derive insights
* Structured outputs are generated for reporting

---

## 🎯 Key Learning Outcomes

* Data cleaning and normalization
* Looping constructs (`for`, `while`)
* Conditional logic and validation
* String manipulation techniques
* Building interactive command-line workflows
* Writing readable and structured output

---

## 📂 Project Structure

```
student-grade-tracker/
│
├── part1_task1.py   # Data parsing & cleaning
├── part1_task2.py   # Marks analysis & user input system
├── part1_task3.py   # Class performance summary
├── part1_task4.py   # String manipulation utility
└── README.md
```

---

# 🧩 Task 1 — Data Parsing & Profile Cleaning

### 🔍 Problem

Raw student data contained:

* Inconsistent spacing and casing in names
* Roll numbers stored as strings
* Marks stored as comma-separated strings

### ⚙️ Solution Approach

* Cleaned names using `strip()` and `title()`
* Converted roll numbers to integers
* Parsed marks using `split()` and list comprehension
* Validated names using:

```python
all(word.isalpha() for word in name.split())
```

### 📌 Output Example

```
================================
Student : Ayesha Sharma
Roll No : 101
Marks   : [88, 72, 95, 60, 78]
✓ Valid name
================================
```

---

# 📊 Task 2 — Marks Analysis & Input System

### 🔍 Problem

Analyze subject-wise marks and build an interactive system to add new subjects.

### ⚙️ Solution Approach

#### 1. Grade Assignment

Used conditional logic:

* A+ (≥90), A (80–89), B (70–79), C (60–69), F (<60)

#### 2. Metrics Computed

* Total marks using `sum()`
* Average using `round(..., 2)`
* Highest & lowest using `max()`, `min()`, and indexing

#### 3. Interactive Input System

* Implemented `while` loop for continuous input
* Used **nested loop** to handle invalid marks without re-entering subject
* Validated:

  * Non-numeric inputs
  * Out-of-range values (0–100)

#### 4. Tracking New Entries

* Stored new subjects using a list of tuples
* Displayed newly added entries after input completion

### 💡 Key Insight

Nested loops significantly improved user experience by isolating validation logic.

---

# 🧾 Task 3 — Class Performance Summary

### 🔍 Problem

Generate a structured report for multiple students.

### ⚙️ Solution Approach

* Iterated using tuple unpacking:
  `for name, marks in class_data`
* Calculated average per student
* Assigned Pass/Fail based on threshold (≥60)

### 📊 Metrics Generated

* Pass/Fail count
* Class topper (highest average)
* Class average (mean of all averages)

### 📌 Output Example

```
Name              | Average | Status
----------------------------------------
Ayesha Sharma     |  78.60  | Pass
Rohit Verma       |  61.00  | Pass
Priya Nair        |  87.40  | Pass
Karan Mehta       |  49.00  | Fail
Sneha Pillai      |  75.60  | Pass
```

---

# ✍️ Task 4 — String Manipulation Utility

### 🔍 Problem

Process and transform a raw essay string.

### ⚙️ Operations Performed

1. Removed whitespace using `strip()`
2. Converted to Title Case using `title()`
3. Counted occurrences of `"python"`
4. Replaced `"python"` with `"Python 🐍"`
5. Split essay into sentences using `.split(". ")`
6. Printed numbered sentences with proper formatting

### 💡 Enhancement

* Ensured each sentence ends with `.`
* Applied Title Case for improved readability

---

# 🛠️ How to Run

### Run in Jupyter Notebook

> Note: `input()` prompts may appear at the top of the interface.

---

# ⚠️ Challenges Faced & Solutions

| Challenge                          | Solution                            |
| ---------------------------------- | ----------------------------------- |
| `input()` not working in Jupyter   | Ran code in `.py` file              |
| Invalid marks restarting full loop | Introduced nested loop              |
| Data inconsistency                 | Applied string cleaning and parsing |
| Output formatting alignment        | Used f-string formatting            |


# 👩‍💻 Author

**Ekta Tiwari**

---

## 🌟 Final Note

This project demonstrates how fundamental Python concepts can be applied to solve practical data problems — a key skill in data analytics, backend development, and data engineering workflows.
