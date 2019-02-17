# bug-free-ecstasy
#include <iostream>
#include <string>
using namespace std;

int main ()
{

cout << endl <<  "Please enter all the grades you wish to use for your GPA." << endl;

cout << endl <<  "When you have finished, enter N to indicate that you have no more grades." << endl;

cout << endl << "The highest acceptable grade is 100%, if you got higher than this congratulations but please enter only 100 as grade."  << endl;
cout << endl;
float Grade = 0;
int NumClass = 0;
const int Stop = -1;
float GPAVal = 0;
float TotGPAVal = 0;
float GPA = 0;
string SemName;
while (SemName != -1)
        {
        cout << "Please enter name of the semester of grades you want to enter." << endl;
        cin >> SemName;
        cout << SemName << endl;
        do {
                cout << endl << "Please enter grade: ";
                cin >> Grade;
                        if  ( Grade <=100 && Grade >= 90 )
                                {
                                GPAVal = 4.0;
                                cout << "Grade: " << Grade << "%; GPA Value: 4.0" << endl;
                                TotGPAVal = TotGPAVal + GPAVal;
                                }
                        else if ( Grade < 90 && Grade >= 80 )
                                {
                                GPAVal = 3.0;
                                cout << "Grade: " << Grade << "%; GPA Value: 3.0" << endl;
                                TotGPAVal = TotGPAVal + GPAVal;
                                }
                        else if ( Grade < 80 && Grade >= 70 )
                                {
                                GPAVal = 2.0;
                                cout << "Grade: " << Grade << "%; GPA Value: 2.0" << endl;
                                TotGPAVal = TotGPAVal + GPAVal;
                                }
                        else if ( Grade < 70 && Grade >= 60 )
                                {
                                GPAVal = 1.0;
                                cout << "Grade: " << Grade << "%; GPA Value: 1.0" << endl;
                                TotGPAVal = TotGPAVal + GPAVal;
                                }
                        else if ( Grade < 60 && Grade >= 0 )
                                {
                                GPAVal = 0.0;
                                cout << "Grade: " << Grade << "%; GPA Value: 0.0" << endl;
                                TotGPAVal = TotGPAVal + GPAVal;
                                }
                        else if ( Grade = Stop )
                                {
                                GPA = (TotGPAVal / NumClass);
                                cout << endl<< "Your overall GPA, after " << NumClass << " courses, is " << GPA << "." << endl << endl;
                                }
                NumClass = NumClass + 1;
                }
        while (( Grade >= 0 ) && ( Grade <=100 ));
        if (SemName = -1)
                {
                cout << "Thank you for using this program!" << endl;
                }
        }
return (0);
}
