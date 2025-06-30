
# 📊 Global AI Careers: Trends, Salaries & Insights

## 🚀 Project Overview

This Power BI dashboard project provides a comprehensive analysis of the global AI job market, focusing on job roles, salary distribution, remote work trends, and regional hiring patterns. The dashboard is designed to help job seekers, recruiters, and data enthusiasts understand the current landscape of artificial intelligence careers using real-world job posting data.

## 🎯 Objectives

- Visualize the distribution of AI job titles by count and average salary.
- Analyze the shift toward remote and hybrid work in the AI industry.
- Understand how salary correlates with experience and education levels.
- Identify top countries and regions hiring for AI roles.
- Track job posting activity over time to discover seasonal patterns.

## 🧰 Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| **Oracle SQL Developer** | Data querying, transformation, and filtering |
| **Power BI Desktop** | Dashboard creation, visualization, and interactivity |
| **DAX** | Calculated columns and custom measures |
| **Excel/CSV** | Initial dataset formatting (if needed) |

## 🗂 Dataset Information

- **Source**: AI job postings dataset (15,000+ records)
- **Columns used**:
  - `job_title`
  - `salary_usd`
  - `experience_level`
  - `company_location`
  - `remote_ratio`
  - `employment_type`
  - `education_required`
  - `posting_date`

- **Derived Columns**:
  - `RemoteType`: Categorizes remote_ratio into Remote, Hybrid, and On-site
  - Quarter (from posting_date)
  - Avg Salary Buckets (used for chart scaling)

## 📈 Key Visuals in the Dashboard

| Visual | Description |
|--------|-------------|
| **KPI Cards** | Summary of total jobs, average salary, and average experience |
| **Donut Chart** | Distribution of RemoteType (Remote, Hybrid, On-site) |
| **Bar Chart** | Top 10 AI job titles by frequency |
| **Map Visual** | Count of AI jobs by company location |
| **Bar Chart** | Average salary by experience level |
| **Line Chart** | Job postings by quarter |
| **Slicers** | Filters for experience level, location, job title, and RemoteType |

## 🧠 Key Insights

- 🔹 **Remote Work**: Over **33%** of roles are fully remote, showing flexibility in the AI industry.
- 🔹 **Top Roles**: The most common job titles include *AI Engineer*, *AI Consultant*, and *ML Engineer*.
- 🔹 **Salary Trends**: Average salary for senior-level roles exceeds **$190K**, while entry-level is around **$63K**.
- 🔹 **Top Hiring Regions**: USA, India, Canada, and Germany dominate AI hiring activity.
- 🔹 **Seasonality**: Q1 shows the highest number of job postings, with a decline toward Q4.

## 📊 Slicers & Interactivity

- **Job Title**: Focus on specific AI roles
- **Company Location**: Filter by country
- **Experience Level**: EN (Entry), MI (Mid), SE (Senior), EX (Executive)
- **RemoteType**: On-site, Hybrid, Remote

Each slicer updates all visuals dynamically for customized exploration.

## 🛠 Custom DAX Measure Example

### RemoteType Column:
```dax
RemoteType = 
SWITCH(
    TRUE(),
    'AI_JOBS'[remote_ratio] = 100, "Remote",
    'AI_JOBS'[remote_ratio] = 50, "Hybrid",
    'AI_JOBS'[remote_ratio] = 0, "On-site",
    "Other"
)
```

## 💡 Learning Outcomes

- Practiced SQL querying on structured job data using Oracle SQL Developer.
- Built professional Power BI dashboards with DAX-based interactivity.
- Enhanced storytelling through data visualization and UX design.
- Learned how to design filters, KPI cards, and make dashboards insight-driven.

## 📁 File Structure (for GitHub)

```
📦 AI-Job-Market-Dashboard/
├── 📊 Global AI Careers.pbix
├── 📈 dashboard_screenshot.png
├── 📝 README.md
└── 📄 ai_job_dataset.csv
```

## 📌 Future Improvements

- Add job trend forecasting using Power BI forecasting tools.
- Integrate live API/job board to keep data dynamic.
- Segment roles by industry or domain (e.g., healthcare, finance, etc.).
- Add gender diversity or company type if data allows.

## 🙌 Acknowledgements

Thanks to the open data contributors and the Power BI community for templates and optimization tips.
