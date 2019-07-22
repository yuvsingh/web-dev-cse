#include<stdio.h>
int main()
{
    int a[50],i,n,j,k,c=0,c2,temp;
    printf("enter the limit of array\n");
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
     for(i=0;i<n;i++)
    {
        if(i!=0)
        {
            k=i-1;
            while(k>=0)
            {
                if(a[i]==a[k])
                {
                    i++;
                    k=i-1;
                }
                k--;
            }
        }
    if(i!=n)
    {
        for(j=i+1;j<n;j++)
        {
            if(a[i]==a[j]&&i!=j)
            {
                c++;
                break;
            }
        }
    }
    if(c==3)
    {
        printf("third repeating element %d",a[i]);
        break;
    }
    }
}

