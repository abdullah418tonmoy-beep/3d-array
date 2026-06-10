#include<stdio.h>

int main()
{
    int x,y,z,arr[100][100][100];

    printf("Enter your array size[x][y][z] : ");
    scanf("%d%d%d",&x,&y,&z);

    if(x>100 || y>100 || z>100)
    {
        printf("Size must be <= 100\n");
        return 1;
    }

    for(int i=0; i<x; i++)
    {
        for(int j=0; j<y; j++)
        {
            for(int k=0; k<z; k++)
            {
                printf("Array[%d][%d][%d]: ",i,j,k);
                scanf("%d",&arr[i][j][k]);
            }
        }
    }

    printf("\nStored Values:\n");

    for(int i=0; i<x; i++)
    {
        for(int j=0; j<y; j++)
        {
            for(int k=0; k<z; k++)
            {
                printf("Array[%d][%d][%d]: %d\n",
                       i,j,k,arr[i][j][k]);
            }
        }
    }

    return 0;
}
