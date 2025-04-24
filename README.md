
# 🎓 FixMyCampus - Campus Issue Tracker

FixMyCampus is a web-based campus issue reporting and management platform developed using **Python**, **Streamlit**, and **MySQL**. It allows students to report infrastructure problems, and admins to track and manage those issues efficiently.



---

## 🚀 Features

### 👨‍🎓 For Students
- Report issues (Electricity, Water, WiFi, etc.)
- Track issue status (Pending, In Progress, Resolved)
- View and update profile
- Change and reset password
- Dashboard with visual analytics (charts & status)
- Fully responsive and stylish UI

### 🛠 For Admins
- Admin login and dashboard
- Manage reported issues (update/delete)
- Export users/issues/banned users as CSV
- Ban or unban students
- View audit logs
- Coming soon: Notifications system

---

## 📁 Folder Structure

```
📦FixMyCampus
 ┣ 📜 app.py              # Main user app (students)
 ┣ 📜 admin.py            # Admin-only dashboard
 ┣ 📜 fmp_db.py           # All database functions
 ┣ 📜 requirements.txt    # Required packages
 ┗ 📁 assets/             # (optional) for logos/images/css if any
```

---

## 🧠 Technologies Used

- Python
- Streamlit
- MySQL (remote or local)
- Plotly (for charts)
- Pandas

---

## 🖥 How to Run Locally

### 🔧 1. Clone the Repo

```bash
git clone https://github.com/mehta-g1/FixMyCampus.git
cd FixMyCampus
```

### 📦 2. Install Dependencies

```bash
pip install -r requirements.txt
```

Required libraries:

```
streamlit
mysql-connector-python
pandas
plotly
streamlit-option-menu
```

### 🛢 3. Setup Database

- Use the SQL tables auto-created in `fmp_db.py` or manually run:

```sql
CREATE DATABASE fmp;

-- The tables will auto-create when you run the app
```

- You can use a local or remote MySQL database.
- Update DB credentials inside `fmp_db.py`:

```python
def get_connection():
    return mysql.connector.connect(
        host="your_host",
        user="your_user",
        password="your_pass",
        database="your_db"
    )
```

---

## 🚀 Run the App

### ▶ For Students App:

```bash
streamlit run app.py
```

### 🛡 For Admin App:

```bash
streamlit run admin.py --server.port 8504
```

(Port is optional — just keeps it separate)

---

## 🌐 Streamlit Cloud Deployment

**This project is not live yet on Streamlit Cloud**, but you can deploy by:

1. Push code to GitHub
2. Go to [streamlit.io/cloud](https://streamlit.io/cloud)
3. Create a new app using this repo
4. Make sure `fmp_db.py` connects to **remote MySQL** (like freesqldatabase)

---

## 🧪 Demo Credentials (for testing)

> ⚠ Change in production!

- **Admin**  
  - Username: `admin@1234`  
  - Password: `123`  

---

## 🙌 Contributing

PRs and contributions are welcome! Please create an issue before submitting a pull request.

---

## 📬 Contact

- 📧 Email: vikahmehta@mail.com
- 🌐 Website: [mitmeerut.net.in](https://mitmeerut.net.in)
- 📇 Linkedin [Vikash Mehta](https://www.linkedin.com/in/mehta-g1/)
---

## ⭐ Credits

Developed by Vikash & Team — Meerut Institute of Technology  
