OCaml-SnakeGame
===============


プログラミング言語OCamlを使ってへびゲーム(SnakeGame)を作りました。

へびゲームは有名なゲームで、プレイヤーはへびを操作し、エリア内のえさを食べ続けるというゲームです。へびの頭が自分の体に触れないように操作するのですが、えさを食べると体（尻尾？）が伸びるので、ぶつからないように食べ続けることが段々難しくなるところがミソです。へびゲームには色々なバリエーションがあり検索するといっぱい見つかると思います。本サイトのへびゲームのポイントは以下の通りです。

* コンソール画面(CUI)で動かす
* へびはキーボード(WASDキー)で操作する

一般的(?)なへびゲーでは、へびは一定速度で頭の進行方向に移動し続け、プレイヤーはへびの方向転換だけを操作するのですが、今回はタイマー処理などを省くため、へびの移動はキーボード押下時のみとします。

ゲームのイメージはこんな感じです。`*`記号がへびです。`O`(大文字オー)がエサです。

```
+-----+
|     |
|  ** |
|   * |
| O * |
|     |
+-----+
```

なお、[Newral技術者ブログ](http://newral.info/publics/index/79/&anchor_link=page79_341#page79_341)というサイトでプログラミングの過程を記事にしております。是非ご覧下さい。

###記事へのリンク  
[OCamlでへびゲームを作る(Part1)](http://newral.info/publics/index/79/page341=6/r_id=180/c_id=341/detail=1/&anchor_link=page79_341_180#page79_341_180)  
[OCamlでへびゲームを作る(Part2)](http://newral.info/publics/index/79/page341=5/r_id=182/c_id=341/detail=1/&anchor_link=page79_341_182#page79_341_182)  
[OCamlでへびゲームを作る(Part3)](http://newral.info/publics/index/79/page341=5/r_id=183/c_id=341/detail=1/&anchor_link=page79_341_183#page79_341_183)  
[OCamlでへびゲームを作る(Part4)](http://newral.info/publics/index/79/page341=5/r_id=185/c_id=341/detail=1/&anchor_link=page79_341_185#page79_341_185)  
[OCamlでへびゲームを作る(Part5)](http://newral.info/publics/index/79/page341=5/r_id=187/c_id=341/detail=1/&anchor_link=page79_341_187#page79_341_187)  

###ソースコードガイド

SnakeGame.ml (上記記事でプログラミングしたソースコード)  

###実行方法

ocamloptコマンドでコンパイルしてから遊びます。

```ocaml
bash-3.2$ ocamlopt SnakeGame.ml
bash-3.2$ ./a.out

+-----+
|     |
|     |
| ****|
|  O *|
|   **|
+-----+
```

