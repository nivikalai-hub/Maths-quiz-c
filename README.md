# Maths-quiz-c#include <stdio.h>
#include <time.h>

int main() {
    int answer, score = 0;
    time_t start, end;
    double time_taken;

    printf(" Welcome to Nivi's Maths Quiz! \n");
    printf("You have 10 seconds to answer each question!\n\n");

    // Question 1
    printf("1) What is 5 + 3? ");
    time(&start); // start time
    scanf("%d", &answer);
    time(&end); // end time

    time_taken = difftime(end, start);
    if (time_taken > 10) {
        printf("Time's up! You took %.0f seconds\n", time_taken);
    } else if (answer == 8) {
        printf(" Correct!\n");
        score++;
    } else {
        printf("Wrong! The correct answer is 8\n");
    }

    // Question 2
    printf("2) What is 6 * 4? ");
    time(&start);
    scanf("%d", &answer);
    time(&end);

    time_taken = difftime(end, start);
    if (time_taken > 10) {
        printf(" Time's up! You took %.0f seconds\n", time_taken);
    } else if (answer == 24) {
        printf(" Correct!\n");
        score++;
    } else {
        printf(" Wrong! The correct answer is 24\n");
    }

    // Add more questions the same way...

    // Final Score
    printf("\n You scored %d out of 2\n", score);  // Change number if more questions added

    return 0;
}
