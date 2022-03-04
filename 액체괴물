#include<iostream>
#include<queue>
using namespace std;

//액괴만들기
//액괴 갯수 받아서 두마리씩 선택하여 합쳐줄때, 액괴 a,b를 선택할시 a+b 초의 시간이 소요된다.
//모든 액괴를 하나로 합칠때 최소시간을 구하시오.

int main()
{
	
	int n;
	cin >> n;

	//적은수~ 큰수
	priority_queue<int, vector<int>, greater<int>> pq;
	vector<int> time;
	for (int i = 0; i < n; i++) {
		int input;
		cin >> input;
		pq.push(input);
	}

	while(pq.size() >1){
		int now = pq.top(); pq.pop();
		int next = pq.top(); pq.pop();
		pq.push(now + next);
		time.push_back(now + next);
	}

	int ans = 0;
	for (int i = 0; i < time.size(); i++) {
		ans += time[i];
	}
	cout << ans;
	return 0;
}

//예시 입출력
//input 1 :
//4 
//3 1 9 7
//output 1 : 
//35
//
//input 2 : 
//4
//3 1 11 8
//
//output 2: 
//39
//
//
//input 3 : 
//4
//50 50 50 50 
//
//output 3 : 
//400
