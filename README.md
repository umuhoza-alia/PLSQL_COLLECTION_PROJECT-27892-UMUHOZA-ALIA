# PL/SQL Collections, Records & GOTO - Complete Project

## 📚 Project Overview

This repository demonstrates comprehensive implementation of **PL/SQL Collections, Records, and GOTO statements** through a practical **Student Grade Management System**.

**Course:** Database Development with PL/SQL (INSY 8311)  
**Instructor:** Eric Maniraguha  
**Institution:** Adventist University of Central Africa (AUCA)  
**Date:** November 2025

---

## 🎯 Learning Objectives

This project demonstrates mastery of:

- **Three Collection Types:**
  - Associative Arrays (Index-By Tables)
  - VARRAYs (Variable-Size Arrays)
  - Nested Tables

- **Two Record Types:**
  - User-Defined Records
  - Table-Based Records (%ROWTYPE)

- **GOTO Statements:**
  - Appropriate flow control usage
  - Label-based branching
  - Multi-stage processing

---

## 📁 Repository Structure

```
PLSQL_Collections_Project/
│
├── sql_scripts/               # All executable SQL files
│   ├── 01_create_tables.sql          # Database schema & sample data
│   ├── 02_associative_arrays.sql     # Associative array demo
│   ├── 03_varray_demo.sql            # VARRAY demo
│   ├── 04_nested_table_demo.sql      # Nested table demo
│   ├── 05_user_defined_records.sql   # User-defined records demo
│   ├── 06_table_based_records.sql    # %ROWTYPE demo
│   └── 07_comprehensive_demo.sql     # Complete integration
│
├── documentation/             # Project documentation
│   └── PLSQL_Collections_Complete_Documentation.docx
│
└── screenshots/              # Execution evidence
    └── [Output screenshots from each demo]
```

---

## 🚀 Quick Start Guide

### Prerequisites

- Oracle Database Express Edition 21c
- SQL Developer or SQL*Plus
- Basic PL/SQL knowledge

### Installation & Execution

1. **Clone or download this repository**

2. **Open SQL Developer and connect to your database**

3. **Enable output:**
   ```sql
   SET SERVEROUTPUT ON;
   ```

4. **Execute scripts in order (01 through 07)**

5. **Review output and capture screenshots**

---

## 🗃️ Database Schema

### Tables

**students**
- `student_id` (PK) - Unique identifier
- `first_name` - Student first name
- `last_name` - Student last name  
- `email` - Contact email
- `enrollment_date` - Registration date

**courses**
- `course_id` (PK) - Unique identifier
- `course_name` - Course title
- `credits` - Credit hours
- `instructor` - Faculty name

**grades**
- `grade_id` (PK) - Unique identifier
- `student_id` (FK) - References students
- `course_id` (FK) - References courses
- `score` - Percentage (0-100)
- `grade_date` - Assessment date

---

## 💡 Key Demonstrations

### 1. Associative Arrays (Script 02)
**Purpose:** Store student GPAs indexed by name  
**Key Features:**
- Dynamic key-value pairs
- Cursor-based population
- Warning system for low performers
- GOTO-controlled iteration

**Output:** GPA listing with academic status flags

---

### 2. VARRAYs (Script 03)
**Purpose:** Manage fixed-size score collections  
**Key Features:**
- Maximum capacity constraint
- Dense storage guarantee
- Integration with records
- Sequential processing

**Output:** Individual student scores with average calculation

---

### 3. Nested Tables (Script 04)
**Purpose:** Handle dynamic enrollment lists  
**Key Features:**
- Unbounded growth
- Sparse operation support (DELETE)
- EXISTS validation
- Flexible sizing

**Output:** Course enrollment with deletion demonstration

---

### 4. User-Defined Records (Script 05)
**Purpose:** Create structured academic reports  
**Key Features:**
- Custom composite types
- Multi-field aggregation
- Calculated attributes
- Complex GOTO flow

**Output:** Comprehensive student performance report

---

### 5. Table-Based Records (Script 06)
**Purpose:** Leverage database schema structure  
**Key Features:**
- %ROWTYPE syntax
- Automatic field mapping
- Schema independence
- Type safety

**Output:** Complete table row information display

---

### 6. Comprehensive Integration (Script 07)
**Purpose:** Combine all concepts into unified system  
**Key Features:**
- All three collection types
- Custom and table-based records
- Complex GOTO orchestration
- Statistical analysis

**Output:** Full class performance analysis with metrics

---

## 🔍 GOTO Statement Patterns

### Pattern 1: Sequential Processing
```
GOTO step1 → GOTO step2 → GOTO step3 → GOTO end_program
```

### Pattern 2: Conditional Branching
```
IF condition THEN GOTO branch_a ELSE GOTO branch_b
```

### Pattern 3: Loop Simulation
```
<<loop_start>>
  process_item;
  IF more_items THEN GOTO loop_start
  ELSE GOTO loop_end
```

### Pattern 4: Error Handling
```
IF error_detected THEN GOTO error_handler
ELSE GOTO normal_processing
```

---

## 📊 Sample Output

### Associative Array Demo
```
=== ASSOCIATIVE ARRAY DEMONSTRATION ===
Loading Student GPAs...
--------------------------------------
Loaded: Jean Uwizera - GPA: 85.17
Loaded: Marie Mukamana - GPA: 82.50
...
⚠ WARNING: Student needs academic support!
Total students processed: 5
```

### Comprehensive Demo
```
╔═══════════════════════════════════════════════════╗
║  COMPREHENSIVE STUDENT PERFORMANCE ANALYSIS      ║
╚═══════════════════════════════════════════════════╝

Student #1: Jean Uwizera
  Courses: 3
  Average: 85.17
  Grade: B (Very Good 80-89)

═══ CLASS STATISTICS ═══
Total Students Analyzed: 5
Honor Roll Students (A/B): 3
Honor Percentage: 60.0%
```

---

## 🧪 Testing

All demonstrations have been tested with:
- Oracle Database 21c Express Edition
- Sample dataset (5 students, 4 courses, 10 grades)
- Multiple execution scenarios
- Error condition handling

### Verification Steps:
1. Execute each script independently
2. Compare output with expected results
3. Validate calculations manually
4. Test error handling
5. Trace GOTO execution paths

---

## 📖 Documentation

Complete documentation available in:
- `documentation/PLSQL_Collections_Complete_Documentation.docx`

Includes:
- Executive Summary
- Problem Statement
- Technical Requirements
- Implementation Details
- Testing Results
- Conclusion
- Appendices with all scripts

---

## 🎓 Key Takeaways

### When to Use Each Collection Type:

**Associative Arrays:**
- Need key-value pairs
- Dynamic indexing required
- No size constraints

**VARRAYs:**
- Fixed maximum size known
- Always dense (no gaps)
- Order matters

**Nested Tables:**
- Dynamic sizing needed
- Sparse operations required
- Flexible growth

### Record Types:

**User-Defined:**
- Custom structure needed
- Mixed data types
- Calculated fields

**%ROWTYPE:**
- Match table structure
- Direct row operations
- Schema maintenance

---

## 🛠️ Troubleshooting

**Problem:** No output displayed  
**Solution:** Execute `SET SERVEROUTPUT ON;`

**Problem:** Table already exists  
**Solution:** Drop existing tables first

**Problem:** Unique constraint violated  
**Solution:** Clear existing data with TRUNCATE

**Problem:** Identifier not declared  
**Solution:** Check variable names and types

---

## 📚 References

1. AUCA Lecture Materials - Database Development with PL/SQL
2. Oracle PL/SQL Language Reference 21c
3. Oracle Learning Library - Collections and Records
4. Course Instructor: Eric Maniraguha

---

## 📝 License

This project is created for educational purposes as part of the INSY 8311 course at AUCA.

---

## 👨‍🎓 Author

**Nshuti**  
Information Technology Student  
Adventist University of Central Africa (AUCA)

---

## 🤝 Contributing

This is an academic project. For questions or suggestions:
- Contact course instructor: eric.maniraguha@auca.ac.rw
- Review during class assessment

---

## ⭐ Acknowledgments

- Eric Maniraguha for comprehensive PL/SQL instruction
- AUCA IT Department for resources and support
- Classmates for collaborative learning

---

**Project Status:** ✅ Complete and Ready for Assessment

**Last Updated:** November 2025

---

## 📧 Contact

For academic inquiries related to this project, please contact through official AUCA channels.

---

**End of README**
