# dis01
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501101218844.png)

![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501101218704.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501101218373.png)

![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501101219880.png)

![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501101219392.png)

# dis02

## 1. Maximum Subarray Sum
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102102444.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102102067.png)
```c++
class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        return maxSubArray(nums, 0, size(nums)-1);
    }
    int maxSubArray(vector<int>& A, int L, int R){
        if(L > R) return INT_MIN;
        int mid = (L + R) / 2, leftSum = 0, rightSum = 0;
        // leftSum = max subarray sum in [L, mid-1] and starting from mid-1
        for(int i = mid-1, curSum = 0; i >= L; i--)
            curSum += A[i],
            leftSum=max(leftSum, curSum);
        // rightSum = max subarray sum in [mid+1, R] and starting from mid+1
        for(int i = mid+1, curSum = 0; i <= R; i++)
            curSum += A[i],
            rightSum = max(rightSum, curSum);        
		// return max of 3 cases 
        return max({ maxSubArray(A, L, mid-1), maxSubArray(A, mid+1, R), leftSum + A[mid] + rightSum });
    }	
};
```

## 2. Pareto Optimality
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102103896.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102103805.png)

## 3. Counting Inversions
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102108375.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102108651.png)

## 4 Monotone matrices
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102121707.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102121463.png)

# dis03
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102256460.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501102256400.png)

# dis04
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501111408621.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501111409881.png)
创建k+1个G的拷贝 $G_0, G_1,G_2\dots,G_k$。点v在图$G_i$中的拷贝叫做$v_i$。对于在$S_i$中的每个点v，我们加$(v_{i-1}, v_i)$权重为0的边。
比如在上图中，$G_0，G_1$ 要靠$S_1$保持联通，$G_1, G_2$要靠$S_2$保持联通……
这这样保证了$G_0$中边必须要到达$S_1$才能进入$G_1$，$G_1$中边必须到达$S_2$才能进入$G_2$，以此类推。保证有序性的同时由于采用最短路算法满足条件。

![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501111448825.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501111449337.png)

# dis06
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501111608919.png)
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501111608945.png)

![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501111609775.png)

# dis07
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501121011765.png)

# dis08
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501121815743.png)

# dis11
![image.png](https://raw.githubusercontent.com/XuandYu000/picture/main/202501122227647.png)
