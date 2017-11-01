# Baskets-of-Gold-Coins

Baskets of Gold Coins

Problem Description

You are given N baskets of gold coins. The baskets are numbered from 1 to N. In all except one of the baskets, each gold coin weighs w grams. In the one exceptional basket, each gold coin weighs w-d grams. A wizard appears on the scene and takes 1 coin from Basket 1, 2 coins from Basket 2, and so on, up to and including N-1 coins from Basket N-1. He does not take any coins from Basket N. He weighs the selected coins and concludes which of the N baskets contains the lighter coins. Your mission is to emulate the wizard's computation.

Input

The input file will consist of one or more lines; each line will contain data for one instance of the problem. More specifically, each line will contain four positive integers, separated by one blank space. The first three integers are, respectively, the numbers N, w, and d, as described above. The fourth integer is the result of weighing the selected coins.

N will be at least 2 and not more than 8000. The value of w will be at most 30. The value of d will be less than w.

Output

For each instance of the problem, your program will produce one line of output, consisting of one positive integer: the number of the basket that contains lighter coins than the other baskets.

Sample Input

10 25 8 1109 10 25 8 1045 8000 30 12 959879400

Sample Output

2 10 50

代码：

#include<stdio.h>

int main()

{

    int a,b,c,d,sum;
    
    while(scanf("%d%d%d%d",&a,&b,&c,&d)!=EOF)
    
    {
    
        sum=a*(a-1)/2*b;
        
        if(sum==d)
        
            printf("%d\n",a);
            
        else
        
            printf("%d\n",(sum-d)/c);
            
    }
    
    return 0;
    
}

