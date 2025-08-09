# reverse-string
import java.util.*;
public class palindrome_string
{
    String s ;
    String rev ;
    boolean flag ; 
    palindrome_string(){
        s="";
        rev= "";
        flag= false;
    }

    public void input()
    {
        Scanner sc = new Scanner(System.in);
        System.out.print("enter the string to be reversed : ");
        s = sc.nextLine();
        s=s.toUpperCase();
    } 

    public String reverse(String n )
    {
        for(int i = 0 ; i<n.length();i++)
        {
            char ch = n.charAt(i);
            rev = ch+rev;
        }
        return rev;
    }

    public boolean check(String ch )
    {
        if(ch.equals(s))
        {
            flag = true;
        }
        else{
            flag = false;
        }
        return flag ; 
    }

    public void display()
    {
        System.out.println("   OUTPUT   ");
        System.out.println("ORIGINAL STRING : "+s);
        System.out.println("REVERED STRING : "+rev);
        if(flag== true  )
        {System.out.println("THE GIVEN STRING IS PALINDROME STRING ");
        }
        else
        {
            System.out.println("THE GIVEN STRING IS NOT A PALINDROME STRING ");
        }
    }

    public static void main(String args[])
    {
        palindrome_string obj = new palindrome_string();
        obj.input();
        obj.reverse(obj.s);
        obj.check(obj.rev);
        obj.display();
    }
}
