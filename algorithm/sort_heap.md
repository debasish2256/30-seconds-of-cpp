//The sort_heap( ) is an STL algorithm which sorts a heap within the range specified by start and end. Sorts the elements in the heap range [start, end) into ascending order.
/*
void sort_heap( RandIter start, RandIter end );
{
    while (start != end)
        std::pop_heap(start, end--);
}
*/

// CPP program
// std::sort_heap 
#include <iostream> 
#include <algorithm> 
#include <vector> 
using namespace std; 
int main() 
{ 
	vector<int> v = {8, 6, 2, 1, 5, 10}; 

	make_heap(v.begin(), v.end()); 

	cout << "heap: "; 
	for (const auto &i : v) { 
	cout << i << ' '; 
	} 

	sort_heap(v.begin(), v.end()); 

	std::cout <<endl<< "now sorted: "; 
	for (const auto &i : v) {												 
		cout << i << ' '; 
	} 
	std::cout <<endl; 
} 
