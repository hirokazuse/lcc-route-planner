# LCC ルートプランナー

LCCを乗り継いで「寄り道」を楽しむルートをAIが提案するアプリ。

## デプロイ手順

### 1. GitHubにリポジトリを作成してpush

```bash
git init
git add .
git commit -m "init"
git remote add origin https://github.com/あなたのユーザー名/lcc-route-planner.git
git push -u origin main
```

### 2. Vercelにデプロイ

1. https://vercel.com にログイン（GitHubアカウントで）
2. "Add New Project" → GitHubリポジトリを選択
3. Framework Preset: **Other** を選択
4. "Environment Variables" に以下を追加：
   - Name: `ANTHROPIC_API_KEY`
   - Value: `sk-ant-...`（あなたのAPIキー）
5. "Deploy" をクリック

### 3. 完了

数分でURLが発行されます。

## ファイル構成

```
lcc-route-planner/
├── index.html        # フロントエンド
├── api/
│   └── route.js      # Serverless Function（APIキー管理）
├── vercel.json       # Vercel設定
└── .gitignore
```

## APIキーの取得

https://console.anthropic.com でアカウント作成 → API Keys → Create Key
