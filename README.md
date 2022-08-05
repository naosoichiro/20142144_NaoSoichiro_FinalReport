#include<iostream>
#include<vector>
#include<algorithm>
using namespace std;

struct TestPoint {
	int point;
	TestPoint(const int secondpoint) : point(secondpoint) {}
};

bool operator< (const TestPoint& i1, const TestPoint& i2) {
	return i1.point > i2.point;
}

int main() {
	vector<TestPoint>class1;
	class1.emplace_back(54);
	class1.emplace_back(94);
	class1.emplace_back(100);
	class1.emplace_back(43);
	class1.emplace_back(75);
	class1.emplace_back(67);
	class1.emplace_back(64);
	class1.emplace_back(85);
	class1.emplace_back(72);
	class1.emplace_back(63);

	sort(class1.begin(), class1.end());
	for (auto a : class1) {
		cout << ""<<a.point<<"\n";
	}
}
