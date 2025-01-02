# Job Board Project

The **Job Board Project** is a web application designed to facilitate job postings and applications. Employers can post job openings, and job seekers can search for and apply to jobs. The project consists of a backend built with **Node.js** and **Express**, and a frontend built with **React**.

## Features

- **User Authentication and Authorization**
  - Register as Employer or Job Seeker
  - Login and logout functionality
- **Job Management**
  - Employers can post, update, and delete job listings
  - Job seekers can view and search for job listings
- **Application Management**
  - Employers can view applications for their job postings
  - Job seekers can apply to jobs and view their applications
- **Responsive Design**
  - User-friendly interface for seamless experience on all devices

---

## Tech Stack

### Backend

- **Node.js**
- **Express**
- **MongoDB**
- **Mongoose**
- **JWT** for authentication
- **bcrypt** for password hashing

### Frontend

- **React**
- **React Router**
- **Axios** for API calls
- **Bootstrap** for styling

---

## Installation

### Backend Setup

1. Clone the repository and navigate to the backend directory:

    ```bash
    git clone https://github.com/yourusername/job-board.git
    cd job-board/backend/
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Create a `.env` file in the `backend/config` directory with the following content:

    ```env
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_jwt_secret
    ```

4. Start the backend server:

    ```bash
    npm start
    ```

### Frontend Setup

1. Navigate to the frontend directory:

    ```bash
    cd ../frontend/
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Start the frontend development server:

    ```bash
    npm run dev
    ```

4. Open your browser and navigate to:

    ```
    http://localhost:5173/
    ```

---

## Usage

1. Register a new account as either an Employer or a Job Seeker.
2. Login with your credentials.
3. Employers can post new job listings and manage existing ones.
4. Job seekers can search for job listings and apply to them.

---

## API Endpoints

### User Routes

- `POST /api/v1/user/register` - Register a new user
- `POST /api/v1/user/login` - Login a user
- `GET /api/v1/user/logout` - Logout a user
- `GET /api/v1/user/getUser` - Get user details

### Job Routes

- `GET /api/v1/job/getAllJobs` - Get all jobs
- `GET /api/v1/job/myJobs` - Get jobs posted by the logged-in employer
- `GET /api/v1/job/:id` - Get a single job by ID
- `POST /api/v1/job/postJob` - Post a new job
- `PUT /api/v1/job/updateJob/:id` - Update a job
- `DELETE /api/v1/job/deleteJob/:id` - Delete a job

### Application Routes

- `POST /api/v1/app/postApp` - Apply to a job (Job Seeker only)
- `GET /api/v1/application/employerGetAllApps` - Get applications for the jobs posted by the user (Employer only)
- `GET /api/v1/application/jobSeekerGetAllApps` - Get applications for the jobs applied by the user (Job Seeker only)
- `DELETE /api/v1/application/job/jobSeekerDeleteApp/:id` - Delete an application (Job Seeker only)

---

## Frontend Routes

- `/` - Home page
- `/login` - Login page
- `/register` - Register page
- `/job/getAllJobs` - View all job listings
- `/job/post` - Post a new job (Employers only)
- `/job/me` - View jobs posted by the logged-in employer
- `/job/:id` - View details of a specific job
- `/application/me` - View applications made by the logged-in job seeker
- `/application/:id` - Apply for a job with the given ID

---
