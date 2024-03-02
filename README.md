<h1>Calculator for Louies Lawn Care service</h1>

<h2>Description</h2>
This program demonstrates the use of Variables and simple arithmetic to create a calculator for Louie's Lawncare and Tree Trimming service. 
<br />


<h2>Used to create:</h2>

- <b>Visual Studios</b> 


<img src="https://i.imgur.com/a9r7PN2.png" height="80%" width="80%" alt="Disk Sanitization Steps]"/>



    Code:
    using System;
    using System.Collections.Generic;
    using System.Linq;using System.Text;
    using System.Threading.Tasks;using System.Web.Services.Description;
    namespace Program1{
    class Program
    {
        static void Main(string[] args)

        {
            double flatLaborCost = 75; //Flat Labor cost
            Console.WriteLine("Welcome to Louie's Lawncare and Tree Trimming Service Calculator!");
            Console.WriteLine("Enter Client Name:");
            string customerName = (Console.ReadLine());//Customer Input Name
            Console.WriteLine("Enter the Width of the Lawn (in feet)");
            double lawnWidth = double.Parse(Console.ReadLine());//Customer Input Width of Lawn
            Console.WriteLine("Enter the Length of the Lawn (in feet)");
            double lawnLength = double.Parse(Console.ReadLine());// customer Input Length of Lawn
            Console.WriteLine("Enter the Color of Mulch for the Flowerbed:");
            string mulchColor = (Console.ReadLine());// Customer input Color of Mulch
            Console.WriteLine("Enter the Length of Flowerbed (in feet)");
            double flowerLength = double.Parse(Console.ReadLine());// Customer Input Length of Flowerbed in feet
            Console.WriteLine("Enter the Width of the Flowerbed (in feet)");
            double flowerWidth = double.Parse(Console.ReadLine());// Customer Input Width of Flowerbed in feet
            Console.WriteLine("Enter the Height of the Mulch layer (in inches)");
            double flowerHeight = double.Parse(Console.ReadLine());// Customer Input Height of Mulch Layer in inches
            Console.WriteLine("Trim Your Trees? (1 for YES, 0 for NO)");
            int trimTree = int.Parse(Console.ReadLine());
            double areaLawn1 = lawnLength * lawnWidth;
            double areaLawn = areaLawn1 / 9; //Calculate area of lawn in yards
            double mowingCost = areaLawn * 20;// Cost of Mowing Lawn
            double flowerHeight2 = flowerHeight * .08333; 
            double areaFlower = flowerLength * flowerWidth; //Flower area
            double areaFlower1 = areaFlower * flowerHeight2; // Flowerbed Area of Flowber bed in feet
            double areaFlower2 = areaFlower / 27; // Flowerbed Cubic yds of Mulch needed
            double mulchCost = .1 * areaFlower2; //MulchCost
            
            if (trimTree == 1)// If Customer chooses trim tree cost (1) $550 is charged
            {
                double trimTreeCost = 550;
                double totalCost = mowingCost + mulchCost + trimTreeCost + flatLaborCost;//total cost
                Console.WriteLine("Client Name: " + customerName + "\nArea of Lawn: " + areaLawn.ToString("0.00") +" sq yds\nLawn Mowing Cost: " + "{0:c}", mowingCost);
                Console.WriteLine("Area of Flowerbed: " + areaFlower2.ToString("0.00") + " cubic yds" + "\nMulch Color: " + mulchColor);
                Console.WriteLine("Mulching Cost: " + "{0:c}", mulchCost);
                Console.WriteLine("Tree Trimming Cost:" + "{0:c}", trimTreeCost);
                Console.WriteLine("The Total Cost of Labor is: " + "{0:c}", totalCost);
                string endProgram = (Console.ReadLine());
            }
            else
            {
                double trimTreeCost = 0;// If customer chooses no trim tree (0) cost is $0
                double totalCost = mowingCost + mulchCost + trimTreeCost + flatLaborCost;//Total cost
                Console.WriteLine("Client Name: " + customerName + "\nArea of Lawn: " + areaLawn.ToString("0.00") + " sq yds\nLawn Mowing Cost: " + "{0:c}", mowingCost);
                Console.WriteLine("Area of Flowerbed: " + areaFlower2.ToString("0.00") + " cubic yds" + "\nMulch Color: " + mulchColor);
                Console.WriteLine("Mulching Cost: " + "{0:c}", mulchCost);
                Console.WriteLine("Tree Trimming Cost:" + "{0:c}", trimTreeCost);
                Console.WriteLine("The Total Cost of Labor is: " + "{0:c}", totalCost);
                string endProgram = (Console.ReadLine());
            }

        }
    }
}

  


 <br/>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
