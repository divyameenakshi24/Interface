# Interface

## Aim:
To Develop a small bank application by declaring deposit() and withdrawal() as abstract methods in the interface.  Get the choice from the user whether to perform withdrawal or deposit operation. After the operation completes, display the balance amount

## Algorithm:
### step 1: 
Create an interface.

### step 2:
Create a child class.

### step 3:
Declare 2 functions deposit() and withdrawal() as abstract methods in the interface.

### step 4:
Create those 2 functions in the child class and perform respective operation.

### step 4:
Use while loop and and switch case to Get the choice from the user whether to perform withdrawal or deposit operation.

### step 5:
After performing the functions display the remaining balance of the user.

## Program:
```c#

using System;
public interface Bank
{
    void deposit();
    void withdrawal();
}

public class Example : Bank
{
    int amount, ch, balance = 5000;
    public Example()
    {
        Console.WriteLine("1.Deposit\n2.Withdrawal");
        ch = Convert.ToInt32(Console.ReadLine());
        if (ch == 1)
        {
            deposit();
        }
        else
        {
            withdrawal();
        }
    }
    public void withdrawal()
    {
        int amount = Convert.ToInt32(Console.ReadLine());
        balance -= amount;
        Console.WriteLine(balance);
    }

    public void deposit()
    {
        int amount = Convert.ToInt32(Console.ReadLine());
        balance += amount;
        Console.WriteLine(balance);
    }
}

public class Hello
{
    public static void Main()
    {
        Example c = new Example();
        c.deposit();
        c.withdrawal();
    }
}
```

## Output:
![image](https://user-images.githubusercontent.com/75235402/172893530-ce300baa-8828-4a4c-b050-a9e7398cd5b4.png)


## Result:
C# program to develop a bank application using interface is implemented successfully.
