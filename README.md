# LaTeXで作成するレポートの雛形

レポートを作るときに、元になるファイルを提供しています。

* `report_sample.tex` レポート本文のソースファイル
* `latexmkrc` オンラインのLaTeX環境 [Overleaf](https://www.overleaf.com) でpLaTeXを利用するための設定
* `golden_egg.png` 画像ファイルの取り込みの例のための画像ファイル

→ [雛形から生成したPDF](https://tos-kamiya.github.io/latex_report_sample/report_sample.pdf)

## PDFの生成

### ptex2pdfコマンドを利用する場合

TeXLiveがインストールされている環境で、ファイルを置いたディレクトリに移動して、次のコマンドラインを実行します。

```sh
$ ptex2pdf -e -l -od '-f ptex-ipaex.map' report_sample.tex
```

※ 相互参照を正しくレンダリングするには2回コンパイルする必要があります。

※ `-e -l`はLaTeXのコンパイラとしてplatexを使う指定です。

※ `-od '-f uptex-ipaex.map'`は生成するPDFにフォントを埋め込む指定です（つけないと、PDFのサイズは小さくなりますが、見る環境によって文字の見た目が変わります）

### Overleafを利用する場合

(1) プロジェクトを作成し、すべてのファイルをアップロードしてください。`report_sample.tex`の中身は`main.tex`にコピーしてください。

(2) メニューから「Settings」の「Compiler」を「LaTeX」に変更してください。

(3) 「Recompile」ボタンでコンパイルしてください。

## 謝辞

このリポジトリでは次のファイルを再利用させていただいています。感謝いたします。

* ファイル `latexmkrc` は doraTeX さんの [Overleaf v2 で日本語を使用する方法](https://doratex.hatenablog.jp/entry/20180503/1525338512) のものを利用しました。
* ファイル `golden_egg.png` は いらすとや さんの [金の卵のイラスト ](https://www.irasutoya.com/2017/02/blog-post_426.html) を利用しました。
* ファイル `.gitignore` は <https://github.com/github/gitignore/blob/main/TeX.gitignore> を利用しました。
