#include <stdio.h>

// Recursive C function to demonstrate the solution of the Tower of Hanoi problem
void towerOfHanoi(int n, char from_rod, char to_rod, char aux_rod)
{
    if (n == 1)
    {
        printf("\n Shift disk 1 from peg %c to peg %c", from_rod, to_rod);
        return;
    }
    towerOfHanoi(n-1, from_rod, aux_rod, to_rod);
    printf("\n Shift disk %d from peg %c to peg %c", n, from_rod, to_rod);
    towerOfHanoi(n-1, aux_rod, to_rod, from_rod);
}

int main()
{
    int n = 4; // Setting the count of disks
    towerOfHanoi(n, 'A', 'C', 'B'); // Here, A, B, and C represent the pegs' identifiers
    return 0;
}
