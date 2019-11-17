# zadachi3



using System;

namespace crops
{
    class Program
    {
        static void Main(string[] args)
        {
            double areaVineyard = double.Parse(Console.ReadLine());
            double grapePerSqMeter = double.Parse(Console.ReadLine());
            double wantedliters = double.Parse(Console.ReadLine());
            double workers = double.Parse(Console.ReadLine());

            double grape = areaVineyard * grapePerSqMeter;
            double litri = grape * 0.4;
            double liters = litri / 2.5;            
            double ostatyk = liters - wantedliters;
            double ostavashtilitri = wantedliters - liters;
            double vinozarabotnik = ostatyk / workers;

            if (liters < wantedliters)
            {
                Console.WriteLine($"It will be a tough winter! More {Math.Floor(ostavashtilitri)} liters wine needed.");
            }
            else if (liters >= wantedliters)
            {
                Console.WriteLine($"Good harvest this year! Total wine: {Math.Ceiling(liters)} liters.");
                Console.WriteLine($"{Math.Ceiling(ostatyk)} liters left -> {Math.Ceiling(vinozarabotnik)} liters per person.");
            }
            
        }
    }
}





