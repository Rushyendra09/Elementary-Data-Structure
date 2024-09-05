# C++ Basics - 01

# **Introduction**

# **What is C++?**

C++ is a widely used programming language that works on different types of computer systems.

It's used to create all sorts of software, from video games and mobile apps to operating systems and even the software that runs on cars and appliances.

Many tech interviews involve C++ due to its strong performance, making it a valuable skill to have.

# **C++ Basic Syntax**

```cpp
#include <iostream> 
    
int main() {
    // ... code ....
    return 0;
}
```

Here's a breakdown of each component:

- **#include <iostream>** is a standard library that provides basic input and output services.
- int main() { ... } where the program's execution starts.
- return 0; a return value of 0 from main typically indicates that the program executed successfully.

# **Things to note:**

- Every line in C++ is ending with semicolon ;.
- Do not forget to add the closing curly bracket } to actually end the main function.
- The **endl** keyword serves the purpose of moving to a new line
- **using namespace std** can simplify code writing by eliminating the need to prefix each line with std::.
- **#include <bits/stdc++.h>** contains all standard libraries of the header files. So if you include it in your code, then you need not have to include any other standard header files.

# **Comments in C++**

- Single line comment

```cpp
// Single line comment
```

• Multi-line Comment

```cpp
/*
Multi line comment 
*/
```

**Hello World Program**

```cpp
#include <bits/stdc++.h>
int main(){
    std::cout << "Hello World!"; // Output - Hello World!
    return 0;
}
```

This line uses the

**cout**

object to print the text "Hello World!" to the standard output.

It is part of the C++ Standard Library's input/output stream (

**iostream**

) and is used for output operations.

# **Input and Output in C++**

```cpp
#include <bits/stdc++.h>
using namespace std;

int main(){
    int a;
    cin >> a; // Input - 5
    cout << a*5 << endl; // Output - 25
    return 0;
}
```

**String as input**

```cpp
#include <bits/stdc++.h>
using namespace std;

int main(){
    string s;
    cin >> s; // Input - HelloWorld
    cout << s << endl; // Output - HelloWorld

    return 0;
}
```

**Example - Addition of Two numbers**

```cpp
#include <bits/stdc++.h>
using namespace std;

int main(){
    int a,b;
    cin >> a >> b; // Input - 2 5
    cout << "Sum: " << a+b << endl; // Output - Sum: 7
    return 0;
}
```

# **Data Types**

| **Data Type** | **Syntax Example** |
| --- | --- |
| int | int myVariable = 42; |
| float | float myFloat = 3.14; |
| double | double myDouble = 3.14159265359; |
| char | char myChar = 'A'; |
| std::string | std::string myString = "Hello, C++"; |
| long | long al = 1234567890L;` |
| long long | long long all = 123456789012345LL; |

```cpp
#include <bits/stdc++.h>
using namespace std;

int main(){
    int a = 42;
    float d = 5.51564;
    double e = 3.14159265359;
    char f = 'A';
    string g = "Hello, C++";
    long b = 1234567890L;
    long long c = 123456789012345LL;

    cout << "Integer a = " << a << " and size is " << sizeof(a) << " bytes" << endl;
    cout << "long b = " << b << " and size is " << sizeof(b) << " bytes" << endl;
    cout << "long long c = " << c << " and size is " << sizeof(c) << " bytes" << endl;
    cout << "float d = " << d << " and size is " << sizeof(d) << " bytes" << endl;
    cout << "double e = " << e << " and size is " << sizeof(e) << " bytes" << endl;
    cout << "char f = " << f << " and size is " << sizeof(f) << " bytes" << endl;
    cout << "string g = " << g << " and size is " << sizeof(g) << " bytes" << endl;
    return 0;
}
```

# **Sentence as input**

# **Using cin**

- ***Cin*** reads and accepts only the first word from the input

```cpp
#include <bits/stdc++.h>
using namespace std;

int main(){
    string s;
    cin >> s; // Input - Hello World
    cout << s; // Output - Hello
    return 0;
}
```

# **Using getline()**

To take a sentence as input, you can use

getline(cin, string_name)

```cpp
#include <bits/stdc++.h>
using namespace std;

int main(){
    string s;
    getline(cin, s); //Input - Hello World!
    cout << s; //Output - Hello World!
    return 0;
}
```

# **Conditional Statements**

Control statements in programming are like instructions that tell the computer what to do based on certain conditions. It's like making a decision. If something is true, do one thing; if it's false, do something else.

Following are the some decision-making statements:

# **if Statement:**

The if statement is a decision-maker that executes a block of code if a specified condition is true and skips it if the condition is false.

**Syntax**

```cpp
if(condition) 
{
   // Statements to execute if
   // condition is true
}
```

The if statement checks a condition, which produces a boolean (true or false) outcome, and executes the subsequent block of code if the condition is true, but not if it's false.

**Example**:

```cpp
#include <iostream>
using namespace std;

int main()
{
    int runs;
    cin >> runs; // Input - 100
    if (runs >= 100) {
        cout << "Century"; // Output - Century
    }
    return 0;
}
```

# **if-else Statement**

The if-else statement consists of two blocks, one for false expression and one for true expression.

**Syntax**

```cpp
if (condition)
{
    // Executes this block if
    // condition is true
}
else
{
    // Executes this block if
    // condition is false
}
```

The if statement runs the following block of code when the condition is true and executes the else block if the condition is false.

**Example**:

```cpp
#include <iostream>
using namespace std;

int main()
{
    int runs;
    cin >> runs; // Input - 90
    if (runs >= 100) {
        cout << "Century";
    }
    else{
        cout << "Not a Century"; // Output - Not a Century
    }
    return 0;
}
```

# **if-else-if Ladder**

Use if-else if statements to choose from multiple options, executed sequentially; when a true condition is found, it's executed, or the final else statement is executed if none are true.

**Syntax**

```cpp
if (condition)
{
    // statements
}
else if (condition)
{
    // statements
}
.
.
.
else{
    // statements
}
```

**Example**:

```cpp
#include <iostream>
using namespace std;
      
int main()
{
    int runs;
    cin >> runs; // Input - 25
    if (runs >= 100) {
        cout << "Century";
    }
    else if(runs >= 50){
        cout << "Half Century";
    }
    else{
        cout << "Less than 50"; // Output - Less than 50
    }
    return 0;
}
```

# **Switch Statement**

The switch-case statement lets you choose between different code blocks based on a variable's value, providing an alternative to a series of if-else if checks.

**Syntax**

```cpp
switch (expression) {
    case value1:
        statements;
    case value2:
        statements;
    ....
    ....
    default:
        statements;
}
```

**Example**:

```cpp
#include <iostream>
using namespace std;
    
int main() {
    int monthNumber;
    cin >> monthNumber; // Input - 8
    switch (monthNumber) {
        case 1:
            cout << "January" << endl;
            break;
        case 2:
            cout << "February" << endl;
            break;
        case 3:
            cout << "March" << endl;
            break;
        case 4:
            cout << "April" << endl;
            break;
        case 5:
            cout << "May" << endl;
            break;
        case 6:
            cout << "June" << endl;
            break;
        case 7:
            cout << "July" << endl;
            break;
        case 8:
            cout << "August" << endl; // Output - August
            break;
        case 9:
            cout << "September" << endl;
            break;
        case 10:
            cout << "October" << endl;
            break;
        case 11:
            cout << "November" << endl;
            break;
        case 12:
            cout << "December" << endl;
            break;
        default:
            cout << "Invalid input!" << endl;
            break;
    }
    
    return 0;
}
```
