# substring
import java.util.Arrays;
import java.util.Scanner;


public class substring {
	
	public static void main(String[] args) {
		
		String s,y,z;
		
		//char c = 'm';
        Scanner in = new Scanner(System.in);
		s= in.next();
		int x = s.length();
		System.out.println(x);
		int n = (x*(x+1))/2;
		System.out.println(n);
		String str[] = new String[n];
		int k=0;
		for(int i=0;i<s.length();i++)
		{
			 for(int j=i+1;j<=s.length();j++)
			{
				str[k]=s.substring(i,j);
				System.out.println(str[k]);
				k++;
			}
		}
	
		
	    Arrays.sort(str);
	    System.out.println("Substrings in alphabatical order :");
		for(int j=0;j<k;j++)
		{
			System.out.println(str[j]);
		}
		System.out.println(" Greatest  Lexicographical String is"+ str[k-1]);
	}

}
