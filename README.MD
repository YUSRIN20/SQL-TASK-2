# GUVI-DB-DESIGN-TASK

This repository contains SQL scripts to set up a relational database schema for managing information about mentors, batches, learners, marks, courses, and tasks.

## Table Structure

The schema consists of the following tables:

1. **mentors**: Stores mentor information.
    - Columns: `mentor_id`, `mentor_name`.

2. **batches**: Stores batch information.
    - Columns: `batch_id`, `batch_name`.

3. **learner**: Stores learner information.
    - Columns: `learner_id`, `learner_name`, `mentor_id`, `batch_id`, `course_id`, `task_id`.
    - Foreign key constraints: References `mentors`, `batches`, `course`, and `tasks` tables.

4. **course**: Stores course information.
    - Columns: `course_id`, `course_name`.

5. **tasks**: Stores task information.
    - Columns: `task_id`, `task_name`, `course_id`.
    - Foreign key constraint: References the `course` table.

6. **marks**: Stores mark information.
    - Columns: `mark_id`, `learner_id`, `marks`, `task_id`.
    - Foreign key constraint: References the `learner` table.

## Table Alteration

- Added columns to the `learner` and `marks` tables to accommodate additional information (`mark_id` and `task_id`, respectively).
- Added a foreign key constraint to the `marks` table to maintain referential integrity with the `tasks` table.

## Description Commands

- `DESC learner;`: Displays the structure of the `learner` table.
- `DESC marks;`: Displays the structure of the `marks` table.
- `DESC tasks;`: Displays the structure of the `tasks` table.

## Usage

1. Execute the provided SQL script to create the database schema.
2. Use the database to manage information about mentors, batches, learners, marks, courses, and tasks.
3. Refer to the README for additional information on each table and the schema setup.

 ------

 ## SQL-QUERY-SCREENSHOTS;
![SS-1](/SS-1.png)
  ---
![SS-1](/SS-2.png)

 ## SQL-EER-DIAGRAM-SCREENSHOT;
 ![EER-DIAGRAM](/EER-DIAGRAM.png)