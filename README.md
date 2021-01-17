# MECH_study_for_graduation
This is a LaTeX format for senior study of mechanical engineering, Dpt. of Mechanical Engineering, Tokyo Tech.
# コンパイル関係  
**環境**：utf-8  
**実行**：platexでコンパイルしてください．  
**構成**：main, intro, second, third, conclusionファイルから成ります．個人好きに追加してください．  
**表示**：mainファイル実行→ファイル内容全部表示，subfileファイル実行→subfileファイル内容のみ表示．全部実行すると重い…という人や小さいファイル単位で確認したい人向け．  
# 本文  
**書式**：jsmepaper.clsファイル及び数々のstyファイルで書式が決定されています．  
**画像**：figファイル内に置きます．mainファイル内に記述がありますが，figファイル内に更に章ごとにファイルを作って画像を入れると管理が楽です．  
```
\graphicspath{{./fig/header/}{./fig/intro/}{./fig/second/}{./fig/third/}}
%figureの相対パスを指定しておきます
```
# 参考文献  
**内容**：ref_ver2.bibに参考文献内容を記載してください．書き方はBibTeXとかでググればよし．  
**注意**：著者名が日本人の場合，以下のようにyomiフィールドを付けましょう．（名前順に並び替えるが故です．）  
```
@article{白井大地:2013-09,
author="白井, 大地 and 武田, 史郎 and 落合, 勝昭",
title="温室効果ガス排出規制の地域間CGE 分析",
journal="環境経済・政策研究",
ISSN="1882-3742",
publisher="岩波書店",
year="2013",
volume="6",
number="2",
pages="12-25",
yomi="Shirai, Daichi",
URL="http://ci.nii.ac.jp/naid/40019823794/",
DOI="",
}
```
**本文での引用の仕方**  
上述の参考文献を引用する場合，本文で以下のように記述してください．よく使う```\cite```ではないので注意．  
```
先行研究\citep{白井大地:2013-09}によると…
```
**書式**：jcon-jsme.bstが書式ファイルです．  
**Tips**：Mendeleyでの論文管理はいいぞ．  
**メモ**：参考文献のファイルを変更する場合は，以下の二か所でファイル名を変えましょう．  
```
%subfileで参考文献が出るようにする
\def\biblio{\def\newblock{\hskip .11em plus .33em minus .07em}\renewcommand{\refname}{文献}\nocite{*}\bibliographystyle{./jecon-jsme}\bibliography{./ref_ver2}}
```
```
% ==== 参考文献 =========================================
\def\newblock{\hskip .11em plus .33em minus .07em}
\renewcommand{\refname}{文献}
\nocite{*}
\bibliographystyle{./jecon-jsme}
\bibliography{./ref_ver2}
```
# Overleaf  
Overleafにてサンプル例を作りました．  
プロジェクトをコピーして自分で編集してもらってもコンパイルができると思います．  
原因を特定中ですが，subfile単位でのコンパイル時に画像が出てこないです．
<https://www.overleaf.com/read/ndzzvqdwbhsv>
