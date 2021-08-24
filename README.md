# CPL FINAL PROJECT.
here we gonna show up the basic code we used in our project and define what every function did.

## We used (print_menu) function.
this a function to display choosing a number to go to encryption technique, or decryption technique, or exiting the program.
and this is our code for this partition :
```C
#include<stdio.h>
int print_menu(void) {
	int c;
	printf("Choose one of the following options : \n");
	printf("[1] Encrypt the message \n");
	printf("[2] Decrypt the message \n");
	printf("[3] Exit the program \n");
	scanf("%d", &c);
	return c;
}
```

## An encryption function.
this function allows the user to type a message to encrypt it by simple substitution method.
and this is our code for this partition :
```C
void encrypt(void) {
	char user_input[50];
	int i;
	printf("Please type the message you want to encrypt : \n");
	scanf("%s", user_input);
	for(i = 0; (i < 50 && user_input[i] != '\0'); i++)
        user_input[i] = user_input[i] + 3;
	printf("\nEncrypted string: %s\n", user_input);

}
```
we have defined a character array (user_input) to receive the user input and store it by (scanf), and we have defined a variable (i) which its data type is integer which will be used later in a for loop which is responsible for calculating the stored message to turn it to a different words by encrypting it by adding 3 letters in the alphabet using simple substitution, then printing the encrypted message.

## A decryption function.
this function allows the user to type a message to decrypt it by simple substitution method.
and this is our code for this partition :
```C
void decrypt() {
	char user_input2[50];
	int i;
	printf("Please type the message you want to decrypt : \n");
	scanf("%s", user_input2);
	 for(i = 0; (i < 50 && user_input2[i] != '\0'); i++)
        user_input2[i] = user_input2[i] - 3;
    printf("\nDecrypted string: %s\n", user_input2);
}
```
we have defined a character array (user_input2) to receive the user input and store it by (scanf), and we have defined a variable (i) which its data type is integer which will be used later in a for loop which is responsible for calculating the stored message to turn it to a different words by decrypting it by subtracting 3 letters in the alphabet using simple substitution, then printing the decrypted message.

## Main function.
this is the main function for the program that contains all the excuted functions.
and this is our code for this partition :
```C
int main() {
	int choice;
	choice = print_menu();
	while (choice != 3) {
		if (choice == 1) {
			encrypt();
		}
		else if (choice == 2) {
			decrypt();
		}
		choice = print_menu();
	}
	return 0 ;
}
```
we have defined a variable (choice) which its data type is integer and then we stored (print_menu) function inside it. then we made (while loop) to check if the user input not equal 3. inside the while loop we created if condition checks if the user entered 1, it calls the (encrypt()) function to be excuted. and if the user entered 2, it calls the (decrypt()) function to be excuted. finally, we put choice equal to (print_menu()) function to print the menu as long as the user entered 1,2. and if the user entered 3, the program will be closed and the procces will be ended.
