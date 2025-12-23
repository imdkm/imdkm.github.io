+++
title = "Ctrl2Cap ver.3.0 が一部アプリで効かない事案"
date = "2025-12-24T02:00:15+09:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = ["jpn",]
+++

　先日 PC 環境を一新した都合でいろいろとアプリを入れ直しているのだけれど、自分にとってかかせないのが Ctrl と CapsLock の入れ替え。Microsoft 謹製の Ctrl2Cap をインストールすれば済むのでややこしいことはない。はずが、**今年リリースされた最新バージョン（3.0）では一部のアプリで入れ替えが効かない**ようだった。

　具体的には、音楽制作ソフト [Renoise](https://www.renoise.com/) で Ctrl2Cap が効かなかった。Ctrl キーを押下しても、CapsLock として認識されてしまう。レジストリを編集するオールドスクールな方法も試したけど無理。この解決策がわからず、しばらくハマっていた。いろいろ試行錯誤した結果、 Ctrl2Cap のバージョン違いが原因ということがわかった。

> v2.0まではインストールを実行すると、「%Windir%￥System32￥drivers」に「Ctrl2cap.sys」ドライバーがインストールされましたが、新しいバージョンv3.0はCtrl2capのインストールでドライバーのインストールを必要としなくなりました（画面1）。そのため、以前はドライバーのインストールを反映するためにOSの再起動が必要でしたが、新バージョンではサインインのし直しで機能するようになりました。

　[ITニュース.　Sysinternals更新情報: Ctrl2Cap v3.0、BgInfo v4.33](https://www.say-tech.co.jp/contents/blog/yamanxworld/2025news022) より。

　インストール時に「再起動いらなくなったのか～　地味だけど便利だな」と思っていたこれが原因かもしれない。

　現在、Ctrl2Cap の旧バージョンは公式に入手できないため、 [Internet Archive](https://archive.org/) から発掘（[公式の配布 URL](https://learn.microsoft.com/ja-jp/sysinternals/downloads/ctrl2cap) を Wayback Machine に突っ込んで、2025 年 2 月より前の任意のスナップショットを参照すれば OK）。インストールの手順自体は現在のものと変わらないが、メモリ整合性の設定をオフにする必要がある（かもしれない）。なのでリスクを認識の上でどうぞ。

　旧バージョンをインストールした結果、Renoise でも問題なく Ctrl キーが動作した。DAW 全般そうっちゃそうなんだけど、Renoise のようなトラッカーはとりわけキーボード操作が命なので、キーボードの使い心地が変わるのはかなり死活問題。これで新環境でも快適トラッカー生活を送れるはず。

　もっとも、たまたまバージョンを下げたタイミングでうまくいっただけかもしれないけれど、これでうまくいきました、という報告だけ……。

　そもそも Renoise ってなに？　という人は現代ドラムンベースの鬼才 Sully の The Art of Production を見ましょう。トラッカー文化と現代 DAW の折衷として素晴らしいソフトウェアです。

{{< youtube yzXCvaMZQ60>}}

　かつ、Ctrl を CapsLock に入れ替えてなにがうれしいんだと思うひともいるかもしれない。これは実際使って慣れてくるとわかるのだが、A の左隣の CapsLock キーを Ctrl キーにすると、小指がめちゃくちゃ楽。もともと UNIX 系の文化らしいけれど、シンプルに便利なのでおすすめです。