# Employee-Management-System

# Feature

User-Friendly Interface: Built using Java Swing

CRUD Operations: Add, update, delete, and view employee records

Persistent Storage: MySQL or SQLite integration via JDBC


# Launch with a custom database config
java -jar target/ems.jar --db-url jdbc:mysql://localhost:3306/ems --db-user root --db-pass pass123
GUI Mode
bash
Copy
Edit

# Compile and run
mvn compile exec:java -Dexec.mainClass="com.ems.Main"
Output Format

# Example Employee JSON export:

json
Copy
Edit
{
  "id": 101,
  "name": "Jane Doe",
  "department": "Finance",
  "designation": "Manager",
  "salary": 95000
}


# Project Structure
bash
Copy
Edit
.
├── src/
│   └── main/
│       ├── java/
│       │   └── com/ems/
│       │       ├── Main.java           # Launcher
│       │       ├── model/              # Data models
│       │       ├── view/               # Swing GUI classes
│       │       ├── controller/         # Business logic
│       │       └── db/                 # JDBC utilities
│       └── resources/
│           └── config.properties       # DB config
├── test/
│   └── java/
│       └── com/ems/
│           └── AllTests.java           # JUnit tests
├── .github/
│   └── workflows/
│       └── ci.yml                      # GitHub Actions workflow
├── pom.xml                             # Maven config
└── README.md
Development
bash
Copy
Edit


# Run all tests
mvn test

# Build the project
mvn package

# Check code style
mvn checkstyle:check
