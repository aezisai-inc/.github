# コントリビューションガイドライン

Aezisai Inc.のプロジェクトへのコントリビューションをご検討いただきありがとうございます！🎉

## 🚀 はじめに

私たちはClean Architecture、DDD（ドメイン駆動設計）、TDD（テスト駆動開発）を重視しています。コントリビューションの際は、これらの設計原則に沿った実装をお願いします。

## 📋 コントリビューションの流れ

### 1. Issue の作成

- バグ報告や機能リクエストは、まずIssueを作成してください
- 既存のIssueを確認し、重複を避けてください
- テンプレートに従って詳細を記載してください

### 2. フォークとブランチ

```bash
# リポジトリをフォーク後
git clone git@github.com:YOUR_USERNAME/REPO_NAME.git
cd REPO_NAME
git checkout -b feature/your-feature-name
```

### 3. 開発規約

#### コーディングスタイル

- **TypeScript/JavaScript**: ESLint + Prettier 設定に従う
- **Python**: Black + isort + flake8 に準拠
- **命名規則**: キャメルケース（変数・関数）、パスカルケース（クラス・型）

#### コミットメッセージ

[Conventional Commits](https://www.conventionalcommits.org/) に従ってください：

```
feat: 新機能の追加
fix: バグ修正
docs: ドキュメントのみの変更
style: コードの意味に影響しない変更
refactor: バグ修正でも機能追加でもないコード変更
test: テストの追加・修正
chore: ビルドプロセスやツールの変更
```

### 4. テストの実行

```bash
# すべてのテストを実行
pnpm test

# リンターを実行
pnpm lint
```

### 5. Pull Request

- PRテンプレートに従って記載
- レビュアーを指定（必要に応じて）
- CIが通過していることを確認

## 🏗️ アーキテクチャガイドライン

### Clean Architecture

```
src/
├── domain/          # エンティティ、値オブジェクト
├── application/     # ユースケース、DTOs
├── infrastructure/  # 外部サービス、DB
└── presentation/    # API、UI
```

### 依存関係のルール

- **Domain層**は他の層に依存しない
- **外側から内側**への依存のみ許可

## 📖 ドキュメント

- 新機能にはREADME更新を含める
- APIの変更にはドキュメント更新が必須
- JSDoc/TSDocによるコード内ドキュメント推奨

## ❓ 質問・サポート

- **一般的な質問**: [Discussions](https://github.com/aezisai-inc/.github/discussions)
- **バグ報告**: [Issues](https://github.com/aezisai-inc/.github/issues)
- **セキュリティ問題**: [SECURITY.md](./SECURITY.md) を参照

---

ご協力ありがとうございます！🙏

