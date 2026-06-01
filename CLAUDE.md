常に日本語で返すこと。回答は簡潔に。
## Stop Hook
タスク完了前に必ず/Users/okawanorihiko/Documents/Obsidian Vault/second-brain/mistakes/claude-mistakes.mdを確認すること。
ミスが発生したら同じファイルに以下の形式で記録すること：
- 何をやったか
- 本来どうするべきか
- どんな状況で起きるか
## セキュリティ
- APIキー・トークン・パスワードなどの機密情報が画面に表示される可能性があるコマンドや操作を提案する場合、実行前に必ず警告を出すこと

---
## 引き継ぎルール

### 作業開始時
- ~/Dev/HANDOVER.md を読む（全体状態の確認）
- 該当プロジェクトの HANDOVER.md を読む（詳細確認）

### 作業中
- 区切りのいいタイミングで両方の HANDOVER.md を更新する

### 作業終了時
- ~/Dev/HANDOVER.md と該当プロジェクトの HANDOVER.md を必ず更新してから終了

### HANDOVER.md に書く内容
- 現在の状態（何をどこまでやったか）
- 重要な決定事項
- 次のタスク（具体的に）
- 注意点・ハマりポイント

## 新規プロジェクト開始時
1. ~/Dev/[プロジェクト名]/ を作成
2. CLAUDE.md を作成（技術スタック・設計ルール・プロジェクト固有の注意点）
3. HANDOVER.md を作成（初期状態を記載）
4. ~/Dev/HANDOVER.md のプロジェクト一覧に追記

## 開発ルール

### ファイル編集
- 文字列の編集は必ずPythonスクリプトを使う（/tmp/ に配置して実行）
- sed は日本語・特殊文字で破壊的なバグを起こすため絶対に使わない

### CSS
- 色の指定は必ずCSS変数を使う（例：var(--color-primary)）
- ハードコードのhex値（例：#3B82F6）は絶対に使わない

### デプロイ・git
- git push は本番に即反映されるため、push前に必ず変更内容を確認すること
- .env ファイルの内容は絶対に表示・共有・コミットしない
- 公開リポジトリへのpush前に機密情報が含まれていないか確認を促すこと

### ツール役割分担
- Claude Code：設計・実装メイン
- Codex：レビュー・実行・自動化

## MCP設定
- Obsidian Vault：/Users/okawanorihiko/Documents/Obsidian Vault/second-brain
- mistakes.md：/Users/okawanorihiko/Documents/Obsidian Vault/second-brain/mistakes/claude-mistakes.md

## dotfiles同期ルール
- 作業開始時は必ずgit pullを実行すること。
- 作業終了時は必ずgit pushを実行すること。
---
