# Using of "const keyword" in C++
<font size="2"> This is my text number 2 </font>

<font size="4">**1) Constant Variables in C++**</font>

<font size="3">We use const to declare that the variable has constant value,and should be initialized while it is declared.

Example:</font>
````
int main
{
    const int j = 20;
    const int k = j + 15;     // works fine
    i++;     // this leads to Compile time error  // you can't change the value after declartion 
}
````


<font size="4">**2)Pointers with const keyword in C++**</font>

<font size="3">we can declare it in two ways, either we can apply const to what the pointer is pointing to, 
or we can make the pointer itself a constant.

Example:</font>
````
int main{
//1)Pointer to a const variable
const int* x = new int (5);
char const* y = new char ('k'); //Also it could be written this way

//2)const Pointer
int w = 1;
int* const z = &w; //We can't change the pointer, which means it will always point to the variable x but can change the value that it points to, by changing the value of x.
    const int * const s =new int (5) ;  // We can also have a const pointer pointing to a const variable.
    }
````


<font size="4">**3) const Function Arguments and Return types**</font>

<font size="3">We can make the return type or arguments of a function as const. 
Then we cannot change any of them.

Example:</font>
````
void f(const int i)
{
    i++;    // error
}

//If a function has a non-const parameter, it cannot be passed a const argument while making a call.//

void t(int*) 
{ 
    // function logic 
    
} //If we pass a const int* argument to the function t, it will give error.

//But, a function which has a const type parameter, can be passed a const type argument as well as a non-const argument.//

void x(const int*) 
{
    // function logic
    
}//This function can have a int* as well as const int* type argument.

const int g()
{
    return 1;
}

int main()
{
    const int j = g(); // j= 1
    int k = g();       // k = 1
}
````


<font size="4">**4) Defining Class Data members as const**</font>

<font size="3">These are data variables in class which are defined using const keyword. 
They are not initialized during declaration. Their initialization is done in the constructor.

Example:</font>
````
class set
{
    const int i;
public:
    set(int x):i(x)
    {
        cout << "i value is: " << i<< endl;
    }
}; // i is a constant data member, it is initialized with each object using the constructor. And once initialized, its value cannot be changed.



int main() {
    set j(10);
    set k(20);
}
````

<font size="4">**5) Defining Class Object as const**</font>

<font size="3">When an object is declared or created using the const keyword, its data members can never be changed, 
during the object's lifetime.

Example:</font>
````
if in //the class set defined above, we want to define a constant object, we can do it like://

const set r(30);
````

# Using of "& operator" in C++

<font size="4">**1) Logical Operator**</font>

<font size="3">Logical AND. True only if all the operands are true.

Example:</font>
````
if(expression1 && expression2){

/* function
   body*/

}
````

<font size="4">**2) reference Operator**</font>
<font size="3">represents memory address of the operand

Example:</font>
````
int x=7;
cout<<&x; // will print address of x
````
