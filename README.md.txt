#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
int computer,you;
 int menu()
{
    int n;

    printf("\n1.select rock");
    printf("\n2.select paper");
    printf("\n3.select scissors");
    printf("\n4.exit");
    printf("\nenter your choice");
    scanf("%d",&n);
    return(n);
}
void setup()
{
    label:
    computer= rand()%4;
    if(computer==0)
        goto label;
    you=menu();
}

void logic()
{
    switch(you)
    {

    case 1:
        if (computer==1)
            printf("\ndraw");
        else if(computer==2)
            printf("\ncomputer won");
        else
            printf("\nyou won");
            break;
    case 2:
         if(computer==2)
        printf("\ndraw");
        else if(computer==1)
            printf("\nyou won");
        else
            printf("\ncomputer won");
            break;
        case 3:
            if(computer==3)
            printf("\ndraw");
        else if(computer==1)
            printf("\ncomputer won");
        else
            printf("\nyou won");
            break;
            case 4:
        exit(0);
        break;
                default:
                printf("\nwrong choice");


    }

}
int main()
{
    while(1){

    setup();
    logic();
    getch();
    }
    return 0;

}




