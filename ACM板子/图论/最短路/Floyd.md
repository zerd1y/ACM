## 时间复杂度 O(N**3) 空间复杂度 O(N**2)
```cpp
for (k = 1; k <= n; k++) {
  for (x = 1; x <= n; x++) {
    for (y = 1; y <= n; y++) {
      f[x][y] = min(f[x][y], f[x][k] + f[k][y]);
    }
  }
}
```
## 输入
```cpp
memset(f, 0x3f, sizeof(f));
for (int i = 0; i < m; i++) {
		int x, y, z;
		cin >> x >> y >> z;
		f[x][y] = z;
		f[y][x] = z;
}
for (int i = 0; i <= n; i++) f[i][i] = 0;
```
