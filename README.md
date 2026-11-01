# OOPS
#include <iostream>
#include <string>
using namespace std;

// Parent Class
class Employee {
public:
    int employeeId;
    string employeeName;

    void getBasicDetails() {
        cout << "Enter Employee ID: ";
        cin >> employeeId;

        cout << "Enter Employee Name: ";
        getline(cin >> ws, employeeName);
    }

    void showBasicDetails() {
        cout << "Employee ID: " << employeeId << endl;
        cout << "Employee Name: " << employeeName << endl;
    }
};

// Child Class
class PermanentEmployee : public Employee {
public:
    string department;
    double monthlySalary;

    void getJobDetails() {
        cout << "Enter Department: ";
        getline(cin >> ws, department);

        cout << "Enter Monthly Salary: ";
        cin >> monthlySalary;
    }

    void showAllDetails() {
        cout << "\n--- Employee Details ---" << endl;

        showBasicDetails();

        cout << "Department: " << department << endl;
        cout << "Monthly Salary: Rs. "
             << monthlySalary << endl;
    }
};

// Main Function
int main() {
    PermanentEmployee emp;

    cout << "EMPLOYEE DETAILS SYSTEM" << endl;

    emp.getBasicDetails();
    emp.getJobDetails();
    emp.showAllDetails();

    return 0;
}
