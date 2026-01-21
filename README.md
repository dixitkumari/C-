# C++
**QUESTION 1**
#include <iostream>
using namespace std;

// Global variable
int gVar = 100;

int main()
{
    // Local variable inside main (stack)
    int lVar = 200;

    // Dynamic memory allocation (heap)
    int* dVar = new int;
    *dVar = 300;

    cout << "Address of Global Variable (Data Segment): " << &gVar << endl;
    cout << "Address of Local Variable  (Stack)       : " << &lVar << endl;
    cout << "Address of Dynamic Variable (Heap)       : " << dVar << endl;

    // Release heap memory
    delete dVar;

    return 0;
}

**OUTPUT**
<img width="674" height="315" alt="image" src="https://github.com/user-attachments/assets/0d5f0840-0d1d-40af-82c4-a08560910b63" />

**QUESTION2**
#include <iostream>
using namespace std;

// Function that returns the square of a number
int square(int x)
{
    return x * x;
}

int main()
{
    int num = 5;

    // 1. Normal function call
    cout << "Normal function call: " << square(num) << endl;

    // 2. Function pointer call
    int (*funcPtr)(int);   // declare function pointer
    funcPtr = square;      // assign function address

    cout << "Function pointer call: " << funcPtr(num) << endl;

    return 0;
}

**OUTPUT**
<img width="466" height="186" alt="image" src="https://github.com/user-attachments/assets/e2a487c9-5113-4ce5-b644-0d69fb38902c" />

**QUESTION3**
#include <iostream>
using namespace std;

int main()
{
    int a = 50;        // variable
    int* p = &a;      // pointer storing address of a

    cout << "Value of variable a: " << a << endl;
    cout << "Address of variable a: " << &a << endl;
    cout << "Value stored in pointer p: " << p << endl;

    return 0;
}

**OUTPUT**
<img width="419" height="207" alt="image" src="https://github.com/user-attachments/assets/db47d8cf-0b2f-4619-b0a0-3666212344bd" />

**QUESTION 4:**
#include <iostream>
using namespace std;

int main()
{
    int a = 25;        // original variable
    int* p = &a;      // pointer storing address of a
    int b;            // third variable

    // Copy value of a into b using dereferencing
    b = *p;

    cout << "Value of a: " << a << endl;
    cout << "Address stored in pointer p: " << p << endl;
    cout << "Value copied into b using dereferencing: " << b << endl;

    return 0;
}

**OUTPUT**
<img width="510" height="225" alt="image" src="https://github.com/user-attachments/assets/a23ede1c-6084-4dc5-b988-503fbff18b0f" />

**QUESTION 5:**
#include <iostream>
using namespace std;

int main()
{
    int x = 5;        
    int* p = &x;

    *p = 10;   // semicolon added

    cout << x;

    return 0;
}

**OUTPUT**
<img width="342" height="193" alt="image" src="https://github.com/user-attachments/assets/145221f3-8afd-41fe-9aac-ae6d3e067e8a" />

**QUESTION6:**
#include <iostream>
using namespace std;

int main()
{
    int a= 1, b=2;        
    int *p = &a;
    p=&b;
    

    *p = 5;  

    cout << a <<""<<b;

    return 0;
}
**OUTPUT**
<img width="431" height="185" alt="image" src="https://github.com/user-attachments/assets/d6d2cf9f-18d7-49ac-bdc3-72449c691760" />





**QUESTION 7**
#include <iostream>
using namespace std;

int main()
{
    int x = 10;        
    int *p = &x;
    int **pp = &p;
    **pp = 20;
    
    cout << x;

    return 0;
}
**OUTPUT**
<img width="411" height="157" alt="image" src="https://github.com/user-attachments/assets/d3e51a67-26c3-4efb-918b-d693ac066df9" />


**QUESTION 8**
#include <iostream>
using namespace std;

int main()
{
    int a[5]= {2,4,6,8,10};     
    int *p = a;
  

    cout << *p++<<"" ;
    cout<<*p ;

    return 0;
}

**OUTPUT**
<img width="587" height="177" alt="image" src="https://github.com/user-attachments/assets/b9a7c49a-12cb-48fa-a78b-a1eb03462e1a" />

**QUESTION 9**
#include <iostream>
using namespace std;

void swap(int *a, int *b)
{
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

int main()
{
    int x, y;

    cout << "Enter two numbers: ";
    cin >> x >> y;

    cout << "Before swapping:\n";
    cout << "x = " << x << ", y = " << y << endl;

    swap(&x, &y);

    cout << "After swapping:\n";
    cout << "x = " << x << ", y = " << y << endl;

    return 0;
}

**OUTPUT**
<img width="551" height="246" alt="image" src="https://github.com/user-attachments/assets/a2832259-4e14-4190-8bc6-09bfcfe2652d" />

**QUESTION 10**
#include <iostream>
using namespace std;

int main()
{
    int *ptr;          // Pointer declaration

    ptr = new int;     // Dynamic memory allocation

    *ptr = 10;         // Modify value through pointer

    cout << "Value stored in dynamic integer: " << *ptr << endl;

    *ptr = 25;         // Modify again
    cout << "Modified value: " << *ptr << endl;

    delete ptr;        // Properly delete memory

    ptr = nullptr;    // Avoid dangling pointer

    return 0;
}

**OUTPUT**
<img width="507" height="293" alt="image" src="https://github.com/user-attachments/assets/842b5478-01dd-4b56-bc47-e784b92f8a88" />

**QUESTION 11**
#include <iostream>
using namespace std;

int main()
{
    int a[] = {1, 2, 3, 4, 5}; 
    int *p = a;                

    cout << *p++ << " ";        
    cout << (*p)++ << " ";    
    cout << ++*p << " ";       
    cout << *p << "\n";       

    for(int i = 0; i < 5; i++)  
        cout << a[i] << " ";    

    return 0;
}

**output**
<img width="487" height="181" alt="image" src="https://github.com/user-attachments/assets/9e7cbe5f-cfef-40f2-a00d-0cffa085f3ef" />







