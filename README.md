using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        Console.WriteLine("Inserisci il testo della canzone:");
        string testo = Console.ReadLine();

        Console.WriteLine("Inserisci le parole da sostituire con spazi vuoti (separate da una virgola):");
        string inputParole = Console.ReadLine();
        
        // Separiamo le parole in un array
        string[] paroleDaRimuovere = inputParole.Split(',');

        // Sostituiamo ogni parola con "____"
        foreach (string parola in paroleDaRimuovere)
        {
            testo = testo.Replace(parola.Trim(), "____");
        }

        Console.WriteLine("\nTesto con spazi vuoti:");
        Console.WriteLine(testo);
    }
}
