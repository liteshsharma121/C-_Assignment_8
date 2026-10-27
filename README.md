
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "EXCEPTION HANDLING IN C++" << endl;
    cout << "-------------------------" << endl;

    cout << "Enter numerator: ";
    cin >> a;

    cout << "Enter denominator: ";
    cin >> b;

    try {
        if (b == 0) {
            throw b;
        }

        if (a < 0 || b < 0) {
            throw "Negative numbers are not allowed.";
        }

        cout << "Result: " << a / b << endl;
    }
    catch (int) {
        cout << "Exception caught: Division by zero is not allowed."
             << endl;
    }
    catch (const char* message) {
        cout << "Exception caught: " << message << endl;
    }

    cout << "Program continues normally." << endl;

    return 0;
}

