# student-utility-toolkit
This is my first C program, which calculates the percentage of subjects based on their marks. It uses basic concepts like arrays, loops, and conditional statements.
#include <stdio.h>

int main() {
    int n;
    int marks[10];
    int total = 0;
    float percentage;

    printf("Enter number of subjects: ");
    scanf("%d", &n);

    for(int i = 0; i < n; i++) {
        printf("Enter marks of subject %d: ", i + 1);
        scanf("%d", &marks[i]);
        total += marks[i];
    }

    percentage = total / (float)n;

    printf("\nTotal Marks = %d", total);
    printf("\nPercentage = %.2f", percentage);

    if(percentage >= 90)
        printf("\nGrade: A");
    else if(percentage >= 75)
        printf("\nGrade: B");
    else if(percentage >= 60)
        printf("\nGrade: C");
    else
        printf("\nGrade: D");

    return 0;
}
