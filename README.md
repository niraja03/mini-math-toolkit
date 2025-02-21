#include<iostream>
using namespace std;

#math toolkit
int main() {
int choice;
do {
cout << "\n1. Swap Numbers\n2. Check Armstrong\n3. Factorial\n4. Check Prime\n5. Array Average\n0. Exit\nChoose: ";
cin >> choice;

    if (choice == 1) { // Swap Numbers
        int a, b, temp;
        cout << "Enter any number 1: ";
        cin >> a;
        cout << "Enter any number 2: ";
        cin >> b;
        temp = a;
        a = b;
        b = temp;
        cout << "After swapping: a = " << a << ", b = " << b << endl;
    } 
    else if (choice == 2) { // Check Armstrong
        int n, temp, sum = 0;
        cout << "Enter number: ";
        cin >> n;
        temp = n;
        while (temp) {
            int d = temp % 10;
            sum += d * d * d;
            temp /= 10;
        }
        cout << (sum == n ? "Armstrong\n" : "Not Armstrong\n");
    } 
    else if (choice == 3) { // Factorial
        int n, fact = 1;
        cout << "Enter number: ";
        cin >> n;
        for (int i = 1; i <= n; ++i) fact *= i;
        cout << "Factorial: " << fact << endl;
    } 
    else if (choice == 4) { // Check Prime
        int n, flag = 1;
        cout << "Enter number: ";
        cin >> n;
        if (n <= 1) flag = 0;
        for (int i = 2; i <= sqrt(n); ++i)
            if (n % i == 0) { flag = 0; break; }
        cout << (flag ? "Prime\n" : "Not Prime\n");
    } 
    else if (choice == 5) { // Array Average
        int n;
        cout << "Enter array size: ";
        cin >> n;
        if (n <= 0) { 
            cout << "Invalid size.\n"; 
            continue; 
        }
        double sum = 0, num;
        for (int i = 0; i < n; ++i) {
            cout << "Enter element " << i + 1 << ": ";
            cin >> num;
            sum += num;
        }
        cout << "Average: " << sum / n << endl;
    }
} while (choice != 0);

return 0;
}
