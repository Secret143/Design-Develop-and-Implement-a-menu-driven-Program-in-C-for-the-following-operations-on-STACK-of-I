#include <stdio.h>

#include <stdlib.h>

#include<conio.h>

int max=5;

int s[5],top=-1;

void push()

{

    if(top==4)

        printf("\nStack overflow!!!!");

    else

    {

        scanf("%d",&s[++top]);

        printf("\n %d is inserted into the stack",s[top]);

    }

}

void pop()

{

    if(top==-1)

        printf("\nStack underflow!!!");

    else

        printf("\nElement popped is: %d",s[top--]);

}

void disp()

{

    int t=top;

    if(t==-1)

        printf("\nStack empty!!");

    else

        printf("\nStack elements are:\n");

    while(t>=0)

        printf("%d ",s[t--]);

}

int main()

{

    int ch;

    do

    {

        scanf("%d",&ch);

        switch(ch)

        {

            case 1:

            push();

            break;

            case 2:

            pop();

            break;

            

            case 3:

            disp();

            break;

            case 4:

            exit(0);

            default:

            printf("\nInvalid choice");

        }

    }

    while(1);

    return 0;

}
