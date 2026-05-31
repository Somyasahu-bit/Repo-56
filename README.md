# Repo-56
check if even number is expressed as sum of 2 prime numbers 
import java.util.*;
public class Equal {
    public static boolean isprime(int n) {
        if (n <= 1) 
            return false;
            for (int i=2; i<=Math.sqrt(n);i++) {
                if (n % i==0)  return false;
            }
            return true;
        }
           public static boolean sum_prime(int num) {
          for (int i = 2; i <= num; i++) {
            if (isprime(i) && isprime(num - i)) {
                System.out.println(i + " " + (num-i));
                return true;
            }
            }
            return false;
        }
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            int num = sc.nextInt();
            if(sum_prime(num)) {
                System.out.println("yes it's possible");
            } else {
                System.out.println("no");
                sc.close();
            }
        }
}
