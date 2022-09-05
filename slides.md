---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: off
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# use UnoCSS (experimental)
css: unocss
---

# 名刺代わりの10冊メイカー

---

# 自己紹介

<div class='flex place-content-center gap-10 mt-10'>
  <img src='/images/Mask_group.png' class='rounded-full w-20 h-20' />
  <div class='self-center'>
    <p>ギア <a href="https://twitter.com/gia_sorairo" class="color-blue">@gia_sorairo</a></p>
    <p>フロントエンドエンジニア 3年目</p>
  </div>
</div>

<div class='flex place-content-center gap-4 mt-10'>

  <div class='p-4' />

  - よく使う技術
    - typescript
    - react/next.js
    - electron
    - node.js

  <div class='p-2' />

  - 最近の悩み
    - 会社辞めたいけど上司に言い出しづらい

</div>

---
layout: center
---

# 目次
- どんなアプリなのか
- なぜ名刺代わりの10冊メイカーをつくろうと思ったのか
  - そもそもなぜ個人開発をしているのか
  - アイデア
- 開発について
  - 使用技術
  - 開発中に心掛けていること
- 実際つくってみてどうだったか
  - リリースツイートをしただけでは、ほとんど使ってもらえなかった
  - 宣伝をサボった自分の怠惰に対する禊として、qiita に記事を投稿することにした
  - 収益
  - 名刺代わりの10冊メイカーをリリースしてからの変化
- まとめ

---

# どんなアプリなのか

- 名刺代わりの10冊を選んで twitter で 書影付きでシェアするアプリ
- 実際に使ってみる

<div class="grid place-content-center">
  <a href="https://tenbooksmaker.com" target="_blank">
    <img src="/images/title.png" class="h-80 self-center mt-4" />
  </a>
  <p class="text-center">名刺代わりの10冊メイカー</p>
</div>

---
layout: center
---

# なぜ名刺代わりの10冊メイカーをつくろうと思ったのか

---

# そもそもなぜ個人開発をしているのか

- 技術のキャッチアップのため🌟
- 仕事で使えない技術を好きに使えるのが楽しいから🌟

<v-click>

  そんな立派な理由ではない。<br />
  自分が個人開発している理由は、

</v-click>

<v-click>

- できるだけ楽にお金を稼ぎたいから💰
- ものづくりが好きだから🚀
- 誰とも関わらず、自分一人で完結できるから👻

</v-click>

<v-click>

ただ個人開発の現実は、

</v-click>

<v-click>

- 楽をしてお金を稼ぐどころか、1 ヶ月かけてアプリをつくっても 1 円も発生しないことがほとんど😇
- お金を稼ぎたいだけなら、アルバイトしたほうがマシ😇

</v-click>

<v-click>

もはや不労所得とは……??😇😇😇😇

</v-click>

---

# アイデア

<div class="grid grid-cols-2 gap-10">

  <div class="">
  

  - きっかけは twitter で「#名刺代わりの小説10選」というハッシュタグのついたツイートが流れてきたこと
  - 小説が好きな自分は、そのハッシュタグのリンクに飛んだ
  - リンク先のツイートを見ていて、改善できそうだなあと思うところがあった

  </div>

  <div>
    <img src="/images/tweet-before.png" class="border" />
    <p class="text-center">流れてきたツイート例</p>
  </div>


</div>


---

# 問題

<div class="grid grid-cols-2 gap-10">

  <div>

  - 「#名刺代わりの小説10選」のツイートはあんまり没入できなかった

  <div class="p-2" />

  ### 理由を考える

  <div class="p-1" />


  - テキストベースで目が滑る
  - 紹介されている書籍を自分で検索する必要がある(リンクがない)

  </div>

  <div>
    <img src="/images/tweet-before.png" class="border" />
    <p class="text-center">流れてきたツイート例</p>
  </div>

</div>

---

# 解決策

<div class="grid grid-cols-2 gap-10">

  <div>

  - この課題は OGP を使えば改善できるなと思った
  - テキストベースから、OGP 画像を利用したイメージベースに改善💪(書影大事)
  - OGP から書籍情報のあるページにユーザを飛ばして、検索体験の改善💪

  </div>

  <div>

  <img src="/images/tweet-after.png" class="border" />
  <p class="text-center">改善後のツイート</p>

  </div>

</div>

---

# マネタイズ

<div class="grid grid-cols-2 gap-10">

  <div>

  - 書籍情報ページに、アフィリエイトリンクを設置すればマネタイズも可能そう

  </div>

  <div class="flex flex-col w-full items-center">

  <img src="/images/detail-page.png" class="border w-60" />
  <p class="">詳細ページ</p>

  </div>

</div>

---

# 集客

- 「#名刺代わりの小説10選」というハッシュタグはそもそも活性がいいので、そのハッシュタグで自分がいくつか OGP 画像つきのツイートすれば、「#名刺代わりの小説10選」をウォッチしているユーザの目にとまって、面白がってつかってくれるはず(妄想、願望)

---
layout: center
---

# ハッシュタグ駆動開発、これはぜったいバズるぞ🤟

---

# 開発について

<a href="https://twitter.com/gia_sorairo/status/1548140744904704000">
  <img src="/images/dev-start-tweet.png" class="border" />
</a>
<p class="text-center">開発開始時のツイート</p>

---

# 使用技術

- typescript
- react/next.js
  - chakra-ui
  - swiper
  - react-infinite-scroller
  - node-canvas
  - imagemin/magemin-webp
- vercel
- firebase (firestore, storage, functions)

<div class="p-2" />

---

# 開発中に心掛けていること

<div class="grid grid-cols-2 gap-10">

  <div>

  - 爆速リリース
    - MVP (Minimum Viable Product) を意識する
    - 完璧を目指さない
    - できるだけライブラリに頼る
    - リファクタリングをしない
    - めちゃめちゃ重要な処理以外はテストを書かない

  自分はすぐに飽きるので、自分が飽きる前にリリースできるかが勝負。
  - 今回は途中で投げ出さないように、進捗をツイートしながら開発を行った。
    - このおかげでサボらずに開発できたと思う

  </div>

  <div>

  <a href="https://twitter.com/gia_sorairo/status/1548140744904704000" target="_blank">
    <img src="/images/dev-start-tweet.png" class="border" />
  </a>
  <p class="text-center">進捗報告</p>

  </div>

</div>
  
---
layout: center
---

# 実際つくってみてどうだったか
- リリース直後は、ほとんど使ってもらえなかった
- 宣伝をサボった自分の怠惰に対する禊として、qiita に記事を投稿することにした結果
- 収益
- 名刺代わりの10冊メイカーをリリースしてからの変化

---

# リリース直後は、ほとんど使ってもらえなかった

<div class="grid grid-cols-2 gap-10">

  <div>

  - 宣伝は、twitter でリリースツイートをしただけ
  - 自分がいくつか「#名刺代わりの小説10選」のハッシュタグをつけてツイートすれば、ハッシュタグ経由でユーザが流れ込んでくるという想定は外れた😢
  - リリースから3日間で、アプリを使用して投稿したユーザは 10 人程度(これはハッシュタグからの流入)
  - 思いのほか流行らなかった😢
  - とはいえ 10 人に使ってもらえた時点で「つくってよかったな」とは思えた🌟
    - 自分の作ったサービスを使ってもらえるとやっぱりうれしい

  </div>

  <div class="flex flex-col w-full items-center">

  <img src="/images/release-tweet.png" class="border w-90" />
  <p class="">リリース報告ツイート</p>

  </div>

</div>

---

# 宣伝をサボった自分の怠惰に対する禊として、qiita に記事を投稿することにした結果📝
- qiita への投稿日 8/13 - (いいね 70)
    - [【個人開発】名刺代わりの10冊メイカーというサービスを作ったけど、恥ずかしくて宣伝してなかった](https://qiita.com/gia_sorairo/items/4aff11325caaf9ae3efd)
- アクセス爆増
  - 投稿日の 8/13 から徐々にアクセスが増えて、アクセス数が最大 6000 [uu/day] くらいまで増えた🆙
  - qiita に投稿してよかった🙏

<img src="/images/google-analitics.png" class="scale-55 mt--25" />

---
layout: center
---

# 収益

---

# 収益 - amazon

- 10,643 yen

<img src='/images/affiliate-amazon.png'>

---

# 収益 - 楽天

- 1025 yen

<img src='/images/affiliate-rakuten.png'>

---

# 収益

- amazon からの収益がほとんど📦
- このまま放置でも 10000 [yen/month] くらいはしばらく稼いでくれそう💰

---

# 名刺代わりの10冊メイカーをリリースしてからの変化

<div class="grid grid-cols-2 gap-10">

  <div>

  - qiita にはじめて記事を書くことができた📝
  - twitter のフォロワが 30 人くらい増えた🆙
  - 名刺代わりの○○10選のハッシュタグをアップデートできた🎉🎉🎉
  - 名刺代わりの10冊メイカーに影響を受けて、サービスを作ったという人が現れた✨
    - [【個人開発】推し曲を動的に生成したOGP付きで共有できるサービス「推し曲.com」を作りました](https://qiita.com/0ba/items/baf8415e0f1593f81cd1)
  - 1 万円の不労所得のおかげで、心置きなく松屋の厚切りネギ塩豚焼肉丼を食べられるようになった🍚
  - はじめて勉強会のお誘いをいただいて、はじめて勉強会というものに参加して、しかも登壇した👩‍🏫

  </div>

<div>

   <!-- <div class="flex flex-col w-full items-center"> -->

  <img src="/images/negi.jpg" class="border" />
  <p class="text-center">松屋 - 厚切りネギ塩豚焼肉丼</p>

</div>

</div>

---
layout: center
---

# さいごに

---
layout: center
---

# まとめ

---
layout: center
---

# アプリをリリースしたら、恥ずかしがらずに qiita に記事を投稿しましょう！




