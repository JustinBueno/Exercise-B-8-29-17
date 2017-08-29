// ExerciseB.cpp
#include <iostream>

using namespace std;

int main ()
{	
	// Variabes used to hold the inputs used double for accuracy for the average score 
	int numAssingments;             
	double totalScore, score, Avg;

	cout << "How many assignments did you have ? ";

	cin >> numAssingments;

	// for loop used i as a counter and added 1 to numAssingments because the counter starts at 1

	for (int i = 1; i < numAssingments + 1; i++)
	{
		cout << "What was the score for assignment " << i << endl;

		cin >> score;

		// the line below adds the scores to totalScore 
		
		totalScore += score;

		// if statement for scores to validate so no scores under 0 and over 100 are accepted 

		if (score < 0 || score > 100)
		{
			cout << "Invalid input. Enter score again: ";

			cin >> score;
		}

	}

	// below calculates the average of the scores by taking totalScore and dividing it by numAssingments inputed by user

		Avg = totalScore/numAssingments;

	// Prints total score and average

		cout << "The number of points scored was " << totalScore << " and the average of the scores was " << Avg << endl;
	
	// Below prints out a letter grade depending on the average 

		if(Avg >= 90)
		{
			cout << "congrats you got an A" << endl;
		}
		else if (Avg < 90 && Avg >= 80)
		{
			cout << "congrats you got a B" << endl;
		}
		else if (Avg < 80 && Avg >= 70)
		{
			cout << "you earned a C you can do better" << endl;
		}
		else if (Avg < 70 && Avg > 60) 
		{
			cout << "you received a D " << endl;
		}
		else if (Avg <= 60)
		{
			cout << "you got an F" << endl;
		}

	return 0;

}
