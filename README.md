# Experiment 8

**Aim:** <br>
To study and implement C++ 2D Array - Matrices<br>
<br>
**Theory:** <br>

A 2D array in C++ can be defined as a data structure that deals with two-dimensional grid formats such as matrices wherein every single element is well identified by two indices: one for rows and another one for columns. It is similar to an array composed of other arrays.<br>

A two-dimensional array could be declared using the syntax type arrayName[rows][columns]; For instance, int matrix[3][4]; indicates three rows by four columns. All its members occupy successive positions in memory meaning they are laid out linearly following row-major order scheme hence it makes it different from accessing them through single index only but rather via two indexes.They may be initialized while being declared. For static arrays they require listing down values enclosed in nested braces whereas dynamic arrays size calculation occurs at run-time stage hence this involves dynamic allocation using new’s keyword and deallocation using delete’s keyword in C++.Elements can be accessed using their respective row and column indexes. The iteration uses mostly a two-fold loop: the outer one is run for rows while the inner one does columns. It enables you to treat or manipulate one element of an entire array.

<br>

**Code:** <br>

a.<br> 
```
# include<iostream>
using namespace std;
int main()
{
    //matrix input and display
    int a[2][2];
    int i,j;
    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }

    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<a[i][j]<<" ";
        }
        cout<<endl;
    }

}
```

<br>

b. <br>
```
# include<iostream>
using namespace std;
int main()
{

    int a[2][2];
    int b[2][2];
    int s[2][2];
    int i,j,r = 0,c=0;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            s[i][j] = a[i][j] + b[i][j];
        }
    }

    cout<<"Sum: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<s[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}
```
<br>

c. <br>
```
# include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0,s = 0;
    int a[r][c];
    int b[r][c];
    int p[r][c];
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
for (int i = 0; i < r; ++i) 
{
        for (int j = 0; j < r; ++j) 
        {
            p[i][j] = 0;
            for (int k = 0; k <c; ++k) 
            {
                p[i][j] += a[i][k] * b[k][j];
            }
        }
}

    cout<<"Product: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<p[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}
```
<br>

d. <br>
```
# include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0;
    int a[r][c];
    int da = 0;
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int i = 0; i < r; i++) 
    {
        da = da + a[i][i];
    }

cout<<"Diagonal Sum: "<<da<<endl;


}
```
<br>

e. <br>
```
# include<iostream>
using namespace std;
int main()
{

    int a[2][2];
    int i,j,r = 0,c=0;
    bool eqr = true;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int j = 0; j < c; j++) 
    {
        if (a[0][j] != a[1][j]) 
        {
            eqr = false;
            break;
        }
    }
    cout<<"Row equality: "<<eqr;
}
```
<br>

**Outputs:** <br>
a.<br>
![8a](https://github.com/user-attachments/assets/f3353732-8f1c-4928-89d0-a9f8afb7e1b9)

<br>
b.<br>
![8b](https://github.com/user-attachments/assets/d939b951-20cd-4f71-b8a0-5a66415ca9bf)

c.<br>
![8c](https://github.com/user-attachments/assets/249c3381-f9ab-46c4-9ac4-c7aac70b0e64)

<br>
d.<br>
![8d](https://github.com/user-attachments/assets/e0836dcc-010e-432e-8d3d-7d862af73826)

<br>
e.<br>
![8e](https://github.com/user-attachments/assets/cf227cde-79cd-4836-88da-499eca32291b)

<br>

**Conclusion:** <br>
&#8594; We learnt the use case of 2D arrays in C++. <br>
&#8594; We learnt how to perform basic operations on a 2-D array in C++. <br>
<br>
*******
