# Chiho's Birthday Live 2026 - Reborn 55

2026年2月22日（日）に広尾 Tomo,K'yon,S で開催したバースデーライブの記録ページ。

UTAGE解約にともない、UTAGE会員サイト
`https://utage-system.com/members/vfjAx8P4xR4s/course/PAwB4Byo3stc/lesson/vgq3TLgN9N0m`
から静的サイトとして移設したもの（2026-08-07）。

## 公開先

https://live.linowellbeing.com/

- GitHub Pages（このリポジトリの main ブランチ / ルート）
- 独自ドメインは `CNAME` ファイルで指定。ムームーDNSに CNAME レコード
  `live` → `lino-well-being.github.io.` を登録している。
- `<meta name="robots" content="noindex, nofollow">` を入れているため検索には出ない
  （UTAGE時代の設定を踏襲）。URLを知っている人は誰でも閲覧できる。

## 構成

```
index.html                     1ページ完結。UTAGEの本文をそのまま移植
images/hero.png                ライブのメインビジュアル
images/member-*.jpg            バンドメンバー写真（Web用に1600px幅へ縮小）
images/comment-hatsuhinode.jpg 掲示板に湯沢かずきさんが投稿された初日の出の写真
images/original/               縮小前のオリジナル画像（3600px / 4032px）
CNAME                          GitHub Pages の独自ドメイン設定
```

## 移設時に変えたところ

UTAGEからの移設で、内容そのものは変えていない。仕組み上の差し替えのみ。

- 画像6枚：UTAGEのS3から切り離してリポジトリ内に取り込み（解約後も表示されるように）
- UTAGE短縮リンク `utlink.jp` 2本 → 実URLに置換
  - 松橋さんの著書 → Amazon（アソシエイトタグ `mille222-22` は維持）
  - 筒井真路さん → Facebook
- YouTube埋め込み3本：`controls=0` を外して再生バーを表示、遅延読み込みに変更
  （動画自体はおうち英語キズナClubチャンネルの限定公開動画で、UTAGEとは無関係）
- 掲示板（コメント機能）：UTAGE依存のため書き込み機能はなくなった。
  いただいていたメッセージ4件（返信含む）は「みなさまからいただいたメッセージ」として本文下に掲載。
  投稿日時はUTAGEが「◯日前」の相対表示しか返さず正確な日付が取れなかったため、日付は載せていない。

## 元ページに残っていること（未対応）

本文後半の「開催概要」「歌ってくださる方へ」「エントリーフォーム（締切2026/1/31）」は
開催前の案内文。ライブ終了後もUTAGE上にそのまま残っていたので、忠実にそのまま移してある。
記録として残すか、アーカイブ扱いの見出しをつけるかは要判断。

## 更新のしかた

`index.html` を直接編集して `git push` すれば数分で反映される。
