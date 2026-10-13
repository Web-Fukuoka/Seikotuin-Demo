# ひだまり整骨院 Webサイト

静的サイト（HTML / CSS / 少量のJS）です。ビルド不要で、GitHub Pages にそのまま公開できます。

## 公開手順（GitHub Pages）
1. GitHub で新しいリポジトリを作り、このフォルダの中身をすべてアップロード
2. リポジトリの Settings → Pages を開く
3. Source を「Deploy from a branch」、Branch を `main` / `/(root)` にして Save
4. 数分後に `https://ユーザー名.github.io/リポジトリ名/` で公開されます

独自ドメインを使う場合は、Settings → Pages の Custom domain に入力してください。

## 公開前に差し替える箇所【要入力】
`index.html` 内で「要入力」「0000」を検索すると見つかります。

- LINE予約ボタンのリンク先（エルメの予約ページURL）… `href="#reserve"` の LINE ボタン3か所
- 電話番号 `03-0000-0000` / `tel:0300000000`
- 住所・地図リンク（Googleマップの共有URL）
- 公開URL（`canonical` と `og:image`、`sitemap.xml`、`robots.txt`）
- OGP画像 `img/ogp.jpg`（1200×630px）を追加
- GA4 の測定ID（`<head>` 内のコメントを外して `G-XXXXXXX` を置き換え）
- 写真の出典（`img/CREDITS.md` とフッターの制作メモ）

## 計測イベント
ボタンを押すと `dataLayer` に以下のイベントが送られます（GTMでコンバージョン設定に使えます）。
`tel_tap` / `tel_tap_bar` / `tel_tap_menu` / `line_tap_main` / `line_tap_bar` / `line_tap_menu` / `cta_hero` / `cta_header` / `map_open`

## 画像
- `xxx-s.webp`：スマホ用（幅480px）、`xxx.webp`：大きい画面用
- 写真を差し替えるときは同じファイル名で上書きすれば反映されます
