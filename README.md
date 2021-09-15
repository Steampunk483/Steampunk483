/*
GitHub_bit: A haighly sarcastic intro for Steampunk483's GitHub Page. I dare you to compile it.

Do it. I know you want to.

Function wait() shamelessly "borrowed" from Prof. S's lab template, because I'm too lazy to figure it out myself.
As Picasso said, "Good artists borrow, great artists steal." 

But don't plagiarize, kids. That's bad.
Always cite relevant sources.
*/

#include <iostream>
#include <string>

using namespace std;
void wait()
{
	//The following if-statement checks to see how many characters are in cin's buffer
	//If the buffer has characters in it, the clear and ignore methods get rid of them.
	if (cin.rdbuf()->in_avail() > 0) //If the buffer is empty skip clear and ignore
	{
		cin.clear();
		cin.ignore(numeric_limits<streamsize>::max(), '\n'); //Clear the input buffer 
	}
	char ch;
	cout << "Press the Enter key to close the program.";
	cin.get(ch);
}

int main() {
	string userHandle = "@Steampunk483";
	string interests = "Coding, music, game development";
	string currentlyLearning = "Computer engineering";
	bool tryingToContact;

	cout << "Hello! You have found " << userHandle << "'s GitHub page!" << endl;
	cout << userHandle << "'s interests include: " << interests << "." << endl;
	cout << userHandle << "'s current field of study is: " << currentlyLearning << endl << endl << endl;

	cout << "Are you trying to contact " << userHandle << "?" << endl << "1 for yes, 0 for no." << endl;
	cin >> tryingToContact;

	if (tryingToContact == 1) {
		cout << endl << "Don't." << endl;

	}
	else {
		cout << endl << "Congratulations! You made a good decision with your life!" << endl << "Keep up the good work!" << endl << endl;
	}

	wait();
}
