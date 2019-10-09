# githubにプルリクエストを送るまでの流れを理解するRTA
---------
## ・プルリクエストを送るまでの手順
1. githubのページからこのリポジトリをフォーク(リモートリポジトリ間で複製)する
2. フォーク先リポジトリをクローン(リモートリポジトリをローカルへ複製)する
```
git clone https://github.com/<your USERNAME>/git-teaching.git
```
3. 適当なファイルを作成し、コミットする
```
touch hogehoge.txt
git add .
git commit -m "fugafuga"
```
4. ローカルリポジトリの変更をフォークしたリポジトリにプッシュ(反映)する
```
git push origin master
```
5. githubのフォーク先リポジトリからフォーク元のリポジトリへプルリクエストを送る

## ・フォーク元の変更をフォーク先に反映させるまでの手順
1. (すでに行っていない場合)フォーク元リポジトリをリモートリポジトリ先として設定する
```
git remote add upstream https://github.com/IRcpjs/git-teaching.git
```
2. フォーク元の変更をローカルのリポジトリへ反映する(コンフリクトに注意)
```
git pull upstream master
```
or
```
git fetch upstream
git merge upstream/master
```
3. フォーク先のリポジトリへローカルリポジトリの変更を反映する
```
git push origin master
```
