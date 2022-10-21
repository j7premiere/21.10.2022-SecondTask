### Task 6 kyu

[Task link](https://www.codewars.com/kata/541c8630095125aba6000c00)

Digital root is the recursive sum of all the digits in a number.

Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. The input will be a non-negative integer.

### My solution

```Java

public class DRoot {
    public static int digital_root(int n) {
        return (n - 1) % 9 + 1;
    }
}

```

### Favourite solution from code-wars

```Java

    public class DRoot {
        public static int digital_root(int n) {
            int sum = 0;
            do {
                char[] array = ("" + n).toCharArray();
                sum = 0;
                for(char c : array) sum += Integer.valueOf("" + c);
                n = sum;
            } while(sum >= 10);
            return sum;
        }
    }

```

USING CHAR HERE? HAHA

I want to proof theorem that I used.

Take any positive integer n. n = a_m a_m-1 ... a_0 , where a_i digits of n.
n=mod9= a_m + a_m-1 + a_m-2 + ... + a_0 =mod9 = digit between 0 and 8.

We cant get sum 9 when using mod9, but we can get sum 9 by recursive sum of digits, so we take (n-1)mod9 + 1, this way we can get 9 by recursive sum 

# Have a nice day!