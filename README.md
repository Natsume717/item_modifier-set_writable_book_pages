# item_modifier-set_writable_book_pages
item_modifierの1項目であるset_writable_book_pagesのサンプルになります。

~詳しくはブログ記事『[]()』を参考にしてください。~<br>
現在執筆中

<h3>概要</h3>
本と羽ペンに対して、ページの挿入を行えます。<br>
署名後はwritten_bookとなるため対応していません。

<h3>使い方</h3>

データパック導入後、ワールドに入り```/reload```と入力し実行してください。

本と羽ペンが複数付与されますので、適当に内容を記述します。

どのコマンドを実行するにしても<b>5ページ程度適当に記載し、署名せずに完了すれば準備OK</b>です。

それをメインハンドに持った状態で以下のコマンドを実行してください。

```copy
/item modify entity @s weapon.mainhand sample:append
```

```copy
/item modify entity @s weapon.mainhand sample:insert
```

```copy
/item modify entity @s weapon.mainhand sample:replace_all
```

```copy
/item modify entity @s weapon.mainhand sample:replace_section
```

すると、sample_textという文面が記載されているページが増えているはずです。

それぞれの挿入方法については、以下の通りです。

|項目|挿入の規則|
|-|-|
|append|最後のページに挿入|
|insert|指定したページに当てはまるよう挿入|
|replace_all|内容をすべて上書き|
|replace_section|指定したページからsizeで指定した分のページをまとめて上書き|

replace_sectionについて補足。<br>
offsetが0、sizeが1だとした場合は、1ページ目と2ページ目の計2ページが指示したテキストへと変更される。<br>
offsetが0ではあるが、1ページを0としてカウントし始めるので、初めの2ページが上書きされるということ。
