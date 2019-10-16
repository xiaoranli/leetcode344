# 11、leetcode344. 反转字符串
解法一：
--  
思路：
--
    双指针来解决。i指向数组的第一个元素，j指向数组的最后一个元素。每次交换i和j的两个位置的元素，然后将i向左移动一步，j向右移动一步即可0  
代码： 
--
<pre>
/**
 * @author lihe
 * @date 2019/10/16 20:22
 * @descriptor  344. 反转字符串
 */
public class ReverseString_344 {
    public static void reverseString(char[] s) {
        if(s == null || s.length < 1)
            return;
        int l = -1,r = s.length;
        while(++l < --r){
            char temp = s[l];
            s[l] = s[r];
            s[r] = temp;
        }
        System.out.println(Arrays.toString(s));
    }
    public static void main(String[] args) {
        char[] c = {'a','b','c'};
        reverseString(c);
    }
}
</pre>
