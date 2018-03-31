# README.md: research-vision-2018

## インストール方法

```
$ gem install slim html2slim
$ yarn global add bower yo grunt-cli generator-reveal gulp
$ git clone git@github.com:zacky1972/research-vision-2018.git
$ cd research-vision-2018
$ yarn install
$ bower install
```

## プレゼンテーション表示方法

```
$ cd research-vision-2018
$ grunt serve
```

## GitHub Pages への公開

```
$ cd research-vision-2018
$ grunt deploy
```

[このページを開きます](https://zacky1972.github.io/research-vision-2018/)

## スライドの追加

### Markdown のスライドの追加

```
$ cd research-vision-2018
$ yo reveal:slide "slide-title" --markdown
$ subl slides/slide-title.md
```

next-slide-title には英語のタイトルを入れる(そのままファイル名になる)。残念ながら日本語は通らない。

### HTML のスライドの追加

```
$ cd research-vision-2018
$ yo reveal:slide "slide-title"
$ subl slides/slide-title.html
```

slide-title には英語のタイトルを入れる(そのままファイル名になる)。残念ながら日本語は通らない。

CSS は css/source/theme.scss を編集する

### Slim のスライドの追加

HTML のスライドの追加をした後，同名の slim ファイルを追加する

```
$ cd research-vision-2018
$ yo reveal:slide "slide-title"
$ html2slim slides/slide-title.html slides/slide-title.slim
$ subl slides/slide-title.slim
```

slide-title には英語のタイトルを入れる(そのままファイル名になる)。残念ながら日本語は通らない。

CSS は css/source/theme.scss を編集する

Slim を追加した場合は，スライドを表示したりデプロイしたりする前に `gulp` を実行して slides/\*.slim を変換しておく

```
$ cd research-vision-2018
$ gulp
```
