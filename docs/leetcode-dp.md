# LeetCode 動態規劃筆記

這是一個測試頁面，用來驗證 **LaTeX** 和 **Mermaid** 在 Zero-md v3 下的渲染效果。

## 1. 數學公式 (MathJax)

斐波那契數列的通項公式（Binet's Formula）：

$$
F_n = \frac{1}{\sqrt{5}} \left[ \left( \frac{1+\sqrt{5}}{2} \right)^n - \left( \frac{1-\sqrt{5}}{2} \right)^n \right]
$$

行內公式測試：時間複雜度為 $O(n \log n)$。

## 2. 系統架構 (Mermaid)

這是一個分散式系統的簡單示意圖：

```mermaid
graph TD
    User[使用者] -->|HTTP Request| LB[負載平衡器]
    LB -->|Round Robin| Web1[Web Server 1]
    LB -->|Round Robin| Web2[Web Server 2]
    
    subgraph Backend
    Web1 --> Cache[(Redis Cache)]
    Web2 --> Cache
    Web1 --> DB[(PostgreSQL)]
    Web2 --> DB
    end
```

## 3. 程式碼高亮 (Python)

```python
def fib(n: int) -> int:
    if n <= 1:
        return n
    dp = [0] * (n + 1)
    dp[1] = 1
    for i in range(2, n + 1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]
```
