# Project Submission - Phase 3

**Prison Data Analysis Project**  
**Authors**: FNU Syed Zubair Ahmed - 50560739, Apoorv Sood - 50599568, Jainam Manish Jain-50606698 , Kalash Thakur -50560545 
**Project Name**: Predicting Crime Rates and Enhancing Resource Allocation Strategies Using Prison Data  
**Professor Name**: Prof. Chen Xu  

---

## Highlights

### Data Product Overview
Our data product leverages **four advanced machine learning algorithms**—Ridge Regression, Random Forest, XGBoost Regression, and Logistic Regression—to validate four key hypotheses. Each algorithm is carefully chosen for its unique strengths: Ridge Regression reduces overfitting in linear models, Random Forest creates robust ensembles of decision trees, XGBoost handles large datasets with exceptional performance, and Logistic Regression provides reliable binary classification. The website features four interactive pages dedicated to these hypotheses, allowing users to explore predictions. Each hypothesis has its own dedicated database, and a centralized "Databases" page organizes all the results for seamless access and review.

### Secure Login and User Management
The website includes a secure **login system** for managing user profiles. Authenticated users can **add, edit, and delete profiles** as needed while ensuring that user inputs and predictions remain secure and unaltered. Each user can only access their own predictions, maintaining privacy and data isolation. This design prioritizes security and usability, creating a personalized experience for each user while safeguarding the integrity of the underlying data.

### Interactive Tableau Dashboards
To enhance understanding and visualization, **interactive Tableau dashboards** have been developed and published on the **Tableau Public server**, accessible at [this Tableau Public Profile](https://public.tableau.com/app/profile/fnu.syed.zubair.ahmed/vizzes). These dashboards provide dynamic insights into trends and patterns in the data. Advanced features like filters, calculated fields, and parameter controls enable users to customize their exploration and drill into specific metrics. Together, the website’s machine learning capabilities and Tableau dashboards create a comprehensive solution for predictive analysis, user engagement, and data-driven decision-making.


## Team Members and Questions 

| Team Member           | Question                                                                                                     | Code Location                       | Report Location                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------|-------------------------------------|
| Jainam Manish Jain     | Rates of Escape and Mental Illness vs. Educational Infrastructure: Identify relationships between inmate education programs and outcomes. | `predictions/views.py` - line 149 function-predict_view_2 | page 2|
|  FNU Syed Zubair Ahmed         | Proportion of Undertrial vs. Convicted Inmates Across States and Crimes: Analyze judicial inefficiencies.    | `predictions/views.py` - line 197 function-predict_view_3 | page 5 |
| Kalash Thakur | Predicting Prison Budget Allocations: Explore historical overcapacity and expenditure data for insights.    | `predictions/views.py` - line 245 function-predict_view_4 | page 7  |
| Apoorv Sood            | Demographic Analysis of Inmate Populations: Classify inmates as undertrial or convicted by demographics.     | `predictions/views.py` - line 102 function-predict_view_1 | page 9 |

---

## Project Structure
- **README.md**: Contains project details, team member contributions, and folder structure.
- **app/**: contains django code for project.
- **exp/**: python notebook code for ML models being used.
- **requirements.txt**: Python dependencies for the project.

### Directory Structure
```plaintext
.
├── Prison_Analysis/
│   ├── manage.py
│   ├── requirements.txt
│   ├── README.md
│   ├── directory_structure.txt
│   ├── Prison_Analysis/  # Django project settings
│   │   ├── __init__.py
│   │   ├── asgi.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── wsgi.py
│   ├── predictions/  # Main app logic
│   │   ├── migrations/
│   │   ├── templates/
│   │   ├── static/
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   ├── forms.py
│   │   ├── admin.py
│   ├── static/
│   │   ├── images/
│   │   ├── css/
│   │   ├── js/
├── exp/  # Experimental files and notebooks
│   ├── Dataset/
│   ├── [Other data files]
├── requirements.txt
└── Prison_Analysis_Report.pdf

```

## Instructions to Build the App

Follow the steps below to set up and run the application locally with Django and ensure scikit-learn version 1.5.1 is installed.Make sure you have python 3.12

1. **Clone the Repository**:
   - Clone the project repository from GitHub:
     ```bash
     git clone https://github.com/apoorvso/Prison_Analysis.git
     ```
   - Navigate into the project directory:
     ```bash
     cd your-repo
     ```

2. **Create a Virtual Environment (Recommended)**:
   It's best to use a virtual environment to manage dependencies. Run the following commands:
   - For Windows:
     ```bash
     python -m venv venv
     .\venv\Scripts\activate
     ```
   - For macOS/Linux:
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```

3. **Install Required Dependencies**:
   - Install the required Python dependencies listed in `requirements.txt`:
     ```bash
     pip install -r requirements.txt
     ```

4. **Ensure scikit-learn version 1.5.1**:
   - Check the currently installed version of scikit-learn:
     ```bash
     pip show scikit-learn
     ```
   - If the installed version is not 1.5.1, you can install the correct version using:
     ```bash
     pip install scikit-learn==1.5.1
     ```

5. **Run Database Migrations**:
   - Apply the database migrations to set up the database schema:
     ```bash
     python manage.py migrate
     ```

6. **Start the Django Development Server**:
   - Run the Django development server:
     ```bash
     python manage.py runserver
     ```
   - The application will be available at `http://127.0.0.1:8000/` in your browser.

7. **Access the Application**:
   - Open your browser and go to `http://127.0.0.1:8000/` to access the application locally.

---
