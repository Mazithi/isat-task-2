# isat-task-2
Adding Conversion Functions and menu
// Mazithi Mhloli
//0408080954089

#include <iostream>
#include <string>
#include <bitset>

using namespace std;

// Convert Decimal to Binary
void decimalToBinary() {
    int decimal;
    cout << "Enter a decimal number: ";
    cin >> decimal;
    cout << "Binary: " << bitset<8>(decimal) << endl; // shows 8-bit binary
}

// Convert Binary to Decimal
void binaryToDecimal() {
    string binary;
    cout << "Enter a binary number: ";
    cin >> binary;
    int decimal = stoi(binary, nullptr, 2); // convert binary string to decimal
    cout << "Decimal: " << decimal << endl;
}

// Convert Decimal to Hexadecimal
void decimalToHex() {
    int decimal;
    cout << "Enter a decimal number: ";
    cin >> decimal;
    cout << "Hexadecimal: " << hex << decimal << endl;
}

// Convert Binary to Hexadecimal
void binaryToHex() {
    string binary;
    cout << "Enter a binary number: ";
    cin >> binary;
    int decimal = stoi(binary, nullptr, 2);
    cout << "Hexadecimal: " << hex << decimal << endl;
}

int main() {
    int choice;

    do {
        // Display menu
        cout << "\n--- Number Converter Menu ---\n";
        cout << "1. Decimal to Binary\n";
        cout << "2. Binary to Decimal\n";
        cout << "3. Decimal to Hexadecimal\n";
        cout << "4. Binary to Hexadecimal\n";
        cout << "5. Exit\n";
        cout << "Enter your choice (1-5): ";
        cin >> choice;

        // Run selected option
        if (choice == 1) decimalToBinary();
        else if (choice == 2) binaryToDecimal();
        else if (choice == 3) decimalToHex();
        else if (choice == 4) binaryToHex();
        else if (choice == 5) cout << "Goodbye!\n";
        else cout << "Invalid choice. Try again.\n";

    } while (choice != 5);

    return 0;
}
//0408080954089

