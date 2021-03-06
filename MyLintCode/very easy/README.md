# *From : www.LintCode.com*
## 2.整数排序
**描述**  
查找斐波纳契数列中第 N 个数。  
所谓的斐波纳契数列是指：

前2个数是 0 和 1 。
第 i 个数是第 i-1 个数和第i-2 个数的和。
斐波纳契数列的前10个数字是：

0, 1, 1, 2, 3, 5, 8, 13, 21, 34 ...

**注意事项**  
The Nth fibonacci number won't exceed the max value of signed 32-bit integer in the test cases.  

**样例**

`Given nums = 1`  
`return 0`  
`Given nums = 2`  
`return 1`  
`Given nums = 10`  
`return 34`
 
## 解决方案一
使用递归的方式，计算出要求的数，返回该数。  
注：本方案执行效率稍低。
## 代码实现（JAVA）
	
	public class Solution {
	    /*
	     * @param n: an integer
	     * @return: an ineger f(n)
	     */
	    public int fibonacci(int n) {
	        // write your code here
	        if (n <= 2){
	            if (n == 1){
	                return 0;
	            }
	            if (n == 2){
	                return 1;
	            }
	        }
	        int sum = 0;
	        sum = fibonacci(n - 1) + fibonacci(n - 2);
	        return sum;
	    }
	}
	
## 解决方案二
这里只是使用了一个for循环，执行时间只是解决方案一的一半，再次领略到算法的魅力。

## 代码实现
	public class Solution {
	    /*
	     * @param n: an integer
	     * @return: an ineger f(n)
	     */
	    public int fibonacci(int n) {
	        // write your code here
	        int j = 0;
	        int k = 1;
			if (n <= 2){
	            if (n == 1){
	                return 0;
	            }
	            if (n == 2){
	                return 1;
	            }
	        }
	        for (int i = 0; i < n - 1; i++) {
	            int c = j + k;
	            j = k;
	            k = c;
	        }
	        return j;
	    }
	}eetCode上刷题的记录，包括原题目、题目的中文大意、解决思路及代码。  
这里我用的是java语言来实现的。

### 持续更新中。。。


**下面是题目的链接：**    

1. [twoSum](https://github.com/tanranuncle/MyLeetCode/blob/master/1.twoSum.md)



