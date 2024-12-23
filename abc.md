# Câu 1
``` txt
a) Nhập mảng 1 chiều các số nguyên là tuổi của n nhân viên.
```
Khai báo biến n, mảng nhập tuổi -> nhập vào 
``` c++
int n, a[1005];
cin >> n;
for (int i = 1; i <= n; i++) cin >> a[i];
```
---
``` txt
b) Đếm số nhân viên có số tuổi là x trong mảng.
```
Dùng biến cnt để đếm và if để so sánh, điều kiện là a[i] == x
```c++
int cnt = 0;
for (int i = 1; i <= n; i++)
    if (a[i] == x) cnt++;
```
---
``` txt
c) Cho biết vị trí của nhân viên có tuổi là x và xuất hiện lần thứ k trong mảng
```
Dùng biến id để lưu vị trí người đó, biến d để xét nhân viên có tuổi x, khi gặp tuổi x thì biến d sẽ tăng thêm 1, tức là đã đi tới người có tuổi x xuất hiện thứ d trong mảng. 
``` c++
int id, d = 0;
for (int i = 1; i <= n; i++) {
    if (a[i] == x) d++;
    if (d == k) {
        id = i;
        break;
    }
}
```
---
``` txt
d) Ghi mảng tuổi vào tệp 'sotuoi.txt', dòng đầu tiên là số nhân viên n, dòng thứ 2 là tuổi của các nhân viên, giữa các tuổi cách nhau 1 khoảng cách.
```
Nhập mảng tuổi vào file 'sotuoi.txt' bằng freopen, sau đó in ra n và số tuổi. 
``` c++
freopen("sotuoi.txt", "w", stdout);
cout << n << endl;
for (int i = 1; i <= n; i++)
    cout << a[i] << ' ';
```
--- 
``` txt
e) Trong hàm main(), thực hiện các công việc sau:
- Nhập một mảng chứa tuổi của 5 nhân viên.
- Cho biết có bao nhiêu nhân viên có tuổi là 30?
- Cho biết vị trí của nhân viên có tuổi 30 và xuát hiện lần thứ 2 trong mảng.
- Ghi số nhân viên n và mảng tuổi của các nhân viên vào tệp 'sotuoi.txt'.
```
``` c++
int main() {
    int n = 5, a[10]; 
    /// yeu cau 1
    for (int i = 1; i <= n; i++) cin >> a[i];

    /// yeu cau 2
    int cnt = 0;
    for (int i = 1; i <= n; i++)
        if (a[i] == 30) cnt++;
    cout << cnt << endl; 

    /// yeu cau 3
    int id, d = 0;
    for (int i = 1; i <= n; i++) {
        if (a[i] == 30) d++;
        if (d == k) {
            id = i;
            break;
        }
    }
    cout << id << endl; 

    /// yeu cau 4
    freopen("sotuoi.txt", "w", stdout);
    cout << n << endl;
    for (int i = 1; i <= n; i++)
        cout << a[i] << ' ';
```
