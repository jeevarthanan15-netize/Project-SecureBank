# SecureBank - Banking Management System

## 📌 Project Overview

SecureBank is a console-based Banking Management System developed using **Java, MySQL, and JDBC**. It allows users to create bank accounts, deposit and withdraw money, transfer funds, view account details, and check transaction history.

The project demonstrates core Java concepts and database connectivity through a simple menu-driven application.

## 🚀 Features

- **Create Account:** Create Savings or Current accounts.
- **Deposit Money:** Deposit money into an account.
- **Withdraw Money:** Withdraw money according to account rules.
- **Transfer Money:** Transfer funds between accounts.
- **View Account Details:** Display account information and balance.
- **Transaction History:** View transaction records.
- **Savings Interest:** Calculate yearly interest for Savings accounts.
- **PIN Authentication:** Authenticate users before banking operations.
- **Account Locking:** Lock an account after repeated incorrect PIN attempts.

## 🛠️ Technologies Used

- Java (JDK 21)
- MySQL
- JDBC
- MySQL Connector/J
- Visual Studio Code
- Git and GitHub

## 📂 Project Structure

```text
banking/
├── src/
│   ├── app/
│   │   └── BankApp.java
│   ├── database/
│   │   └── DBConnection.java
│   ├── dao/
│   │   ├── AccountDAO.java
│   │   └── TransactionDAO.java
│   ├── exception/
│   │   └── InsufficientFundsException.java
│   ├── model/
│   │   ├── Account.java
│   │   ├── SavingsAccount.java
│   │   └── CurrentAccount.java
│   └── service/
│       └── BankService.java
├── sql/
│   └── securebank.sql
├── lib/
│   └── mysql-connector-j/
├── .gitignore
└── README.md
```

## ⚙️ Setup and Installation

### 1. Install the Requirements

Install Java JDK 21, MySQL Server, and Visual Studio Code.

### 2. Clone the Repository

```bash
git clone https://github.com/jeevarthanan15-netize/Project-SecureBank.git
cd Project-SecureBank
```

### 3. Create the Database

Open MySQL Workbench and execute the SQL statements in `sql/securebank.sql` to create the database and required tables.

### 4. Configure Database Connection

Update `src/database/DBConnection.java` with your local MySQL username and password.

**Security note:** Never commit your real database password to GitHub.

### 5. Compile the Project

Run these commands from the project root in PowerShell. Adjust the Connector/J path to match the JAR file in your `lib` folder.

```powershell
javac -cp ".\lib\mysql-connector-j\mysql-connector-j.jar" -d out src\database\DBConnection.java src\exception\InsufficientFundsException.java src\model\Account.java src\model\SavingsAccount.java src\model\CurrentAccount.java src\dao\AccountDAO.java src\dao\TransactionDAO.java src\service\BankService.java src\app\BankApp.java
```

### 6. Run the Application

```powershell
java -cp "out;.\lib\mysql-connector-j\mysql-connector-j.jar" app.BankApp
```

## 💻 Application Menu

1. Create Account
2. Deposit Money
3. Withdraw Money
4. Transfer Money
5. View Account Details
6. View Transaction History
7. Calculate Savings Interest
8. Exit

## 📚 Java Concepts Demonstrated

- Classes and Objects
- Inheritance
- Method Overriding
- Encapsulation
- Abstract Classes
- Exception Handling
- Collections
- JDBC and SQL
- Data Access Objects (DAO)
- Object-Oriented Programming

## 🏦 Account Rules

- **Savings Account:** Maintains a minimum balance of ₹1,000 and calculates yearly interest at 4%, according to the implemented rules.
- **Current Account:** Supports an overdraft limit of ₹5,000, according to the implemented rules.
- **Insufficient Funds Exception:** Prevents withdrawals that violate the account's balance rules.

## 🔐 Security and Limitations

This is an educational project, not a production banking system. Depending on the current implementation, account locking may be session-based and PINs may not be securely hashed. Production systems require secure credential storage, persistent lockout controls, input validation, and database transactions for transfers.

## 👥 Team Project

SecureBank is a collaborative academic project created to practice Java programming, database integration, and Git/GitHub teamwork.

## 📄 License

This project is intended for educational purposes.
