# how_to_use_git

## Gitをつかうとき

- ソースコードを管理したい時
- 誰かとプログラムを共有したい時
- オープンソースを使いたい時
- 高度なバージョン管理をしたいとき

## Gitを使うと何がうれしいのか

例えばあなたがプログラマだとしましょう。
プログラマというのはプログラムを書いて不具合を見つけたら修正をするという繰り返しをします。
プログラムとは不思議なもので、さっきまで動いていたものも一行足しただけで全く動かないということはざらです。そのため、前のバージョンを残すことは大切です。
もしその流れをGoogleDriveで行ったらどうなるでしょうか。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/01.png)

きっとこのようにたくさんの過去バージョンにフォルダは埋め尽くされているでしょう。
そこで便利なのがGitというわけです。

また、Githubにはクオリティチェックという概念があり、設定によっては文章やプログラムを自動でレビューさせることもできます。

## Gitの基本的な考え方

Gitにはブランチという概念があります。
プログラムは最初に作ったファイルがあり、内容を足したり引いたりして改善しています。それを木のようにたとえているのです。(画像ではmasterと書かれたブランチ)
このように、最初に作られたファイルに対しての差分を順に記録しているということになります。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/02.png)

また、バグ修正などのためにプログラムを書き換えるが、安定した本バージョンは残しておきたいというときもあります。
そんな時にブランチというものが役に立ちます。
ブランチとは、安定なものが木だとしたら枝のようなものです。木と全く同じものに手を加えることはできるが、木本体には変更が反映されないという状況が使えるというわけです。(画像ではdebugブランチ)

![version](https://github.com/mask337/how_to_use_git/blob/master/images/03.png)

その後デバッグしているものも安定したらそれを木に取り込むことで安定版のみを更新し続けることができます。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/04.png)

このように、masterブランチには安定版が更新されていますね。

## Githubでの簡単な更新の仕方

Githubで始めたらまずリポジトリ(Gitを組み込んだフォルダ)を作ります。
ホーム画面のnewボタンを押下すると、画像のようになります。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/005.png)

本ファイルは私の知り合い向けに作っているので、それ向けに説明します。
まず、Owner。これは作成者アカウントを指します。
その右のRepositryNameというところに作成するフォルダの名前を入れましょう。なんでもいいです。
その下のDescriptionは無視して大丈夫です。
その下にはPublic Privateの切り替えがあります。Publicだと他の人から見ることができ、Privateだと自分と指定したユーザのみが閲覧編集が可能です。
Initialize this repository with a README というのは、このフォルダに説明書をつけるか聞かれています。つけておくとあとで自分で参照するときなどに便利でしょう。
そこまで終えたらCreateRepositryを押下しましょう。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/06.png)

そうしたらこのような画面になると思います。これがリポジトリの中身です。
とりあえず今はWeb上で使うことを想定していますのでそれ以上は後々。
緑のボタンの左、CreateNewFile, UploadFile, FindFileとありますが、きっとみなさんはすでにものを書き始めていると思いますのでUploadFileを選択しましょう。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/07.png)

次の画面ですが、ここにアップロードするファイルをドラッグ&ドロップしましょう。フォルダでもいいと思うます。
最後に、Commit Changesとあります。これは後の自分に向けて「ここを変えたよ！」とメモを残しておくものです。
このコミットというものが前章の図でいう丸で、このコミットの積み重ねがバージョンとして記録されているというわけです。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/08.png)

最後に、ブランチの作り方と統合(マージと呼ぶ)の仕方を説明します。
リポジトリの画面に戻りまして、先ほどアップロードした時に押したボタンのずっと左、Branch:masterと書かれたところがあります。これは今masterブランチにいると示しています。
これを押すと検索窓が出てきますので、そこに任意の名前を入れます。下にCreate branch : hogehogeと表示されますので、クリックするとブランチが作成できます。
切り替えるときは、同じボタンから、すでに作成済みのブランチ一覧が表示されるので好きなものを選びましょう。

最後に、統合の仕方です。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/09.png)

このようなバーからBranchsを選択しましょう。ブランチの名前が並んでいると思いますので、右端のNew Pull Requestを押下。
緑色のCreate Pull Requestを押下。もう一度緑のボタン、Merge Pull requestを押下すると、目的のブランチはmasterに統合されます。

![version](https://github.com/mask337/how_to_use_git/blob/master/images/10.png)

![version](https://github.com/mask337/how_to_use_git/blob/master/images/11.png)

## おわりに

おめでとうございます。これでGitを使えるようになりました。

ここに書かれていることはGitのうち本当にごく一部です。
必要に応じて知識を追加したり人に聞いたりしましょう。
