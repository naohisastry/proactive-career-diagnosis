# 提案型転職 5タイプ価値観診断ツール

> **「求人票に自分を合わせるな。いままでの経験で『役割』をつくる。」**  
> 40代・ミドルシニアがこれまでの経験を活かし、自らの強みから企業の課題を解く「提案型転職」を実践するための価値観診断Webアプリケーションです。

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?logo=github)](https://naohiro-s.github.io/proud-babbage/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Zero Config](https://img.shields.io/badge/Build-Zero%20Config%20(Pure%20HTML)-orange.svg)]()

---

## 🌟 プロジェクト概要

「条件検索型の転職市場」では、年齢や職務経歴の型にはめられ、ミドルシニアは構造的に不利な戦いを強いられがちです。  
本ツールは、10問のリアルな就業体験シナリオ（100点満点・按分配点）を通じて、回答者の潜在的な仕事の価値観と強み構造を可視化し、**「自分らしい提案書と面接スタンス」**を導き出します。

### ✨ 主な特徴
- 📱 **スマホファースト UI/UX**: 直感的なステップ進行、快適なカードUI、プログレスバー。
- 🛡 **完全匿名・端末内処理（Serverless / No DB）**: 回答データはサーバー等に一切送信されず、ブラウザローカルで安全に完結。
- 📊 **100点満点レーダーチャート**: Chart.jsを活用した動的5軸バランス可視化。
- 🔀 **選択肢シャッフル（順不同）**: 選択肢の位置バイアスを排除し、純粋な価値観を抽出。
- 🎯 **複数選択・按分配点ロジック**: 1問につき1〜2個選択可能（1個=10点、2個=各5点）。
- 🧬 **4つの強み構造パターン & 20通りのシナジー辞書**: 単一特化・二刀流シナジー・主軸＋補佐連携・多面統合バランサーを精密判定。
- 📤 **SNSワンタップ共有**: X（140文字最適化）・LinkedIn・クリップボードコピー対応。

---

## 🧭 5つの提案型転職タイプ（Archetypes）

| タイプ | 呼称 | キャッチコピー | 提案書の型 |
| :---: | :--- | :--- | :--- |
| **Type A** | **安定実行型** | 「明確な役割のもと、組織の安定運用と着実なリスク管理を支える信頼の守護者」 | 業務改善・安定運用シート（A4 1枚） |
| **Type B** | **専門追求型** | 「高度な専門知見と職人的スキルで、特定の難問を解き明かすスペシャリスト」 | 専門領域特化の技術・実務分析シート（2〜3枚） |
| **Type C** | **関係協働型** | 「対話を通じて人を巻き込み、チームの力で組織の壁を越えるコミュニケーター」 | 対話型・論点整理メモ（A4 1枚・アジェンダ形式） |
| **Type D** | **課題解決型** | 「企業の経営・業務課題を読み解き、仮説改善案で価値を示すソリューション提案者」 | 課題仮説＋改善アプローチシート（3〜5枚） |
| **Type E** | **事業創造型** | 「用意された枠を飛び越え、新しい事業と役割そのものを切り拓くパイオニア」 | 事業構想・新ポジション提案書（5〜10枚） |

---

## 🔬 診断・判定アルゴリズム

```
[ Step 0: 基本属性入力 ] ──> [ Step 1〜10: シナリオ設問 ] ──> [ スコア集計 (合計100点) ]
  (年代・在職年数・転職意向)     (順不同シャッフル / 1〜2選択)      (1選択=10点, 2選択=各5点)
                                                                       │
                                                                       ▼
                                                          [ 4つの強み構造判定 ]
                                                                       ├─ ① 単一特化型 (S1≧45 & 差≧20)
                                                                       ├─ ② 二刀流シナジー型 (差≦15 & S2≧25)
                                                                       ├─ ③ 多面統合バランサー型 (S1-S3≦12)
                                                                       └─ ④ 主軸＋補佐連携型 (標準構造)
                                                                       │
                                                                       ▼
                                                          [ パーソナライズド・レポート ]
                                                            ・レーダーチャート (Chart.js)
                                                            ・主副シナジー解説 (20通り)
                                                            ・転職処方箋 (提案書/面接/落とし穴)
                                                            ・属性別アンラーニング助言
```

---

## 🚀 GitHub Pages へのデプロイ手順（完全完結）

本リポジトリは **外部サーバーやビルドツール（Node.js / Webpack等）を一切必要としません**。  
`index.html` 1ファイルのみでCDN経由ですべて完結して動作します。

### 手順（約1分で公開完了）:

1. **GitHubリポジトリを作成し、コードをプッシュ**:
   ```bash
   git init
   git add .
   git commit -m "feat: Initial commit of Proactive Career Diagnosis Tool"
   git branch -M main
   git remote add origin https://github.com/<YOUR-USERNAME>/<YOUR-REPO-NAME>.git
   git push -u origin main
   ```

2. **GitHub Pages の有効化**:
   - リポジトリの **[Settings]** タブを開く。
   - 左側メニューの **[Pages]** を選択。
   - **[Build and deployment]** > **[Source]** で `Deploy from a branch` を選択。
   - **[Branch]** で `main` ブランチ、フォルダ `/ (root)` を選択して **[Save]** をクリック。

3. **公開完了**:
   - 数十秒〜1分程度で、`https://<YOUR-USERNAME>.github.io/<YOUR-REPO-NAME>/` にてWebサイトが即座に一般公開されます。

---

## 🛠 使用技術・ライブラリ

- **Markup / Script**: HTML5, Vanilla JavaScript (ES6+)
- **Styling**: [Tailwind CSS CDN](https://tailwindcss.com/)
- **Charts**: [Chart.js CDN](https://www.chartjs.org/)
- **Icons**: [Font Awesome 6.4.0 CDN](https://fontawesome.com/)
- **Fonts**: [Google Fonts (Noto Sans JP / Plus Jakarta Sans)](https://fonts.google.com/)

---

## 📄 License / ライセンス

- **Code**（HTML / CSS / JavaScript）: [MIT License](LICENSE)
- **Content**（文章・図表・分析結果・整理済みデータ）: [CC BY 4.0](LICENSE-CONTENT.md)
- 出典表示例 / Attribution: Naohisa Hashimoto, "proactive-career-diagnosis", https://naohisastry.github.io/proactive-career-diagnosis/
- 第三者の元データの権利は各発行元に帰属します。 / Third-party source data remain the property of their original publishers.
- **連動コラム**: [note.com 連載『【40歳からの転職】求人票は見るな！組織の課題を自ら解く「提案型転職」のススメ』](https://note.com)

© 2026 Naohisa Hashimoto
