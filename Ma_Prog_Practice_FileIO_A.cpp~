// Name: Mavey Ma
// Due: Thursday, October 22, 2015
// FILE I/O PROGRAM PRACTICE A, GITHUB
#include <iostream>
#include <fstream> //ALLOWS YOU TO READ AND WRITE TO FILES
#include <cstdlib>
#include <cctype> //toupper()
using namespace std;

int main()
{
    ifstream fin; //gba.txt
    ofstream fout; //result.txt
    ofstream foutCap; //capitalize.txt
    ofstream foutUp; //uppercase.txt
    string word;
    double average, sum = 0, count = 0;
    int length1 = 0, length2 = 0, length3 = 0, length4 = 0;
    int length5 = 0, length6 = 0, length7 = 0, length8 = 0;
    int length9 = 0, length10 = 0, length11orMore = 0;
    
    //OPEN SESAME, FILES!
    fin.open("gba.txt");
    fout.open("result.txt");
    foutCap.open("capitalize.txt");
    foutUp.open("uppercase.txt");
    
    //IN CASE FILE DOESN'T OPEN PROPERLY
    if (fin.fail())
    {
        cout << "ERROR OPENING INPUT FILE.\n";
        exit(1);
    }
    if (fout.fail())
    {
        cout << "ERROR OPENING INPUT FILE.\n";
        exit(1);
    }
    if (foutCap.fail())
    {
        cout << "ERROR OPENING INPUT FILE.\n";
        exit(1);
    }
    if (foutUp.fail())
    {
        cout << "ERROR OPENING INPUT FILE.\n";
        exit(1);
    }
    
    //LET'S READ IN THE gba.txt FILE WORD BY WORD
    while (fin >> word)
    {
        string copyWord = word;
        //1 DETERMINES THE AVERAGE NUMBER OF CHARACTERS PER WORD
        count++; //3 TOTAL NUMBER OF WORDS
        sum += word.length(); //TOTAL NUMBER OF CHARACTERS 
        //2 PROVIDE A COUNT OF THE NUMBER OF WORDS PER EACH LENGTH
        switch (word.length())
        {
            case 1: 
                length1++;
                break;
            case 2:
                length2++;
                break;
            case 3:
                length3++;
                break;
            case 4:
                length4++;
                break;
            case 5: 
                length5++;
                break;
            case 6:
                length6++;
                break;
            case 7:
                length7++;
                break;
            case 8:
                length8++;
                break;
            case 9:
                length9++;
                break;
            case 10:
                length10++;
                break;
            default:
                length11orMore++;
                break;
        }//END SWITCH   
        
        //4 CAPITALIZE ALL LETTERS IN gba.txt
        for (int ix = 0; ix < word.length(); ix++)
        {
            if (word[ix] >= 'a' && word[ix] <= 'z')
            {
                word[ix] -= 32;
                foutCap << word[ix];
            }
            else
            {
                foutCap << word[ix];
            }
        }//END FOR LOOP
        //4 INCLUDE SPACES BETWEEN EACH CAPITALIZED WORD
        //WRITE TO capitalize.txt
        foutCap << " ";
        
        //5 UPPERCASE FIRST LETTER OF EACH WORD IN  gba.txt
        char firstLetter = toupper(copyWord[0]);
        foutUp << firstLetter << copyWord.substr(1);
        //5 INCLUDE SPACES BETWEEN EACH CAPITALIZED WORD
        //WRITE TO uppercase.txt
        foutUp << " ";
        
    }//END WHILE
    //1 PRINTS RESULT TO result.txt
    average = sum / count;
    fout << "average characters per word: " << average << endl;
    //2 PRINTS RESULT TO result.txt
    fout << length1 << " words of length 1\n";
    fout << length2 << " words of length 2\n";
    fout << length3 << " words of length 3\n";
    fout << length4 << " words of length 4\n";
    fout << length5 << " words of length 5\n";
    fout << length6 << " words of length 6\n";
    fout << length7 << " words of length 7\n";
    fout << length8 << " words of length 8\n";
    fout << length9 << " words of length 9\n";
    fout << length10 << " words of length 10\n";
    fout << length11orMore << " words of length 11 or longer\n";
    //3 TOTAL NUMBER OF WORDS IN gba.txt. PRINTS RESULT TO result.txt
    fout << "Total number of words: " << count << endl;
    
    //CLOSE FILES
    fin.close();
    fout.close();
    foutCap.close();
    foutUp.close();
    return 0;
}//END INT MAIN
