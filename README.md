# HR Management Backend API

A robust backend API built with **FastAPI** and **MongoDB** to manage employee attendance, regularizations, and advanced analytics. 

This project was built to demonstrate backend development best practices, including handling race conditions, managing complex database aggregations, and ensuring data integrity.

## Features
* **Employee Management:** Create and list employee records.
* **Attendance System:** Punch-in/punch-out functionality with strict timezone handling (UTC to IST conversions).
* **Automated Calculations:** Automatically computes total working hours, overtime (applying a 30-minute minimum rule), and late minutes based on shift timings.
* **Attendance Regularization:** Allows HR to manually update/correct missing or incorrect attendance logs.
* **Advanced Analytics:** 
  * Monthly summaries for individual employees.
  * Department-wise monthly rollups.
  * Late Leaderboards using standard competition ranking.
  * 7-day moving average department trends (handling missing days dynamically).

## Tech Stack
* **Framework:** Python / FastAPI
* **Database:** MongoDB (using `pymongo`)
* **Deployment:** Uvicorn

## Key Technical Decisions
Details regarding database indexing, race condition handling, handling edge cases like overnight shifts, and pagination optimization can be found in the [`DECISIONS.md`](DECISIONS.md) file.
