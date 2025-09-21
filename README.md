# Cloud Enabled Deployment – Course, Student & Media Management

This repository demonstrates a **microservices-based architecture** with Spring Boot backend services and a React frontend. It is designed for **cloud deployment (AWS/GCP)** and supports multiple data sources.


Architecture Diagram

```mermaid
flowchart LR
    User["User Browser"] --> Frontend["React + Vite App"]

    Frontend --> CourseService["Course Service (Spring Boot + MySQL on GCP/AWS)"]
    Frontend --> StudentService["Student Service (Spring Boot + MongoDB)"]
    Frontend --> MediaService["Media Service (Spring Boot + Local)"]
    
    CourseService --> MySQL["Cloud SQL / RDS"]
    StudentService --> MongoDB["MongoDB Database"]
    MediaService --> Storage["Local Disk"]
```

## Student Details
- Name               - I.Likshan Lahiru Lolitha Perera
- Registration Number- 2301671025
- Email Address      - lahiru212001@gmail.com
- Contact            - +94774703170


## Projects

### 1. course-service
- **Tech:** Spring Boot + MySQL (GCP Cloud SQL / AWS RDS)
- **Entity:** `Course(id, name, duration)`
- **Endpoints:**
  - `GET /courses` – List all courses
  - `GET /courses/{id}` – Fetch course by ID
  - `POST /courses` – Create new course
  - `DELETE /courses/{id}` – Delete course
- **Default Port:** `8081`

### 2. student-service
- **Tech:** Spring Boot + MongoDB
- **Document:** `Student(registrationNumber, fullName, address, contact, email)`
- **Endpoints:**
  - `GET /students` – List all students
  - `GET /students/{id}` – Fetch student by ID
  - `POST /students` – Add new student
  - `DELETE /students/{id}` – Delete student
- **Default Port:** `8082`

### 3. media-service
- **Tech:** Spring Boot + Local
- **Resource:** Files (upload & retrieval)
- **Endpoints:**
  - `POST /files` – Upload file (multipart/form-data)
  - `GET /files` – List all files
  - `GET /files/{id}` – Download file
  - `DELETE /files/{id}` – Delete file
- **Default Port:** `8083`
- **Storage:** Local path `./data/media` (override with `MEDIA_STORAGE_DIR`)

### 4. frontend-app
- **Tech:** React + TypeScript + MUI + Vite + Axios
- **Features:**
  - Courses management
  - Students management
  - Media management
- **Scripts:**
  - `npm run dev` – Start dev server
  - `npm run build` – Build app
  - `npm run preview` – Preview build

---

## Build & Run

## Build

- Backend: run `mvn -q -e -DskipTests package` at repo root to build services.
- Frontend: run `npm install` then `npm run dev` inside `frontend-app`.

## Run
- cd frontend-app
- npm install
- npm run dev

---

## Video Link
- click the image below to watch the demonstration video: 👇
- [![Watch the video](https://i.ibb.co/WXKQKjS/Untitled-design.jpg)](https://drive.google.com/file/d/1h1XydRXeEfesJzU_7Omp1qTrkAVN32ro/view?usp=sharing)


## License

MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE  
SOFTWARE.  


