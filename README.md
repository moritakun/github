# GitHub基本操作

* repositoryを作成したいディレクトリへ移動し、Gitリポジトリの初期化
  * git init
    ```
    Reinitialized existing Git repository in /Users/moritahiro/.git/
    ```
* インデックスにファイルを追加（コミットするファイルが集まる場所）
※新規レポジトリを追加する場面では特に意識する必要はない
  * git add -A
* インデックスに控えているファイルたちをコミットする
  * git commit -m "コミットメッセージ"
    ```
    [master (root-commit) 7b26a4a] new repository
    2 files changed, 125 insertions(+)
    create mode 100644 git.md
    create mode 100644 setup.md
    ```
* リモートリポジトリをGitHubweb上で作成

  ※コマンドで作成する場合は以下
  ```
  git remote add <リポジトリ名>
  ```
* githubのリモートリポジトリ情報をローカルリポジトリに追加する
  * git remote add origin https://github.com/moritakun/brew.git
* ローカルリポジトリの変更をリモートリポジトリに反映する
  * git push origin master
    ```text
    "master"は、pushを行いたいブランチを指定すること。
    すなわち作業しているローカルブランチ名を指定する必要がある
    ```
* リモートリポジトリをローカルに複製する
  * git clone https://github.com/moritakun/brew.git