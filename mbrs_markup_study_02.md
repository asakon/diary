# まぼろしのマークアップ勉強会 #3 (#mbrs_markup_study) 「おさらいしておきたい基本仕様」に参加しました

2018/02/23(金)、池袋の株式会社まぼろし様で開催された、[まぼろしのマークアップ勉強会 #2](https://maboroshi.connpass.com/event/77979/)に参加しました。

おいしいピザを、あったかいうちに【※重要】食べつつ、ゆったりとした雰囲気で、参加者の皆さんのLTを聞いて、対話するという会でした。

バックグラウンドは様々な参加者でしたが、共感することもあり、「知らなかった！」もあり、楽しく参加できました。

「参加したかったんですけれども、LTできるか不安で、一回、見送りました＞＜」と伝えると、まぼろしの久保さん@kojika17から「全然構えなくてOKですよ～」とやさしいお言葉が・・・！
ありがとうございます！

ちなみに・・・

誰も（※もちろん自分もね）基本仕様の話、して、なかった、ような・・・（笑）

いえ、応用も基本に通ずる！！！

皆さん、自由に、発表したいテーマでのびのび発表して楽しい会でした。


## ふりかえり

### 『figureとfigcaptionと私』 by webcre8

はっきり言って、かなりの問題作でした。

この発表はラストでしたが、それまでみんなで「もう、マークアップでもめることって無くなったよね」って言っていたのに…

動揺が残る発表でした。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">Q. HTML5ではimgはfigureにいれるんでしょ？<br>A. 本文の流れに組み込まれたものはfigureではない。 <a href="https://twitter.com/hashtag/mbrs_markup_study?src=hash&amp;ref_src=twsrc%5Etfw">#mbrs_markup_study</a></p>&mdash; 久保 知己 (@kojika17) <a href="https://twitter.com/kojika17/status/967020142163931136?ref_src=twsrc%5Etfw">2018年2月23日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">Q.キャプションをつけたいならfigureでしょ？<br>A. 話の流れに組み込まれているならfigureではない。 <a href="https://twitter.com/hashtag/mbrs_markup_study?src=hash&amp;ref_src=twsrc%5Etfw">#mbrs_markup_study</a></p>&mdash; 久保 知己 (@kojika17) <a href="https://twitter.com/kojika17/status/967020961252876288?ref_src=twsrc%5Etfw">2018年2月23日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


### 考察：figureでなぜ人はモメるのか？

- HTMLはもともと学術論文をベースにしていたはず。それを考えると「fig 1.」とかでグラフとか図像とか配置されてる。それが「無くても」論文は成立すると言い切れるのだろうか？？

[Living Standard](https://html.spec.whatwg.org/#the-figure-element)より

>The figure element represents some flow content, optionally with a caption, that is self-contained (like a complete sentence) and is typically referenced as a single unit from the main flow of the document.

- 「本文から参照される単一ユニット」の定義が哲学的過ぎる（※個人の感想です）
と思ったけど、（今は何となく）わかるかも・・・

- さし絵はfigureだとは思えない・・・文脈と関連するのでは・・・

- 「文書の流れに組み込まれていないもの」という定義は、ちょっと厳しいのでは・・・
文書に必要だからそのコンテンツが配置されているのであって、「なくてもフローが成立するという判断」の難易度が高いように感じる

というモヤモヤを残してセッションが終わりました。。。。。

### 『君の名は。』 by kojika17

「class名に使って良い文字の範囲があるんだよ」というお話でした。

資料名をメモしそびれたのですが、たしか、この当たり↓のお話かと

[4.1.3 文字と活字ケース - Cascading Style Sheets Level 2 Revision 2 (CSS 2.2) Specification 日本語訳](https://momdo.github.io/css2/syndata.html#characters)

> CSSにおいて、（要素名、クラス、およびセレクター内のIDを含む）識別子は、文字[a-zA-Z0-9]およびISO 10646のU+0080以上の文字、さらにハイフン（-）およびアンダースコア（_）のみを含むことができる。識別子は、数字、2つのハイフン、ハイフンの直後の数字で開始できない。識別子はまた、エスケープされた文字および数字コードとして任意のISO 10646文字を含めることができる（次項を参照）。たとえば、識別子"B&W?"は、"B\&W\?"または"B\26 W\3F"として記述してもよい。 

この「およびISO 10646でU+00A0以上の文字」の、「以上の文字なんでもいいんかーい」というのがポイントでした。

(私は、スライドで使われている筑紫B丸ゴシック（Typekitに入っているそうです）がきれいで感動しました。)

発表後の対話時間で、私が「今日、Gitのタグに絵文字が入ることに気づいて遊んでました。SourceTreeでは表示されたんですが、ターミナルでは表示されなかったような？」と（テーマから逸れた）お話をしたところ、「バッククオートと16進数表記で行けるかもですね。そう言えば昔、書いた記事がありまして・・・」と、久保さんが紹介してくださったのがこちら！

[CSSの変態向き - ID, classを顔文字でコーディングする方法｜Web Design KOJIKA17](http://kojika17.com/2013/03/kaomoji_selectors.htm)

サンプルのCSSがこちら

http://kojika17.com/demo/kaomoji/style.php

な、なるほど！よめない！！！

ちょっと面白いお話でした。


### 『srcset + sizes 迷宮の再訪問（仮）』 by toru_

img要素で使う、srcset, sizesのお話でした。

toru_さんの「皆さん、使ってますよね？」の問いかけに「もちのろんよ」という顔で頷いてしまいましたが、私はpicture派でした。。。

すみません。。。。（IEを捨ててました・・・）

toru_さんの、複雑な仕様に斬り込む姿勢に圧倒されました。なにがなんだか・・・ややこしいですね。。。

「sizesとsrcsetは連動しなくていい」まじすか・・・

「srcは必須ではないらしい」まじすか・・・

なお、toru_さんは、WordPressのコントリビューターでもいらっしゃって、WPのテーマの話も聞けました。

（そして、ライティングの話でも、みんなで盛り上がりました。）

### 『JSON-LD書いてみた。』 by Kitada_Elly

グーグル検索結果ページに良き感じで表示されたりするJSON-LDのお話でした。

私は、Microdataしか知らなかったのと、Microdataのしんどさに「うう」と引いていたので、きたださんの「JSONだとエラーがはっきりわかるからメリットある」というお話にハッとしました。

GoogleはJSON-LD推しで、テスティングツールもあるそうです。
https://search.google.com/structured-data/testing-tool?hl=ja

日本円の書き方にちょいと一工夫必要だそうです。ローカライズはひと手間かかるものですよね・・・。

あと、検索結果の表示は、どうもグーグルのお気持ち次第というところがあるらしく、「同じ書き方をしていても必ずしも同じようには表示されない」という現象もあるそうです。


### 『なつかしいね！HDML』 by asakon

昔話がしたかったんです・・・。

[発表資料改訂版](https://docs.google.com/presentation/d/1rHGg8n0WqG3XV5fkN_YOys4dBtA813kZuyC6dyQe9mc/edit?usp=sharing)


~~マークアップの話してるのに、そしてマークアップの仕事してるのに、マークダウンで書かなくてごめんなさい。あとでどうにかするかも。~~ amended!
