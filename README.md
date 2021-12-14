# codeforces--3A--Shortest-path-of-king

**----->Question:**

The king is left alone on the chessboard. In spite of this loneliness, he doesn't lose heart, because he has business of national importance. For example, he has to pay an official visit to square t. As the king is not in habit of wasting his time, he wants to get from his current position s to square t in the least number of moves. Help him to do this.


In one move the king can get to the square that has a common side or a common vertex with the square the king is currently in (generally there are 8 different squares he can move to).

Input
The first line contains the chessboard coordinates of square s, the second line — of square t.

Chessboard coordinates consist of two characters, the first one is a lowercase Latin letter (from a to h), the second one is a digit from 1 to 8.

Output
In the first line print n — minimum number of the king's moves. Then in n lines print the moves themselves. Each move is described with one of the 8: L, R, U, D, LU, LD, RU or RD.

L, R, U, D stand respectively for moves left, right, up and down (according to the picture), and 2-letter combinations stand for diagonal moves. If the answer is not unique, print any of them.

Examples
inputCopy
a8
h1
outputCopy
7
RD
RD
RD
RD
RD
RD
RD




**------> Code:**


#include<bits/stdc++.h>
using namespace std;

int main(){
	string s,t;
	cin>>s>>t;
	
	cout<<max(abs(s[0]-t[0]),abs(s[1]-t[1]))<<endl;
	
	while(s!=t){
		if(s[0]<t[0]){
			cout<<"R";
			s[0]=s[0]+1;
		}else if(s[0]>t[0]){
			cout<<"L";
			s[0]=s[0]-1;
		}
		
		if(s[1]>t[1]){
			cout<<"D";
			s[1]=s[1]-1;
		}else if(s[1]<t[1]){
			cout<<"U";
			s[1]=s[1]+1;
		}
		
		cout<<endl;
	}
	
	return 0;
}
