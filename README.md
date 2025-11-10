#include <iostream>
#include <cmath>
using namespace std;
int main() {
    double a, b, c, discriminant, realPart, imaginaryPart;
    cout << "Enter coefficients a, b, and c: ";
    cin >> a >> b >> c;
    discriminant = b * b - 4 * a * c;
    if (discriminant > 0) {
        double root1 = (-b + sqrt(discriminant)) / (2 * a);
        double root2 = (-b - sqrt(discriminant)) / (2 * a);
        cout << "Roots are real and distinct.\n";
        cout << "Root 1 = " << root1 << "\n";
        cout << "Root 2 = " << root2 << "\n";
    }
    else if (discriminant == 0) {
        double root = -b / (2 * a);
        cout << "Roots are real and equal.\n";
        cout << "Root = " << root << "\n";
    }
    else {
        realPart = -b / (2 * a);
        imaginaryPart = sqrt(-discriminant) / (2 * a);
        cout << "Roots are complex and imaginary.\n";
        cout << "Root 1 = " << realPart << " + " << imaginaryPart << "i\n";
        cout << "Root 2 = " << realPart << " - " << imaginaryPart << "i\n";
    }
    return 0;
}
