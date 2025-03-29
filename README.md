#include <stdio.h>
#include <stdlib.h>

void giamdan(int array[], int n)
{
    int i,j,tam;
    for (i = 0; i < n - 1; i++)
        {
            for (j=0;j<n-i-1;j++)
            {
                if (array[j]<array[j+1])
                {
                // Hoán đổi giá trị
                int tam=array[j];
                array[j]=array[j+1];
                array[j+1]=tam;
                }
            }
        }
}

void printarray(int array[], int n)
{
    int i;
    for (i=0;i<n;i++)
    {
        printf("%d ",array[i]);
    }
    printf("\n");
}

int main()
{
    int a[5] = {3, 2, 6, 1, 0};
    int n=5;

    printf("Mang truoc khi sap xep: \n");
    printarray(a,n);
    giamdan(a,n);
    printf("Mang sau khi sap xep: \n");
    printarray(a, n);

    return 0;
}
