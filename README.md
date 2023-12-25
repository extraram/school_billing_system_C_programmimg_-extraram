# school_billing_system_C_programmimg_-extraram
//School Billing System in C programming. You can expand on this foundation by adding features such as multiple students, handling multiple bills, storing data in files, etc., based on your project requirements.


#include <stdio.h>
#include <stdlib.h>

// Define structures for student and billing information
struct Student {
    int rollNumber;
    char name[50];
};

struct Bill {
    int billNumber;
    float amount;
};

// Function to input student details
void inputStudent(struct Student *student) {
    printf("Enter Roll Number: ");
    scanf("%d", &student->rollNumber);
    printf("Enter Name: ");
    scanf("%s", student->name);
}

// Function to generate a bill
void generateBill(struct Bill *bill) {
    printf("Enter Bill Number: ");
    scanf("%d", &bill->billNumber);
    printf("Enter Amount: ");
    scanf("%f", &bill->amount);
}

// Function to display student details
void displayStudent(struct Student student) {
    printf("Roll Number: %d\n", student.rollNumber);
    printf("Name: %s\n", student.name);
}

// Function to display bill details
void displayBill(struct Bill bill) {
    printf("Bill Number: %d\n", bill.billNumber);
    printf("Amount: %.2f\n", bill.amount);
}

int main() {
    // Declare variables
    struct Student student;
    struct Bill bill;

    // Input student details
    printf("Enter Student Details:\n");
    inputStudent(&student);

    // Generate a bill for the student
    printf("\nEnter Billing Information:\n");
    generateBill(&bill);

    // Display student details and bill information
    printf("\nStudent Details:\n");
    displayStudent(student);

    printf("\nBilling Information:\n");
    displayBill(bill);

    return 0;
}
