# 🧪 API Testing - Student Management System (Postman Project)

This project showcases a complete **API Testing workflow** for a Student Management REST API using **Postman** and **Newman CLI**. It includes all the key testing artifacts: CRUD operations, test validations, manual test cases, test data, and detailed reports — all in a clean GitHub-ready format.

---

## 📚 Project Overview

The purpose of this project is to demonstrate practical API testing skills using a mock backend (JSON Server). It covers:

- Validating API responses for all major operations (`GET`, `POST`, `PUT`, `DELETE`)
- Writing and running tests using Postman
- Automating API testing using Newman
- Asserting headers, status codes, field values, data types, and schemas
- Maintaining a professional QA test case document
- Generating HTML reports for execution summary

---

## 🚀 Features Tested

| Feature        | Method | Endpoint                     |
|----------------|--------|------------------------------|
| Get All Students   | GET    | `/students`                    |
| Get Single Student | GET    | `/students/:id`                |
| Add New Student    | POST   | `/students`                    |
| Update Student     | PUT    | `/students/:id`                |
| Delete Student     | DELETE | `/students/:id`                |
| Error Handling     | GET/POST/DELETE | Invalid/missing inputs |

---

## 📁 Folder Structure

```
API_Testing_StudentApp_Postman/
├── Student_API_Collection.postman_collection.json   # Postman collection file
├── students_data.json                               # Sample API data for local server
├── TestCases/
│   └── Student_Test_Cases.xlsx                      # Excel sheet with test cases
├── newman-report.html                               # Newman HTML test result report
├── README.md                                        # Project documentation
```

---

## 🧰 Tools Used

- ✅ Postman – API testing interface
- ✅ Newman – Command-line execution and reporting
- ✅ JSON Server – Local mock API for testing
- ✅ Excel – Manual test case documentation
- ✅ Assertions – JavaScript validation logic inside Postman
- ✅ JSON Schema – For validating structure of responses

---

## 🧪 Sample Assertions (Postman Tests)

- `pm.response.code === 200`
- `pm.response.header.contains("Content-Type")`
- `pm.expect(jsonData.name).to.eql("Tithi Paul")`
- `pm.expect(jsonData.courses).to.include("API Testing")`
- JSON schema validation using `tv4`

---

## 📝 Manual Test Case Examples

| TCID   | Request Type | Endpoint              | Expected Status | Expected Result         |
|--------|--------------|-----------------------|------------------|--------------------------|
| TC_01  | GET          | /students             | 200              | List of all students     |
| TC_02  | GET          | /students/3           | 200              | One student by ID        |
| TC_06  | GET          | /students/9999        | 404              | Student not found        |
| TC_07  | POST         | /students (invalid)   | 400              | Missing required fields  |

📌 Full test cases are inside `Student_Test_Cases.xlsx`

---

## 📊 HTML Report Preview

The `newman-report.html` file contains:
- Pass/fail breakdown
- Graphs and colored status
- Request/response logs
- Assertion counts
- Response time stats

Generated using:
```bash
newman run Student_API_Collection.postman_collection.json --reporters cli,htmlextra --reporter-htmlextra-export newman-report.html
```

---

## 💻 How to Run

### 🔹 Start your mock API server:
```bash
json-server --watch students_data.json
```

### 🔹 Run collection using Newman:
```bash
newman run Student_API_Collection.postman_collection.json --reporters cli,htmlextra --reporter-htmlextra-export newman-report.html
```

---

## 👩‍💻 Author

**Tithi Paul**  
🧪 Aspiring Software QA Engineer  
🎓 MSc in Advanced Computer Science — University of Sheffield  
📧 Email: [tithi.cse3.bu@gmail.com](mailto:tithi.cse3.bu@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/paultithi/)

---

## 📬 Let's Connect

If you're a recruiter or hiring manager, feel free to visit this repository to evaluate my API testing skills — or connect with me on LinkedIn(🔗 [Visit My LinkedIn Profile](https://www.linkedin.com/in/paultithi/))


