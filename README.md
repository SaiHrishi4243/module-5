# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM

```C

#include <stdio.h>
#include <stdlib.h>
int main() 
{
    char *str;
    str = (char *)malloc(100 * sizeof(char));
    printf("Enter a string: ");
    scanf("%[^\n]", str);  
    printf("You entered: %s\n", str);
    free(str);
    return 0;
}

```

## OUTPUT
		       	
![Screenshot 2025-04-30 012743](https://github.com/user-attachments/assets/b5ec493a-c514-41b2-a6f6-517c7f0b3aea)

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM

```C

#include <stdio.h>
struct student 
{
    char name[50];
    int roll_no;
    float marks;
};
int main() 
{
    struct student s;
    printf("Enter name: ");
    scanf("%s", s.name);
    printf("Enter roll number: ");
    scanf("%d", &s.roll_no);
    printf("Enter marks: ");
    scanf("%f", &s.marks);
    printf("\nStudent Details:\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll_no);
    printf("Marks: %.2f\n", s.marks);
    return 0;
}

```

## OUTPUT

![Screenshot 2025-04-30 013253](https://github.com/user-attachments/assets/4765c538-01b4-4ae4-ac64-afb0ce1f8e67)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM

```C

#include <stdio.h>
int main() 
{
    int x,z;
    int *y;
    int area;
    printf("Enter length of the rectangle: ");
    scanf("%d", &x);
    printf("Enter breadth of the rectangle: ");
    scanf("%d", &z);
    *y=z;
    area = x *(*y);  
    printf("Area of the rectangle: %d", area ); 
    return 0;
}

```

## OUTPUT

![Screenshot 2025-04-30 013800](https://github.com/user-attachments/assets/98d8ae48-50a1-48d4-86b4-6549d0c56f98)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM

```C

#include <stdio.h>
struct employee 
{
    char name[50];
    int id;
    float salary;
};
int main() 
{
    struct employee e;
    printf("Enter employee name: ");
    scanf("%s", e.name);
    printf("Enter employee ID: ");
    scanf("%d", &e.id);
    printf("Enter employee salary: ");
    scanf("%f", &e.salary);
    float gross_salary = e.salary + (e.salary * 0.20);
    printf("\nEmployee Details:\n");
    printf("Name: %s\n", e.name);
    printf("ID: %d\n", e.id);
    printf("Salary: %.2f\n", e.salary);
    printf("Gross Salary (including 20%% bonus): %.2f\n", gross_salary);
    return 0;
}

```

 ## OUTPUT

 ![Screenshot 2025-04-30 014204](https://github.com/user-attachments/assets/a7d267ab-bd06-452b-845f-d8192530fae5)

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM

```C

#include <stdio.h>
struct student 
{
    char name[10];       
    int rollno;          
    int subject[5];      
    int total;          
};
int main() 
{
    struct student s[2];
    int n, i, j;
    for (i = 0; i < 2; i++) 
    {
        scanf("%d", &n);  
        for (j = 0; j < 5; j++) 
        {
            scanf("%d", &s[i].subject[j]);  
        }
    }
    for (i = 0; i < 2; i++) 
    {
        s[i].total = 0;
        for (j = 0; j < 5; j++) 
        {
            s[i].total += s[i].subject[j];
        }
    }
    for (i = 0; i < 2; i++) 
    {
        printf("Total marks of student %d: %d\n", i + 1, s[i].total);
    }
    return 0;
}

```

## OUTPUT

 ![Screenshot 2025-04-30 015805](https://github.com/user-attachments/assets/01c52ba7-6df5-4672-bd5a-e02dff2b1bbe)

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


