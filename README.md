# Remote-Procedure-Call

## 概要
異なるプログラミング言語で書かれたクライアントとサーバが共通の方法で通信し、特定の関数を実行することができるシステムです。</br>

具体的にはクライアントがPythonで書かれたサーバーに対して、Javascriptから命令を出します。

サーバは以下の関数を RPC としてクライアントに提供します。</br>

- floor(double x): 10進数xを最も近い整数に切り捨て、その結果を整数で返す。
- nroot(int n, int x): 方程式 r**n = x における、rの値を計算する。
- reverse(string s): 文字列sを入力として受け取り、入力文字列の逆である新しい文字列を返す。
- validAnagram(string str1, string str2): 2つの文字列を入力として受け取り2つの入力文字列が互いにアナグラムであるかどうかを示すブール値を返す。
- sort(string[] strArr): 文字列の配列を入力として受け取り、その配列をソートして、ソート後の文字列の配列を返す。

さらに、上記に示されているような一連の関数をクライアントに提供することで、サーバはRPCを実現します。これにより、クライアントはサーバ上で定義された関数を呼び出し、その結果を取得することができます。

- floor
実行
```
Input Method --> floor
Input params --> 5.7
Input Id --> 1
```
サーバーからのレスポンス
```
{ results: 5, id: '1' }
```

- nroot
実行
```
Input Method --> nroot
Input params --> 2, 16
Input Id --> 2
```
サーバーからのレスポンス
```
{ results: 4, id: '2' }
```

- reverse
実行
```
Input Method --> reverse
Input params --> hello
Input Id --> 3
```
サーバーからのレスポンス
```
{ results: "olleh", id: '3' }
```

- validAnagram
実行
```
Input Method --> validAnagram
Input params --> listen, silent
Input Id --> 4
```
サーバーからのレスポンス
```
{ results: true, id: '4' }
```

- sort
実行
```
Input Method --> sort
Input params --> banana,apple,orange
Input Id --> 5
```
サーバーからのレスポンス
```
{ results: ["apple", "banana", "orange"], id: '5' }
```









