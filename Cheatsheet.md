# Cheatsheet

## 直前のコメントを修正
$ git commit --amend -m "cssを修正"

## 強制再プッシュ
$ git push -f origin master


## ローカルの変更をすべて取り消したいとき、gitignoreが適用されないとき

キャッシュを削除する

$ git rm -r --cached .


## フォークしたレポジトリのフォーク元が進んだとき

参考：https://qiita.com/Nossa/items/ace2ab802adc85f86b20

・ローカルのフォークリポジトリにフォーク元のリポジトリをリモートブランチとして追加する

$ git remote add upstream https://github.com/フォーク元オーナー名/フォーク元リポジトリ名.git

・リモートブランチの一覧を確認するとのフォーク元のリポジトリが追加されている

$ git remote -v

・フォーク元の master ブランチの変更差分をフェッチ

 ※upstream/master に保管されます
 
$ git fetch upstream

・（必要に応じてmasterブランチをチェックアウトし）フォーク元の差分をマージします。
$ git checkout master

$ git merge upstream/main

## 今使っているアカウントの確認

・アカウントの確認

$ git config user.email

・リモートURLの確認

$ git remote -v

## Branch

ブランチの作成

$ git branch < branchname >

ローカルのブランチの一覧

$ git branch


リモートのブランチの一覧

$ git branch -r

ローカルの作業を新しいブランチを作成し移管

$ git checkout -b < branchname >
