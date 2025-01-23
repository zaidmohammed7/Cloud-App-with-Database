# Online Course Assessment Feature

## Project Overview

In this project, I developed a **new course assessment feature** for an online course application. The application allows instructors to create courses with exams, and learners to take exams, view their results, and review their answers. 
This project highlights full-stack development using **Django**, with a focus on back-end functionality, database modeling, and front-end integration.

---

### Key Features:
- **Course Assessment System:**
  - Instructors can create questions and choices for exams.
  - Learners can take exams and submit answers.
  - Automatic grading and result evaluation.
- **Dynamic Result Display:**
  - Shows total score and results for each question.
  - Indicates correct, incorrect, and unselected answers.
- **Custom Models:**
  - **Question Model:** Stores questions with grades and relationships to courses.
  - **Choice Model:** Stores answer choices and whether they are correct.
  - **Submission Model:** Tracks learners' exam submissions and selected answers.
- **Django Admin Integration:**
  - Instructors can manage courses, questions, and choices using the Django Admin interface.
- **Stylized Front-End:**
  - Templates stylized using **Bootstrap** for a clean and responsive user interface.

---

## Skills Demonstrated

- **Django Models:**
  - Built custom models for Questions, Choices, and Submissions.
  - Integrated Many-to-One and Many-to-Many relationships for data integrity.
- **Views and Templates:**
  - Implemented function-based views for exam submission and result display.
  - Developed dynamic templates to display exam questions, choices, and results.
- **Database Operations:**
  - Used Django ORM for database schema creation and data manipulation.
  - Ran migrations to apply model changes to the database schema.
- **Django Admin Site:**
  - Extended the Django Admin interface for managing exams and submissions.
- **Bootstrap Integration:**
  - Enhanced the front-end design with Bootstrap for responsiveness.
- **GitHub & Version Control:**
  - Managed the project through Git and GitHub for version control and peer review submission.

---

## Project Setup and Installation

### Clone the Repository
To set up this project locally, follow these steps:

1. **Clone this repository:**

    ```bash
    git clone https://github.com/zaidmohammed/Django-Course-Manager.git
    cd Django-Course-Manager
    ```

2. **Set up a Virtual Environment:**

    Create and activate a virtual environment:

    ```bash
    pip install virtualenv
    virtualenv djangoenv
    source djangoenv/bin/activate
    ```

3. **Install Required Dependencies:**

    Install the dependencies listed in the `requirements.txt` file:

    ```bash
    pip install -U -r requirements.txt
    ```

4. **Apply Migrations:**

    Run the following commands to create the database schema:

    ```bash
    python3 manage.py makemigrations
    python3 manage.py migrate
    ```

5. **Create an admin user:**

    Use the createsuperuser command to create an admin user to manage the application via the Django Admin interface:

    ```bash
    python3 manage.py createsuperuser
    ```

    You will be prompted to enter a username and password for the admin

6. **Run the Application:**

    Start the Django development server:

    ```bash
    python3 manage.py runserver
    ```

    The application will be accessible at `http://127.0.0.1:8000/`. 

   Navigate to `http://127.0.0.1:8000/onlinecourse/` to access the main course platform for students.

   Navigate to `http://127.0.0.1:8000/admin/` to manage courses, lessons, questions, and users via the Django Admin interface. 

---

## Application Features

### Instructor Features:
- Create and manage courses, lessons, and exams through the Django Admin interface.
- Add questions and multiple-choice answers for exams.

### Learner Features:
- Enroll in courses and view course details.
- Take exams, select answers, and submit them for evaluation.
- View exam results, including:
  - Total score.
  - Detailed feedback on correct, incorrect, and unselected answers.

### Exam Result Display:
- Results are dynamically displayed after submission, indicating:
  - Correct answers selected.
  - Incorrect answers selected.
  - Correct answers that were not selected.

---

## Models Overview

### Question Model:
- Links to a specific course.
- Includes question text and grade points.

### Choice Model:
- Links to a specific question.
- Stores answer text and whether it is correct.

### Submission Model:
- Links to an enrollment record.
- Tracks selected choices for an exam submission.

### ER Diagram

![Onlinecourse ER Diagram](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database/blob/master/static/media/course_images/onlinecourse_app_er.png)
---

## Testing the Application

1. **Set Up Test Data:**
   - Create a course and add lessons, questions, and choices using the Django Admin site.
   - Add learners and enroll them in the course.

2. **Take an Exam:**
   - Navigate to the course detail page and take the exam.
   - Submit answers for evaluation.

3. **View Results:**
   - See the total score and detailed feedback for each question and choice.

---

## Acknowledgements

- The course *"Django Application Development with SQL and Databases"*, offered by **IBM** through **Coursera**.
  You can find more details about the course [here](https://www.coursera.org/learn/developing-applications-with-sql-databases-and-django).
- Special thanks to the **IBM Developer Skills Network** for providing the foundational project structure and guidance.
