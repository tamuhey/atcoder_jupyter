# Jupyter Magic Command for AtCoder

## install

`$ git clone https://github.com/tamurahey/jupyter_magic`  
`$ cp jupyter_magic/atcoder_test.py ~/.ipython/profile_default/startup/`

## How to Use

テストしたいコードを書いたセルの最初に

```
%%test_input url
```

と書くだけでテストできます．  
  
例えば[ABC100 A](https://abc100.contest.atcoder.jp/tasks/abc100_a)の問題なら

```python
%%test_input https://abc100.contest.atcoder.jp/tasks/abc100_a
a, b = map(int, input().split())
print("Yay!") if a <= 8 and b <= 8 else print(":(")
```
とかけば
  
```
... test case 0 ...
<<< 5 4
Yay!
... test case 1 ...
<<< 8 8
Yay!
... test case 2 ...
<<< 11 4
:(
```
と出力されます．
  
urlでなく，テストケースが書いてあるファイル名を指定してもOK．

```
%%test_input filename
```

複数ファイルを指定できます.

```
%%test_input f1 f2 f3...
```
-sオプションを付けると，urlから読み込んだ結果をテストケースごとにファイルに保存します．

## Note

コンテスト開催中は使えません  
