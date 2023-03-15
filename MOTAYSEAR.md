Task1 :
the web works through a set of protocols and technologies that facilitate communication between computers.
The two primary protocols used on the web are the Hypertext Transfer Protocol (HTTP) and the Transmission Control Protocol/Internet Protocol (TCP/IP)
The client-server model is a computing architecture in which multiple clients communicate with a central server to access resources, data, or services. In this model, the client sends requests to the server using HTTP, and servers respond with the requested resources or error messages.
This model is the basis of the web as we know it now.

Task 2 : 

In Object-Oriented Programming a class is a template that defines the attributes (data members) and behaviors (methods) that objects of that class will have.
It is like a template or a blueprint that describes what an object should look like and what it can do.

An object is an instance of a class that is created at runtime.
It is a concrete entity that has a specific state and behavior as defined by its class.
An object is created by instantiating a class, and it can be used to perform operations, store data, and interact with other objects.

The  difference between a class and an object is that a class is a general concept while an object is a specific instance of that concept.
A class defines the properties and behaviors that an object will have, while an object is an instance of that class that has its own unique values for the properties defined by the class.
 a class is like a blueprint or a plan,

Task 3 : 

using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter the number of elements in the array: ");
        int n = int.Parse(Console.ReadLine());

        int[] arr = new int[n];

        for (int i = 0; i < n; i++)
        {
            Console.Write("Enter element {0}: ", i + 1);
            arr[i] = int.Parse(Console.ReadLine());
        }

        int largest = arr[0];
        int secondLargest = arr[0];

        for (int i = 1; i < n; i++)
        {
            if (arr[i] > largest)
            {
                secondLargest = largest;
                largest = arr[i];
            }
            else if (arr[i] > secondLargest && arr[i] != largest)
            {
                secondLargest = arr[i];
            }
        }

        Console.WriteLine("The second largest element in the array is: {0}", secondLargest);
    }
}


Task 4 :

using System;
using System.Linq;

class Program
{
    static void Main()
    {
        Console.Write("Enter a string: ");
        string input = Console.ReadLine();

        char firstNonRepeatingChar = input.FirstOrDefault(c => input.Count(x => x == c) == 1);

        if (firstNonRepeatingChar != default(char))
        {
            Console.WriteLine("The first non-repeating character is: {0}", firstNonRepeatingChar);
        }
        else
        {
            Console.WriteLine("There is no non-repeating character in the string.");
        }
    }
}
