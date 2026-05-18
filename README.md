# pat2.subtask-3
#include <iostream> 
#include <iomanip> 
using namespace std;

const int NUM_EXPERIMENTS = 3;
const int NUM_READINGS = 3;

int main() {
    int i, j;
    double readingValue, total, average;

    for (i = 1; i <= NUM_EXPERIMENTS; i++) {
        total = 0;
        cout << "\nEXPERIMENT " << i << endl;
        cout << "===========\n";

        for (j = 1; j <= NUM_READINGS; j++) {
            cout << "Enter reading " << j << " value: ";
            cin >> readingValue;
            total = total + readingValue;  
        }

        average = total / NUM_READINGS; 

        
        if (average > 300) {
            cout << "Experiment " << i << " average: "
                 << fixed << setprecision(2) << average
                 << " → Above acceptable range\n";
        } 
        else if (average >= 100 && average <= 300) {
            cout << "Experiment " << i << " average: "
                 << fixed << setprecision(2) << average
                 << " → Within acceptable range\n";
        } 
        else {
            cout << "Experiment " << i << " average: "
                 << fixed << setprecision(2) << average
                 << " → Below acceptable range\n";
        }
    }

    return 0;
}
