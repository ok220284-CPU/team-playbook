# Claude への申し送り

## 絶対ルール

### 1. URLは絶対に変えない
- Cloudflare Pages の `project_name` = リポジトリ名そのまま
- 先頭の数字プレフィックス（1, 2, 3, 5 など）も **絶対に外さない**
- URLは他人に共有済みの可能性が高い、変更すると壊れる
- 「シンプル化のため」という理由で勝手にURLを変えてはいけない

例：
- リポジトリ名: `3digital-log`
- project_name: `3digital-log`（そのまま）
- URL: `3digital-log.pages.dev`

### 2. リポジトリは非公開維持
- private: true を必ず保つ
- 一度公開化しても、必ず非公開に戻す

### 3. 設定の場所
- `.github/workflows/deploy.yml` の `project-name` 引数
- ここを勝手に書き換えない

## こーた との進め方

- 日本語で対応
- 「簡単」「すぐ」「だけ」みたいな言葉は使わない（非エンジニアからは大変な作業）
- スクショは負担なので何度も求めない
- 慌てず、ひとつずつ確実に
- 過去の約束はちゃんと覚える

## 環境メモ

- GitHub PAT は `workflow` スコープ必須
- Cloudflare API はサンドボックスから直接アクセス不可
- → デプロイは GitHub Actions 経由のみ
- Cloudflare アカウントID: `7236d591bcc2a40c3032d6aea2f1bab4`
