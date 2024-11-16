
# **🌐 Job Portal App Backend**

### **Project Overview**

The **Job Portal App Backend** is designed as the core of a robust job portal platform, catering to both job seekers and recruiters with secure, scalable functionalities.

- **For Users:**
  - Register, manage profiles, and apply for job postings.
- **For Recruiters:**
  - Register companies, post jobs, and manage applications.

---

## **🛠️ Technology Stack**

- **Node.js** ![#00FF00](https://via.placeholder.com/10/00FF00?text=+) `JavaScript runtime environment powering backend execution.`
- **Express.js** ![#FFA500](https://via.placeholder.com/10/FFA500?text=+) `Web framework for Node.js applications.`
- **MongoDB** ![#00C851](https://via.placeholder.com/10/00C851?text=+) `Flexible NoSQL database for data management.`

---

## **✨ Key Features**

- **User Authentication and Authorization**
  - Secure registration, login, and password reset functionalities for users and recruiters.
  - Role-based access control to ensure secure operations for each user role.
- **Company Management**
  - Recruiters can register, update, and delete company profiles.
- **Job Management**
  - Create, update, delete, and search job postings with title, description, requirements, salary, and location.
- **Job Application**
  - Users can apply to jobs and track applications, while recruiters manage applications.
- **User Profiles**
  - Users can create and manage profiles, including resumes and work experience.

---

## **🌐 API Endpoints**

### **🔐 User Authentication** ![#4169E1](https://via.placeholder.com/10/4169E1?text=+)

* `/api/v1/user/register` - Register a new user(role can choose while registration).
* `/api/v1/user/login` - Log in an existing user.
* `/api/v1/user/profile/update` - Update the Users database


### **🏢 Company Management** ![#FFD700](https://via.placeholder.com/10/FFD700?text=+)

* `/api/vi/company/register` - Create a new company.
* `/api/vi/company/get/:id` - Find Company information by Id
* `/api/vi/company/update/:id` - Update comapany details by id.

### **📄 Job Management** ![#FFD700](https://via.placeholder.com/10/FFD700?text=+)

* `/api/v1/job/post` - Create a new job posting.
* `/api/jobs/update/:jobId` - Update an existing job posting.

* `/api/v1/job/get` - Search for jobs
* `/api/v1/job/get/:id` - Search for jobs by id

### **📩 Job Application** ![#FF00FF](https://via.placeholder.com/10/FF00FF?text=+)

* `/api/v1/application/apply/:id` - Apply to a job.
* `/api/v1/application/get` - Get all applied jobs
* `/api/v1/application/status/:id/update` - Application status


## **🗄️ Database Structure**

### **Users** ![#BA55D3](https://via.placeholder.com/10/BA55D3?text=+)
- `_id` (ObjectId) - Unique identifier for the user.
- `email` (String) - User’s email address.
- `password` (String) - Hashed password for security.
- `role` (String) - Role assigned (e.g., "user" or "recruiter").
- `resume` (String) - URL to the user's resume.
- `workExperience` (Array) - List of past work experience.

### **Companies** ![#BA55D3](https://via.placeholder.com/10/BA55D3?text=+)
- `_id` (ObjectId) - Unique identifier for the company.
- `name` (String) - Company name.
- `description` (String) - Brief overview of the company.
- `location` (String) - Company location.
- `createdBy` (ObjectId) - Reference to the recruiter who created the profile.

### **Jobs** ![#BA55D3](https://via.placeholder.com/10/BA55D3?text=+)
- `_id` (ObjectId) - Unique identifier for the job.
- `title` (String) - Job title.
- `description` (String) - Job description.
- `requirements` (Array) - Required skills and experience.
- `salary` (Number) - Salary offered.
- `location` (String) - Job location.
- `postedBy` (ObjectId) - ID of the recruiter posting the job.
- `applicants` (Array) - List of user IDs who applied.

---

