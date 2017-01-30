# DictionaryBricks
Homework dictionary
VV Code start VV




using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace CAdictionary
{
    class Program
    {
        static void Main(string[] args)
        {

            Bricks brickstype1 = new Bricks()
            {
                ID = 12,
                weight = 2,
                amount = 100
            };

            Bricks brickstype2 = new Bricks()
            {
                ID = 25,
                weight = 5,
                amount = 70
            };

             Bricks brickstype3 = new Bricks()
             {
                 ID = 31,
                 weight = 7,
                 amount = 90
             };

            Dictionary<int,Bricks> dictionaryBricks = new Dictionary<int, Bricks>();
            dictionaryBricks.Add(brickstype1.ID, brickstype1);
            dictionaryBricks.Add(brickstype2.ID, brickstype2);
            dictionaryBricks.Add(brickstype3.ID, brickstype3);

        

            Bricks brickstype31 = dictionaryBricks[31];

            foreach(KeyValuePair<int, Bricks> BricksKeyValuePair in dictionaryBricks)
            {
                Console.WriteLine("Key = {0}", BricksKeyValuePair.Key);
                Bricks brick = BricksKeyValuePair.Value;
                Console.WriteLine("ID = {0}, Weight = {1}, Amount = {2}", brick.ID, brick.weight, brick.amount );
                Console.WriteLine("______________________________________________");
            
            }

            Console.ReadKey();
        }
    }
    public class Bricks
    {
        public int ID { get; set; }
        public int weight { get; set; }
        public int amount { get; set; }
    }
}
