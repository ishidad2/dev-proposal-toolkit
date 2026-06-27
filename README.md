# dev-proposal-toolkit

Web・システム開発案件の受注提案を一気通貫でサポートするスキルセット。

## 含まれるスキル

| スキル | 使い方 | 典型的なトリガー |
|--------|--------|----------------|
| **market-researcher** | クライアント企業の調査 | 「〇〇社を調べて」「クライアント情報をまとめて」 |
| **engineer** | 技術選定・アーキテクチャ設計 | 「技術選定して」「DB設計して」「システム構成を考えて」 |
| **design** | UI/UX設計・デザイン方針 | 「デザインの方向性を決めて」「UI設計して」 |
| **estimator** | 工数・費用・スケジュール見積もり | 「見積もりして」「いくらかかる？」「工数を出して」 |
| **proposal-creator** | 提案書（PowerPoint）の作成 | 「提案書を作って」「提案書を仕上げて」 |

## 推奨ワークフロー

```
1. market-researcher → クライアント調査（CLIENT_CONTEXT を生成）
2. engineer          → 技術設計（技術スタック・DB・API設計）
3. design            → UI/UX設計（カラー・レイアウト・画面構成）
4. estimator         → 工数・費用見積もり
5. proposal-creator  → PowerPoint提案書の生成
```

各スキルは前のスキルの出力（CLIENT_CONTEXT など）を自動的に引き継ぎます。

## 別途インストールが必要なスキル

**pptxスキル**（Anthropic提供）が `proposal-creator` の実行に必要です。
ライセンス制約により本プラグインには含まれていません。
チームメンバーは別途インストールしてください。

## スキルの連携イメージ

```
market-researcher
  └─ CLIENT_CONTEXT ──→ engineer
                    ──→ design
                    ──→ estimator
                    ──→ proposal-creator
                              └─ pptx（別途インストール）
```
