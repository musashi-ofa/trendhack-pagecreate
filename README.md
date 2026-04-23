# 整骨院ページ作成アシスタント

症状名を入力するだけでAIがページ原稿を生成するWebアプリです。

## セットアップ

### 1. GitHubにアップロード
このフォルダの中身をすべてGitHubリポジトリにアップロードします。

### 2. Netlifyにデプロイ
1. Netlify（https://netlify.com）にログイン
2. 「Add new site」→「Import an existing project」→ GitHubリポジトリを選択
3. そのまま「Deploy site」

### 3. APIキーを設定
1. Netlify管理画面 →「Site configuration」→「Environment variables」
2. 「Add a variable」をクリック
3. Key: `ANTHROPIC_API_KEY` / Value: AnthropicのAPIキー
4. 保存後「Deploys」→「Trigger deploy」で再デプロイ

## 使い方

1. ページ種別を選ぶ（急性症状／慢性症状／交通事故／産後骨盤矯正）
2. ヒアリングシート（.xlsx）をアップロード
3. 症状名を入力して「原稿を生成する」
4. 生成された原稿を「全文コピー」してSTUDIOや資料に貼り付け

## ファイル構成

```
/
├── index.html               ← アプリ本体
├── netlify.toml             ← Netlify設定
├── netlify/functions/
│   └── claude.js           ← APIプロキシ
└── README.md
```
