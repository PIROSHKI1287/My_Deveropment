# CLAUDE.md — AI Operating System Core
# このファイルは「大脳皮質」である。常に最初に読め。

## Mission
[プロジェクト開始時に1文で記入: このシステムは何をするか]

---

## 絶対制約（違反禁止）

1. **計画先行**: 何の作業も `/plans/` への計画記述なしに開始してはならない
2. **/core/ 保護**: `/core/` は明示的な指示なしに変更禁止。変更前に依存関係を全列挙すること
3. **失敗記録**: 予想外の動作・エラーが発生したら即座に `/memories/lessons_learned/` に記録
4. **認証情報ゼロトレランス**: APIキー・パスワード・トークンをコードにハードコード禁止（`.env` を使用）
5. **破壊的操作の確認**: ファイル削除・DBマイグレーション・本番反映は必ず人間に確認を取る

---

## アーキテクチャ設定
[プロジェクト開始時に記入 — docs/ARCHITECTURE.md も同時更新すること]

```
フレームワーク (Frontend) : [例: Next.js 15 / React 19]
フレームワーク (Backend)  : [例: FastAPI / Express / Hono]
データベース              : [例: PostgreSQL / Supabase / MongoDB]
認証                      : [例: NextAuth / Clerk / Firebase Auth]
インフラ                  : [例: Vercel / Railway / AWS]
主要パターン              : [例: Repository Pattern / Server Actions / REST]
```

---

## 既知の失敗パターン（繰り返し禁止）
[/memories/lessons_learned/ から週次で蒸留・更新。初期は空]

---

## 優先順位
**セキュリティ > 正確性 > パフォーマンス > 可読性**

---

## ディレクトリ読み込みルール

| タスク種別 | 追加で読むべきファイル |
|-----------|----------------------|
| 設計判断   | `docs/ARCHITECTURE.md` |
| 過去の失敗確認 | `memories/lessons_learned/` |
| コア変更   | `core/.clauderules` → 計画必須 |
| API設計    | `api/` の `.clauderules`（存在する場合） |

---

## メタデータ
- 最終更新: [YYYY-MM-DD]
- 更新理由: 初期作成
- GitHub: https://github.com/PIROSHKI1287/My_Deveropment
