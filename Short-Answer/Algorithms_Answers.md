#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) O(n) or an error - n is not defined

b) O(n \* log(n))

c) O(n)

## Exercise II

To minimize the number of eggs broken in search of the floor from which eggs begin to be broken, I'd propose using a modified binary search algorithm. We would drop an egg from the middle floor. If the egg breaks, we move to the middle of the floors below us and try again. However, if the egg doesn't break, we move up a single floor and re-attempt. This way we arrive at floor F with minimal breakage.

If we use a standard binary search algorithm, we run the risk of breaking more eggs. Consider the case in which n = 100 and f = 26. With a standard implementation of binary search, we would break an egg at floor 50, not break an egg at floor 25, and then proceed to break several more eggs as we reduce the search scope to the ultimate destination of floor 26.

Under my proposed algorithm, under the same conditions (n = 100, f = 26), we would end up breaking only 2 eggs. One on the initial drop at floor 50, then no break at floor 25, and a second broken egg at floor 26.
