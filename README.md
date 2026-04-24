# attendance assignment

## Execute the following programs and create a  document in github with question, code and output and then upload the pdf file generated from github and also give the github link in the submission

### 1. Write a C program to find the maximum of three numbers without using logical operators.

PROGRAM:
```
#include <stdio.h>

int main() {
    int a, b, c, max;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    max = a;

    if (b > max)
        max = b;

    if (c > max)
        max = c;

    printf("Maximum = %d", max);

    return 0;
}
```

OUTPUT:

<img width="1186" height="592" alt="image" src="https://github.com/user-attachments/assets/8ee8d001-a178-4182-adda-7bbacddccb46" />


### 2. Write a  C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)

PROGRAM:
```
#include <stdio.h>

int main() {
    int year;

    printf("Enter year: ");
    scanf("%d", &year);

    if (year % 400 == 0) {
        printf("%d is a century leap year", year);
    }
    else if (year % 100 == 0) {
        printf("%d is not a leap year (century year)", year);
    }
    else if (year % 4 == 0) {
        printf("%d is a non-century leap year", year);
    }
    else {
        printf("%d is not a leap year", year);
    }

    return 0;
}
```

OUTPUT:

<img width="1180" height="651" alt="image" src="https://github.com/user-attachments/assets/f487a2df-0d76-4798-9078-6bad8a280db2" />


### 3. Write a C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without using built in functions.

PROGRAM:
```
#include <stdio.h>

int main() {
    char ch;

    printf("Enter a character: ");
    scanf(" %c", &ch);

    if ((ch >= 'A' && ch <= 'Z') || (ch >= 'a' && ch <= 'z')) {
        printf("Alphabet\n");

        if (ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U'||
            ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u') {
            printf("Vowel");
        } else {
            printf("Consonant");
        }
    }
    else if (ch >= '0' && ch <= '9') {
        printf("Digit");
    }
    else {
        printf("Special Character");
    }

    return 0;
}
```

OUTPUT:

<img width="1178" height="754" alt="image" src="https://github.com/user-attachments/assets/f6138bc3-a39a-4181-b521-cfaa7e535f71" />


### 4. Write a  C program for simple ATM simulation with operations Check Balance, Deposit,  Withdraw,  Exit using switch and update balance accordingly.

PROGRAM:
```
#include <stdio.h>

int main() {
    int choice;
    float balance = 1000, amount;

    do {
        printf("\n--- ATM Menu ---\n");
        printf("1. Check Balance\n");
        printf("2. Deposit\n");
        printf("3. Withdraw\n");
        printf("4. Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch(choice) {
            case 1:
                printf("Balance: %.2f\n", balance);
                break;

            case 2:
                printf("Enter amount to deposit: ");
                scanf("%f", &amount);
                balance += amount;
                printf("Deposited successfully\n");
                break;

            case 3:
                printf("Enter amount to withdraw: ");
                scanf("%f", &amount);
                if (amount <= balance) {
                    balance -= amount;
                    printf("Withdrawn successfully\n");
                } else {
                    printf("Insufficient balance\n");
                }
                break;

            case 4:
                printf("Thank you!\n");
                break;

            default:
                printf("Invalid choice\n");
        }

    } while(choice != 4);

    return 0;
}
```

OUTPUT:

<img width="1631" height="866" alt="image" src="https://github.com/user-attachments/assets/725846f3-f770-440c-aa53-59c6fcd0a733" />


### 5. Write a C program for menu driven calculator using switch statement.

PROGRAM:
```
#include <stdio.h>

int main() {
    int choice;
    float a, b;

    do {
        printf("\n--- Calculator ---\n");
        printf("1. Add\n2. Subtract\n3. Multiply\n4. Divide\n5. Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        if (choice >= 1 && choice <= 4) {
            printf("Enter two numbers: ");
            scanf("%f %f", &a, &b);
        }

        switch(choice) {
            case 1:
                printf("Result = %.2f\n", a + b);
                break;

            case 2:
                printf("Result = %.2f\n", a - b);
                break;

            case 3:
                printf("Result = %.2f\n", a * b);
                break;

            case 4:
                if (b != 0)
                    printf("Result = %.2f\n", a / b);
                else
                    printf("Cannot divide by zero\n");
                break;

            case 5:
                printf("Exiting...\n");
                break;

            default:
                printf("Invalid choice\n");
        }

    } while(choice != 5);

    return 0;
}
```

OUTPUT:

<img width="1627" height="864" alt="image" src="https://github.com/user-attachments/assets/2c761256-b554-466c-86c1-f5a18d0c0793" />
