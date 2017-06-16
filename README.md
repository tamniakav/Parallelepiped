using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam5
{
    class Exam5
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            char dot = '.';
            int j = 0;

            Console.WriteLine("+{0}+{1}", new string('~', n - 2), new string('.', (2 * n) + 1));

            for (int i = 1; i <= (2 * n) + 1; i++)
            {
                Console.WriteLine("|{0}\\{1}\\{2}", new string(dot, j), new string('~', n - 2), new string('.', (3 * n + 1) - (3 + (n - 2) + j)));
                j++;
            }

            int f = 0;

            for (int i = 1; i <= (2 * n) + 1; i++)
            {
                Console.WriteLine("{0}\\{1}|{2}|", new string(dot, f), new string('.', (3 * n + 1) - (3 + (n - 2) + f)), new string('~', n - 2));
                f++;
            }
            Console.WriteLine("{0}+{1}+", new string('.', (2 * n) + 1), new string('~', n - 2));
        }
    }
}
