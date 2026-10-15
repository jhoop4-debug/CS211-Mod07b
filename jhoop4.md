- Name: Jared Hooper
- Major: Computer Science
- Favorite Topic: Data Structures
- Most Challenging Topic: Everything Related To Machine Organization

  

```c
int findCatalan(int n) {
    // code here
    
    long long memo[20];

    long long catalan(int n) {
        if (n == 0 || n == 1) {
            return 1;
        }

        if (memo[n] != 0) {
            return memo[n];
        }

        long long ans = 0;

        for (int i = 0; i < n; i++) {
            ans += catalan(i) * catalan(n - 1 - i);
        }

        memo[n] = ans;
        return ans;
    }

    int findCatalan(int n) {
        return catalan(n);
    }
    

}




```
