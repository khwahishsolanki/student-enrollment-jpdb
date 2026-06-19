# Student Enrollment Form — JsonPowerDB Micro Project

## Description

This is a serverless web form built as the micro-project for the
**Introduction to JsonPowerDB – V2.0** course on Login2Xplore. It performs
full CRUD (Create, Read, Update) operations on student enrollment data,
talking directly to the **JsonPowerDB** REST API — no backend server or
database installation required.

- **Database**: `SCHOOL_DB`
- **Relation**: `STUDENT_TABLE`
- **Primary key**: Roll No
- **Fields**: Roll No, Full Name, Class, Birth Date, Address, Enrollment Date

On page load, only the Roll No field is enabled. Typing a Roll No and
moving out of the field checks the database:
- If it **doesn't exist** -> the rest of the form unlocks and the **Save**
  button becomes active, to enroll a new student.
- If it **already exists** -> the student's data is loaded into the form,
  the Roll No field locks, and the **Update** button becomes active, so
  the details can be edited.

A **Reset** button clears the form back to its initial state, and a table
below the form lists every enrolled student, pulled live from the database.

## Benefits of using JsonPowerDB

- **Truly serverless** - the entire project is a single HTML file with no
  backend code, no server setup, and no database installation. All data
  operations happen through direct REST API calls.
- **Schema-free & instant** - there's no need to design and migrate a
  database schema before storing data; relations are created on the fly.
- **Simple REST commands** - operations like insert, lookup, update, and
  list-all map to a handful of clear commands (PUT, GET_BY_KEY, UPDATE,
  GET_ALL), which makes the client-side code easy to read and maintain.
- **Fast to prototype with** - since there's no backend layer to build,
  a working data-driven form like this one can go from idea to a working
  demo very quickly, which is ideal for small projects, hackathons, and
  learning exercises.
- **Real-time** - changes made through one client (this form) are
  immediately visible to any other client querying the same database.

## Release History

- **v1.0** (June 2026) - Initial release: Student Enrollment Form with
  Save / Update / Reset functionality and a live student list, built using
  the JsonPowerDB REST API as taught in the Introduction to JsonPowerDB -
  V2.0 course.

## Tech Stack

- HTML, CSS, JavaScript (jQuery)
- JsonPowerDB REST API (jpdb-commons.js)

## How to run

1. Open index.html in a browser.
2. Enter a Roll No to look up or create a student record.
3. Fill in the remaining fields and click Save (new student) or
   Update (existing student).

## Source

- JsonPowerDB API Docs: http://login2explore.com/jpdb/docs.html
- Course: Introduction to JsonPowerDB - V2.0, Login2Xplore
