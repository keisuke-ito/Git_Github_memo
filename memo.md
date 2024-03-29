# About Git/GitHub
Git/githubの使用法についてのメモ


## コマンド
---
基本的にGitの使用用途は
1. Gitを用いてローカルリポジトリ作成
2. githubにローカルリポジトリを反映させたいリポジトリの作成
3. 追加

になるのでこれに沿った流れのメモを記載．

---

### リポジトリの作成
```
$ git init
```
→初期リポジトリの作成ができる．


### リモートリポジトリの追加
・ 既存のリモートリポジトリと共有するなら
```
$ git clone https://username@dimain/path/to/repository
```

・ ローカルリポジトリにリモートリポジトリを反映させる
反映させたい自分のPCのディレクトリで
```
$ git remote add origin https://github.com/~~~~
$ git remote add [追加するリモートリポジトリ名] [追加したいリポジトリ]
```

### ファイルの追加&コミット
### 追加
```
$ git add <filename> or git add * #変更があったファイルを全て索引に追加する．
```

### 変更内容のコミット
```
$ git commit -m "add new file" # -m "commitメッセージ"→なんでも良い
```

この段階では，まだ共有リポジトリには反映されていないので次に反映させる必要がある．

 ### リモートリポジトリへの追加
```
$ git push origin master
```

### 変更内容の確認
```
$ git log
```

・より詳細
```
$ git log -p
```

## ブランチ
記載


### Word
索引(Index)
コミットするためにファイルを索引に追加し，コミット予定のファイル群を記録します．
このコミット対象のファイルを索引に追加する操作は，「ステージング」，「コミット予定」，「管理対象」と
言われる．