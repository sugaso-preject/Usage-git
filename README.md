# gitの使い方

gitの使い方。  
PCのターミナルでgitコマンドが使えるようにする必要がある。  
インストール方法はwindows git インストールとかで検索。(kosukeGMへ)

Gitで開発するときの基礎の基礎。  
1.クローン/clone :リポジトリの内容をローカルPC(自分のPC)にコピーする。  
2.コミット/commit :更新した情報を、Gitに記憶させる。  
3.プッシュ/push:ローカル(自分のPC)で変更した内容を、元(Github上)のリポジトリに反映する。  
以下詳しい説明。

まずは、リポジトリをクローンする。クローンとはGitHub上で管理されているリポジトリを、
ローカルPC上(自分のPC)にコピーすることをいう。  
チーム開発では全員が同じファイルを修正することがあるため、マスタのリポジトリ(Github)と作業用(自分のPC)のリポジトリとに分けて管理する。

cloneの実行例  
$ git clone https://github.com/sugaso-preject/Usage-git  ;(多分コピペでいけるはず)

Cloning into 'sugaso-project'...  
remote: Counting objects: 6, done.  
remote: Compressing objects: 100% (2/2), done.  
remote: Total 6 (delta 0), reused 3 (delta 0), pack-reused 0  
Unpacking objects: 100% (6/6), done.  
Checking connectivity... done.  

成功したときは上のような内容がでる(はず)。

lsコマンドでコピーできたか確認できる。  
$ ls　　　　　　　　　　　　　　  
README.md　sugaso-project/　　(sugaso-projectがあればOK)  

新しいファイルを作ってみる。  
Self-idというファイルを作り自己紹介文を書く。  
書き終わったら **git add -A** というコマンドと **git commit -m "Self-id"**というコマンドを実行する。この**commit**というコマンドがファイルの変更をGitに反映させるという命令。

コミットが終わったら最後に**git push**を実行。
これによって自分が修正した内容が他のチームメンバーからも見られるようになる。

git commitが出来ない時の対応.  
ターミナルを開き、以下を入力。  
$ git config --global user.email "your mailaddress writed"  
$ git config --global user.name "your mailaddress writed"  

これでユーザー情報の登録完了。

設定した情報を上書きするには、以下を入力。  
$ git config --global --replace-all user.email "your mailaddress writed"

設定した情報を確認するコマンドは以下のコマンド。  
$ git config --global -l
