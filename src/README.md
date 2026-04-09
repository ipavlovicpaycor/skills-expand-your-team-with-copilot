# Mergington High School Activities

A web application for Mergington High School that lets students and teachers manage extracurricular activities.

## Features

- **Browse Activities** – View all extracurricular activities with descriptions, schedules, and enrollment counts
- **Search & Filter** – Search by name/description, filter by category, day, time, and difficulty level
- **Dark Mode** – Toggle between light and dark themes; preference is saved automatically
- **Difficulty Tracks** – Activities are labeled Beginner, Intermediate, or Advanced
- **Group by Category** – Organize activities into Sports, Arts, Academic, Community, and Technology sections
- **Calendar View** – See all activities on a weekly calendar from Sunday to Saturday (6 AM – 8 PM)
- **Teacher Login** – Teachers log in to register or unregister students
- **Register / Unregister Students** – Authenticated teachers can manage student enrollment

## Activities

The following activities are currently available:

| Activity | Schedule | Difficulty |
|---|---|---|
| Chess Club | Mon & Fri, 3:15–4:45 PM | Beginner |
| Programming Class | Tue & Thu, 7:00–8:00 AM | Intermediate |
| Morning Fitness | Mon/Wed/Fri, 6:30–7:45 AM | — |
| Soccer Team | Tue & Thu, 3:30–5:30 PM | Beginner |
| Basketball Team | Wed & Fri, 3:15–5:00 PM | — |
| Art Club | Thu, 3:15–5:00 PM | Beginner |
| Drama Club | Mon & Wed, 3:30–5:30 PM | Intermediate |
| Math Club | Tue, 7:15–8:00 AM | Advanced |
| Debate Team | Fri, 3:30–5:30 PM | — |
| Weekend Robotics Workshop | Sat, 10:00 AM–2:00 PM | Advanced |
| Science Olympiad | Sat, 1:00–4:00 PM | — |
| Sunday Chess Tournament | Sun, 2:00–5:00 PM | Advanced |
| Manga Maniacs | Tue, 7:00–8:00 PM | — |

## Technology Stack

- **Backend:** Python / FastAPI
- **Database:** MongoDB (local instance)
- **Frontend:** Vanilla HTML, CSS, and JavaScript
- **Authentication:** Argon2 password hashing, session stored in localStorage

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/activities` | List activities (supports `day`, `start_time`, `end_time`, `difficulty` filters) |
| GET | `/activities/days` | List all days with scheduled activities |
| POST | `/activities/{name}/signup` | Register a student (teacher auth required) |
| POST | `/activities/{name}/unregister` | Unregister a student (teacher auth required) |
| POST | `/auth/login` | Teacher login |
| GET | `/auth/check-session` | Validate teacher session |
