# Exp03-Constructor
## Aim: 
To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.

## Algorithm:
### Step1: 
Initialize the program with the system library.
### Step2:
Define the Employee Class and set it as public.
### Step3:
Define the variables.
### Step4:
Write a parameterized constructor under the class Employee.
### Step5:
Define a function to calculate the salary.
### Step6:
Define the display() function to print the output.

## Program:
```C#
using System;
namespace EX03
{    public class Employee
    {
        public string name, designation;
        public int basicSalary, noofexp, insurance;
        public double hra, ta, grosspay;
        public Employee(string name, string designation, int bsalary, int noofexp, int insurance)
        {
            this.name = name;
            this.designation = designation;
            this.basicSalary = bsalary;
            this.noofexp = noofexp;
            this.insurance = insurance;

            hra = (0.1) * basicSalary;
            ta = (0.2) * basicSalary;
            grosspay = (0.15) * basicSalary;
        }
        public double salary()
        {
            return basicSalary + hra + ta - insurance - grosspay;
        }
        public void Display()
        {
            Console.WriteLine("\nEmployee Name: " + name);
            Console.WriteLine("Employee Designation: " + designation);
            Console.WriteLine("Employee No of Experience: " + noofexp);
            Console.WriteLine("Employee Basic Salary: " + basicSalary);
            Console.WriteLine("Employee HRA: " + hra);
            Console.WriteLine("Employee TA: " + ta);
            Console.WriteLine("Employee GROSSPAY: " + grosspay);
            Console.WriteLine("Employee Salary: " + salary());
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            Employee emp1 = new Employee("Shyam Kumar A", "Data Analyst", 80000, 5, 6000);
            emp1.Display();
            Employee emp2 = new Employee("Jaison", "Frontend Developer", 75000, 6, 5000);
            emp2.Display();
            Console.ReadLine();
        }
    }
}

```

## Output:
![image](https://github.com/ShyamKumar-AI-DS/Exp03-Constructor/assets/93427182/9dc356a3-244d-43ba-bff5-71df2261050d)

## Result:
Thus, a C# program is written to calculate the salary of an employee using a constructor is implemented and the output is verified.
