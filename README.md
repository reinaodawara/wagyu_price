# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
- リモートリポジトリ→ネット上に配置するして複数人で共有するためのリポジトリ。
ローカルリポジトリ→開発者一人ひとりが司代いうするために自分のPC上に配置するためのリポジトリ。

## プッシュとマージの違いは何でしょうか？
- プッシュ→ローカルの内容をリモートにアップする作業
マージ→別のブランチの作業内容（変更履歴）をブランチに取り込むこと

## コミットとプッシュの違い
- コミット→追加・変更したファイルをGitに保存するためのコマンド。ローカルリポジトリに変更を反映する
プッシュ→リモートリポジトリに変更を反映する

## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
###一目で変更内容がわかるようにする。
「指摘箇所修正」や　「とりあえずコミット」のようなコミットメッセージは、良いメッセージではない。
履歴を見た際に、そのコミットメッセージから「どんな変更を行ったのか」がわかるようなメッセージにすることが重要。

## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
- リモートリポジトリ上でリポジトリをしているという点
ローカルでマージするフロー
１．masterブランチにいる状態であることを確認
２．git merge working　を実行
└git merge　コマンドは、あとにブランチ名を記載して実行することで現在いるブランチに指定したブランチの変更履歴を取り込むことができる。

プルリクエストでマージするフロー
プルリクエストとは、変更内容をマージしてくださいという依頼を行うこと
１．pull requestタブを選択し、画面右のNew pull requestボタンをクリックする
２．差分が相違なければ、右上の緑のCreate pull requestボタンをクリックする
３．タイトルを記入して右下のCreate pull Requestボタンをクリックする

## コンフリクトを起こしてしまった場合、どう対処すべきですか？
- 同じタイミングで切った2つのブランチでそれぞれ同じファイルの同じ行に対して別の変更を行った状態でmergeすると、どちらの変更を採用するべきかをGitが判断することができず、mergeが中断されてしまうこと。

コンフリクトが発生した場合、以下の3通りの方法で変更を取り込む必要がある。
1.先にマージされた変更内容を取り込む
2.あとにマージしようとしている変更内容を取り込む
3.どちらの変更も取り込む
