# prime-numbers
import java.util.Scanner;
 class Application
{
    public static void main(String[] args) {
        int flag,count=0;
        int a,b;
        int i,j;
        Scanner input= new Scanner (System.in);
        System .out.println ("Enter two number [a,b]");
        a=input.nextInt();
        b=input.nextInt();
        if(a<=0||b<=0||a>=b)
        {
            System.out.println ("error!Invalid input");
            System .exit(0);
        }
        System .out.println ("prime numbers  are :");
        for(i=a; i<=b;i++)
        {
            flag=0;
            
            for(j=2; j<=i/2;j++)
            {
                if(i%j==0)
                {
                    flag =1;
                    break;
                }
            }
            if(flag==0)
            {
                System .out.printf("%d\t",i);
                count++;
                
            }
        }
        System .out.printf ("total number of prime numbers are %d",count);
    }
}
