# 🚀 TableCraft（テーブルクラフト）完全放置マネタイズ・デプロイ手順書

TableCraft は、Markdown 表、CSV、Excel/TSV を即座に相互変換し、美しいテーマで Word/Docs用リッチHTMLコピーや高解像度PNG保存ができる、**完全クライアントサイド型・維持費永久0円**のマイクロWebツールです。

---

## 💎 特徴とキラー機能

1. **維持費 永久0円**: データベース不要、静的HTML/JS完結のため、Vercel / Cloudflare Pages / GitHub Pages 等で無料ホスティング可能。
2. **完全機密保持 (100% Client-Side)**: サーバー通信一切なし（Zero-Tracking）。企業や研究者が安心して業務で使えるため、リピート率が高い。
3. **Word/Docs用リッチHTMLコピー**: インラインCSS付きでクリップボードへ保存され、WordやGoogleドキュメントに美しい装飾のまま貼り付け可能。
4. **AdSense審査対応済み**: フッターにプライバシーポリシー・利用規約モーダルを完備。

---

## 🛠️ 世界公開（デプロイ）の3大ルート（すべて無料・所要時間3〜5分）

### ルート1: Vercel（最もおすすめ・最速で全世界HTTPS公開）

1. [Vercel](https://vercel.com/) にアクセスし、無料アカウントを作成（GitHub連携が便利）。
2. ダッシュボードで **「Add New...」→「Project」** を選択。
3. **方法A（ドラッグ＆ドロップ）**:
   - Vercel CLIを使うか、GitHubリポジトリ経由でこの `tablecraft/` フォルダをインポートする。
4. **方法B（GitHub連携）**:
   - 新規GitHubリポジトリ（例: `tablecraft`）を作成し、このフォルダ内の全ファイルをプッシュ。
   - Vercel でそのリポジトリを選択して **「Deploy」** をクリック。
5. **完了**: 数秒で `https://tablecraft-xxxx.vercel.app` のような世界中からアクセス可能なURLが即時発行されます！

---

### ルート2: Cloudflare Pages（超高速・帯域無制限・完全無料）

1. [Cloudflare](https://dash.cloudflare.com/) にログインし、「Workers & Pages」→「Create application」→「Pages」を選択。
2. GitHubリポジトリを連携するか、この `tablecraft/` フォルダを直接ドラッグ＆ドロップしてアップロード。
3. **完了**: `https://tablecraft.pages.dev` のURLが発行されます。

---

### ルート3: GitHub Pages（GitHubアカウントだけで完結）

1. GitHub で新規公開リポジトリ（例: `tablecraft`）を作成。
2. このフォルダのファイルをプッシュ。
3. リポジトリの **Settings → Pages** を開き、Source を `Deploy from a branch`（`main` / root）に設定して保存。
4. **完了**: 数分後に `https://<あなたのユーザー名>.github.io/tablecraft/` で公開されます。

---

## 💰 完全自動化・マネタイズ（収益化）の手順

### ステップ1: Google Search Console に登録（完全放置集客の第1歩）
1. [Google Search Console](https://search.google.com/search-console) にログイン。
2. デプロイしたURL（例: `https://tablecraft.vercel.app`）を登録。
3. 左メニューの「サイトマップ」から `sitemap.xml` を送信。
4. これにより、Googleの検索エンジンが数日〜数週間でページをインデックスし、「Markdown 表 変換」「CSV 表 整形」などの検索から勝手に人が集まり始めます。

### ステップ2: Google AdSense に申請（自動広告収入）
1. [Google AdSense](https://www.google.com/adsense/) に申し込み、サイトURLを登録。
2. 発行された `ca-pub-XXXXXXXXXXXXXXXX` コードを、`index.html` の `<head>` 内のコメントアウト部分に貼り付ける。
3. 審査通過後、上部のスポンサー枠やフッター上に自動で広告が表示され、クリック・表示ごとに収益が発生します。

### ステップ3: Buy Me a Coffee（投げ銭リンク）の本番化
1. [Buy Me a Coffee](https://www.buymeacoffee.com/) で無料アカウントを作成。
2. 自分のページURL（例: `https://www.buymeacoffee.com/yourname`）を取得。
3. `index.html` 内の `https://www.buymeacoffee.com/` と書かれている箇所（ヘッダーとフッター）を自分のURLに差し替える。

---

## 📂 構成ファイル一覧

- `index.html`: 本番Webアプリケーション本体（SEOタグ、構造化データ、プライバシーポリシー、全機能内蔵）
- `robots.txt`: 検索エンジンクローラー制御
- `sitemap.xml`: Googleインデックス用サイトマップ
- `vercel.json`: Vercelホスティング用セキュリティヘッダー設定
- `README.md`: 本手順書
