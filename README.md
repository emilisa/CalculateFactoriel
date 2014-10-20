CalculateFactoriel
==================
using System;

using System.Collections.Generic;

using System.Numerics;

class CalculateFactoriel

{

    static void Main()
    
    {
        Console.Title = "CalculateFactoriel";
        int numberToCalculate;
        bool tryParse = int.TryParse(Console.ReadLine(), out numberToCalculate);

        if (tryParse == false)
        {
            Console.WriteLine("Please type number");
            Console.ReadKey();
        }

        else
        {
            BigInteger result = 1;

            for (int i = 1; i <= numberToCalculate; i++)
            {
                result *= i;
            }

            Console.Clear();
            Console.WriteLine("The factoriel of the number {0} is:", numberToCalculate);
            Console.ForegroundColor = ConsoleColor.Cyan;
            Console.WriteLine(result);
            Console.ResetColor();
            Console.ReadKey();
        }
    }
}
