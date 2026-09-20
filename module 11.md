

### EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>
int max_of_four(int a,int b,int c,int d)
{
    if(a>b && a>c && a>d)
    {
       return a;
    }
    else if(b>a && b>c && b>d)
    {
         return b;
    }
    else if(c>a && c>b && c>d)
    {
        return c;
    }
    else
    {
        return d;
    }
}
int main()
{
    int a,b,c,d,m;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    m=max_of_four(a,b,c,d);
    printf("%d",m);
    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/ba750873-0383-435e-8597-eb545771f3a1)


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
### EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>
void calculate_the_maximum(int n, int k) {
    int max_and = 0;
    int max_or = 0;
    int max_xor = 0;
    for (int a = 1; a < n; a++) {
        for (int b = a + 1; b <= n; b++) {
        int and_val = a & b;
        int or_val = a | b;
        int xor_val = a ^ b;
        if (and_val < k && and_val > max_and) {
            max_and = and_val;
        }
       if (or_val < k && or_val > max_or) {
          max_or = or_val;
        }
       if (xor_val < k && xor_val > max_xor) {
           max_xor = xor_val;
       }
    }
}
printf("%d\n", max_and);
printf("%d\n", max_or);
printf("%d\n", max_xor);
}
int main() {
    int n, k;
    scanf("%d %d", &n, &k);
    calculate_the_maximum(n, k);
    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/9639bd51-8b55-40a4-8da2-88afa5d0e501)


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
### EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int shelves, queries;
    scanf("%d %d", &shelves, &queries);
    int* book_count = calloc(shelves, sizeof(int));
    int** pages = malloc(shelves * sizeof(int*));
    for (int i = 0; i < shelves; i++)
    {
         pages[i] = NULL;
    }
    for (int i = 0; i < queries; i++)
    {
        int type;
        scanf("%d", &type);
        if (type == 1)
    {
        int shelf, page;
        scanf("%d %d", &shelf, &page);
        int count = book_count[shelf];
        pages[shelf] = realloc(pages[shelf], (count + 1) * sizeof(int));
        pages[shelf][count] = page;
        book_count[shelf]++;
    }
    else if (type == 2)
    {
         int shelf, book;
         scanf("%d %d", &shelf, &book);
         printf("%d\n", pages[shelf][book]);
    }
    else if (type == 3)
    {
        int shelf;
        scanf("%d", &shelf);
        printf("%d\n", book_count[shelf]);
    }
}
for (int i = 0; i < shelves; i++)
{
    free(pages[i]);
}
free(pages);
free(book_count);
return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/5f24e87b-1410-4181-80e9-eaf3d97f5f3c)



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
### EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int n;
    int *arr;
    int sum = 0;
    scanf("%d", &n);
    arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL)
    {
       printf("Memory allocation failed\n");
       return 1;
    }
    for (int i = 0; i < n; i++)
    {
       scanf("%d", &arr[i]);
       sum += arr[i];
    }
    printf("%d\n", sum);
    free(arr);
    return 0;
}
```


Output:

![image](https://github.com/user-attachments/assets/e32227b2-d2cd-4e20-a78d-6c4b8ba02f73)


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
### EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
int main() {
    char sentence[1000];
    int i, word_count = 0, in_word = 0;
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);
    for (i = 0; sentence[i] != '\0'; i++) {
        if (sentence[i] != ' ' && sentence[i] != '\n' && !in_word) {
           in_word = 1;
           word_count++;
        } else if (sentence[i] == ' ' || sentence[i] == '\n') {
            in_word = 0;
        }
}
printf("The number of words in the sentence: %d\n", word_count);
return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/949c9316-ed7c-427f-a43f-a43ed9586f85)




Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
