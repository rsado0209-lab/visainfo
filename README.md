# Visa Info - 世界各国ビザ取得ガイド

日本人向けのビザ取得条件をまとめたWebサイトです。

## デプロイ設定

### 初回セットアップ（GitHub Secrets）

main ブランチへのプッシュで自動デプロイするため、以下の手順で `FIREBASE_TOKEN` を設定してください。

1. ローカルで Firebase CLI にログイン済みであることを確認
2. トークンを取得：
   ```bash
   firebase login:ci
   ```
3. 表示されたトークンをコピー
4. GitHub リポジトリ → **Settings** → **Secrets and variables** → **Actions**
5. **New repository secret** をクリック
6. Name: `FIREBASE_TOKEN`、Value: コピーしたトークンを入力して保存

### デプロイ

`main` ブランチにプッシュすると自動で Firebase Hosting にデプロイされます。

```bash
git push origin main
```

## ローカルで確認

```bash
firebase serve
```

ブラウザで http://localhost:5000 を開いてください。
