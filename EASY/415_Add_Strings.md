# :books: [Add Strings](https://leetcode.com/problems/add-strings/)

### :star: Question

- Given two non-negative integers num1 and num2 represented as string, return the sum of num1 and num2.
- The length of both num1 and num2 is < 5100.
- Both num1 and num2 contains only digits 0-9.
- Both num1 and num2 does not contain any leading zero.
- You must not use any built-in BigInteger library or convert the inputs to integer directly.

--- 

### :car: Example



---

### :hammer: Code

#### :coffee: Java Version - 1

```java
public class Solution {
    public String addStrings(String num1, String num2) {
        StringBuilder sb = new StringBuilder();
        int carry = 0;
        for(int i = num1.length() - 1, j = num2.length() - 1; i >= 0 || j >= 0 || carry == 1; i--, j--){
            int x = i < 0 ? 0 : num1.charAt(i) - '0';
            int y = j < 0 ? 0 : num2.charAt(j) - '0';
            sb.append((x + y + carry) % 10);
            carry = (x + y + carry) / 10;
        }
        return sb.reverse().toString();
    }
}
```

- Runtime: 2 ms, faster than 95.05% of Java online submissions for Add Strings.
- Memory Usage: 36 MB, less than 99.80% of Java online submissions for Add Strings.

---

### :pencil: Explanation



---

### :computer: Complexity Analysis:

- Time complexity: O(n)
- Space complexity: O(1)

---

### :pen: Author

YIMING DAI - 2019.07.18
