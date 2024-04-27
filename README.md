This Is Essentialy A test file for macbooks in school that let you almost download anything without having to execute 


I know it sounds Confusing but this is just a test so this file is temporaily being put up on the servers

This code is also just a test

#include <iostream>

// Function to calculate the factorial of a number using recursion
unsigned long long factorial(int n) {
    if (n == 0 || n == 1) {
        return 1; // Base case: factorial of 0 and 1 is 1
    } else {
        return n * factorial(n - 1); // Recursive call to calculate factorial
    }
}

int main() {
    int number;
    std::cout << "Enter a non-negative integer to calculate its factorial: ";
    std::cin >> number;

    if (number < 0) {
        std::cout << "Factorial is not defined for negative numbers." << std::endl;
    } else {
        unsigned long long result = factorial(number);
        std::cout << "Factorial of " << number << " is: " << result << std::endl;
    }
    #include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    // Seed the random number generator
    srand(time(0));

    // Generate a random number between 1 and 100
    int secretNumber = rand() % 100 + 1;
    int guess;
    int attempts = 0;

    std::cout << "Welcome to the Guessing Game!" << std::endl;
    std::cout << "I have selected a number between 1 and 100. Try to guess it!" << std::endl;

    do {
        std::cout << "Enter your guess: ";
        std::cin >> guess;
        attempts++;

        if (guess < secretNumber) {
            std::cout << "Too low! Try again." << std::endl;
        } else if (guess > secretNumber) {
            std::cout << "Too high! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You've guessed the number in " << attempts << " attempts." << std::endl;
        }
    } while (guess != secretNumber);

    return 0;
}#include <iostream>

class ATM {
private:
    double balance;

public:
    // Constructor to initialize the balance
    ATM(double initialBalance) : balance(initialBalance) {}

    // Function to check balance
    void checkBalance() {
        std::cout << "Your current balance is: $" << balance << std::endl;
    }

    // Function to withdraw money
    void withdraw(double amount) {
        if (amount > balance) {
            std::cout << "Insufficient funds! Your current balance is: $" << balance << std::endl;
        } else {
            balance -= amount;
            std::cout << "Withdrawal successful! Remaining balance: $" << balance << std::endl;
        }
    }

    // Function to deposit money
    void deposit(double amount) {
        balance += amount;
        std::cout << "Deposit successful! New balance: $" << balance << std::endl;
    }
};

int main() {
    // Create an instance of ATM with an initial balance of $1000
    ATM atm(1000);

    int choice;
    double amount;

    do {
        std::cout << "\nATM Menu:\n1. Check Balance\n2. Withdraw\n3. Deposit\n4. Exit\nEnter your choice: ";
        std::cin >> choice;

        switch (choice) {
            case 1:
                atm.checkBalance();
                break;
            case 2:
                std::cout << "Enter the amount to withdraw: $";
                std::cin >> amount;
                atm.withdraw(amount);
                break;
            case 3:
                std::cout << "Enter the amount to deposit: $";
                std::cin >> amount;
                atm.deposit(amount);
                break;
            case 4:
                std::cout << "Exiting ATM. Have a nice day!" << std::endl;
                break;
            default:
                std::cout << "Invalid choice! Please enter a number between 1 and 4." << std::endl;
                break;
        }
    } while (choice != 4);

    return 0;
}
