# Carrel 公式サイト（静的HTML）

Google Cloud の OAuth 同意画面（ブランディング）に登録するホームページ・プライバシーポリシー・利用規約。
ビルド工程・フレームワークはなく、GitHub Pages にそのまま置ける。

## 構成

```
index.html     トップ（Google のブランディング「アプリのホームページ」）
privacy.html   プライバシーポリシー（同「プライバシーポリシーのリンク」）
terms.html     利用規約（同「利用規約のリンク」・任意）
style.css      共通スタイル。配色はアプリの src/theme/index.ts（light/dark）に合わせ、OSの外観設定に追従
.nojekyll      GitHub Pages の Jekyll 処理を止める空ファイル
assets/icon.png アプリアイコン（Carrel の assets/icon.png のコピー）
```

## 文言について

- pakiin-website の privacy.html / terms.html を下敷きに、Carrel の実装に合わせて書き換えたもの
  （広告・課金・分析・クラッシュ報告はなし、Googleドライブは `drive` スコープで利用者が開いたフォルダのみ読み、
  編集保存とチェックボックスのときだけ対象ファイルを書き換える、更新データは EAS Update から取得）。
- アプリに外部SDKを足したとき（分析・広告・課金など）や、Drive の扱いを変えたときは privacy.html を必ず更新する。
- 運営者表記は「Bootstrapp Works」、問い合わせ先は hello.apps.support@gmail.com（pakiin と共通）。

## 公開

GitHub に公開リポジトリ（例: `kazuwind/carrel-website`）を作って push し、
Settings → Pages → Branch: `main` / `/(root)` で公開する。独自ドメインを使う場合は CNAME を追加して DNS を設定する。
