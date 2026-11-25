# Ex-1 IMPLEMENTATION-OF-SYMBOL-TABLE
# Register Number :212225040495
# Date : 25-11-2026
# AIM :
## To write a C program to implement a symbol table.
# ALGORITHM
1.	Start the program.
2.	Get the input from the user with the terminating symbol ‘$’.
3.	Allocate memory for the variable by dynamic memory allocation function.
4.	If the next character of the symbol is an operator then only the memory is allocated.
5.	While reading, the input symbol and memory address are inserted into the symbol table.
6.	The steps are repeated till ‘$’ is reached.
7.	To reach a variable, enter the variable to be searched and the symbol table has been checked for the corresponding variable, the variable along with its address is displayed as a result.
8.	Stop the program. 
# PROGRAM
```
printf("Enter the Expression terminated by $: ");
while ((c = getchar()) != '$' && i < MAX_EXPRESSION_SIZE - 1) {
	b[i++] = c;
}
b[i] = '\0';
n = i - 1;

printf("\nGiven Expression: %s\n", b);

printf("\nSymbol Table\n");
printf("Symbol\tType\t\tAddress\n");

for (j = 0; j <= n; j++) {
	c = b[j];
	if (isalpha((unsigned char)c)) {
		int alreadyExists = 0;
		for (k = 0; k < x; k++) {
			if (d[k] == c) {
				alreadyExists = 1;
				break;
			}
		}

		if (!alreadyExists) {
			d[x] = c;
			printf("%c\tidentifier\t%p\n", c, (void*)&d[x]);
			x++;
		}
	}
}

// Clear input buffer
while ((c = getchar()) != '\n' && c != EOF);

printf("\nEnter the symbol to search: ");
srch = getchar();

for (i = 0; i < x; i++) {
	if (srch == d[i]) {
		printf("Symbol Found\n");
		flag = 1;
		break;
	}
}
if (flag == 0)
	printf("Symbol Not Found\n");

return 0;
```
# OUTPUT

<img width="1166" height="656" alt="image" src="https://github.com/user-attachments/assets/9e888d5a-1c75-480d-867a-f9f09d4c1341" />


 
# RESULT
### The program to implement a symbol table is executed and the output is verified.
