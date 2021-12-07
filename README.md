#include <iostream>
using namespace std;

int main()
{
	int n, guess, times = 0;

	srand(time(0)); 
	n = rand() % 10 + 1;
	
	cout << "We kept a number between 1-10. Can you guess the number?\n\n";

	do
	{
		cout << "Your prediction: ";
		cin >> guess;
		times++;

		if (guess > n)
			cout << "Smaller\n";
		
		else if (guess < n)
			cout << "Bigger\n";
		
		else
			cout << "\nCongratulations! You found it on the " << times << " try\n";
	
	} while (guess != n);

	return 0;
}
