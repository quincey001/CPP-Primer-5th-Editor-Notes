# 1. Namespace using declarations

The program have explicitly indicated that each library name we use in the std namespace. std:cin , std::cout, These examples use the scope operator :: which says that the compiler should look in the scope of the left-hand operand for the name of the right-hand operand.

There is another safest way to referencing a namespace in c++, which is a using declaration.

Form: using namespace::name;

```cpp
#include <iostream>
using std::cin;

int main()
{
	int i;
	cin >> i; // cin is a synonym for std:cin
	cout << i; // error: std::cout is not declared 
	std::cout << i; // explicitly use cout from the namespace std
	return 0;
}
```