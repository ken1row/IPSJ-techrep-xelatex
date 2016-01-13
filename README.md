# IPSJ-techrep-xelatex
情報処理学会研究会原稿をShareLatexなどのXeLaTeX環境で執筆するための疑似スタイルファイルです．

### 注意点
* 本プロジェクトは，情報処理学会とは無関係です．本スタイルファイルを使用する場合は，自己責任でお願いします．
* スタイルの正確性は保証していません．提出時は，情処提供クラスファイルを用いてローカルでコンパイルしてください．

# クイックスタート
### ShareLatex での同時共同執筆
1. 以下の4つのファイルをShareLatexにアップロードする．
 * ipag.ttf
 * ipamjm.ttf
 * ipsj.sty
 * tech_jsample_xela.tex
2. ShareLatex の左上メニューから，コンパイラに XeLaTex を設定する．
 
### 提出時 (Windowsの場合)
1. tech_jsample_xela.tex をダウンロードし，以下の2行をコメントアウトする．

 ```
 \documentclass[a4paper]{article}
 \usepackage{ipsj}
 ```
2. 以下の行を有効にする．

 ```
 \documentclass[submit,techreq,noauthor]{ipsj}
 ```
3. compile_original.bat をダブルクリックし，コンパイルする．

#その他
### フォントについて
実は，ShareLatexにはIPAフォントが用意されているので，フォントのアップロードは不要だったりします．
フォントをアップロードしない時は，```ipsj.sty```の ```\setCJKmainfont{ipamjm.ttf}```を```\setCJKmainfont{ipam.ttf}```に書き換えてください．
IPA明朝jmフォントは人名などに使われる特殊漢字が収録されています．そういう文字を使わない時は，通常のIPA明朝で十分です．

IPAフォントがインストールされていない環境でXeLaTexを使うときのために，フォントを同梱しています．
### 既知の問題
* レイアウトずれ 
  * 著者名の間のスペース
  * 小さい文字（ャなど）
  * subsection, subsubsection の後の行間
  * itemize 環境の行間
  * etc...
* ヘッダーに線が入っている
* biography （の無視）には非対応

### 免責
本スタイルファイルを用いたことによるいかなる損害についてもその責を負いません．
自己責任にてご使用ください．また，スタイルの正確性は保証していません．
提出時は必ず学会提供クラスファイルを用いてコンパイルしてください．
