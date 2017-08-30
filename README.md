# tplab
#include <stdio.h>
#include <stdlib.h>

int capicua(int a[],int ini, int dim);

int main()
{
    int array[5] = {1,2,3,4,1};
    int rta = capicua(array,0,5);
    printf("%i",rta);

    return 0;
}

int capicua(int a[],int ini, int dim){
    int flag = 1;
    if ( ini < dim ){
        if ( a[ini] == a[dim-1] ){
            flag = capicua(a,ini+1,dim-1);
        }
        else{
            flag = 0;
        }
    }

    return flag;
}
