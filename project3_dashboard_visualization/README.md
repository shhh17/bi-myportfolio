# 広告運用データを活用したダッシュボード可視化

## 概要

広告運用に関するパフォーマンスデータは多くの媒体に分散しており、日々の状況把握や分析に工数がかかっていました。  
そこで、**BigQueryやGoogle スプレッドシートに格納されたデータを統合し、Looker Studioで視覚的に整理する**ことで、チーム内での共有や意思決定のスピード向上を目指しました。  
また、これまで業務の中で培った**データ整形の知見や自動化スクリプトの活用スキルを活かし、手動作業の軽減と指標の一元化**を実現しています。

---

## 目的・背景
広告運用に関するデータを可視化し、日々のパフォーマンスの傾向や異常値の早期発見、改善のためのヒントを得ることを目的に作成しました。

---

## 特徴

- 複数媒体の広告データを統合して可視化
- 重要指標（CPA・CV・COSTなど）のカード型表示
- フィルタで日付・サービス・プロモーションの切り替えが可能
- 成果の高いプロモーションをランキング形式で表示
- Google Apps Script（GAS）によるデータ統合処理の自動化（一部）

---

## Google スプレッドシート構成

| シート名 | 内容 |
|----------------------|------------------------------------------|
| `campaign_report`     | BigQueryから取得した自動連携データ（日別） |
| `manual_input_sample` | 手入力による補足データ（売上・粗利など）     |
| `merged_output`       | 上記2つのデータを統合し、Looker Studio用に整形。 |

---

## 使用技術
- **BigQuery（スプレッドシートのデータコネクタ経由）**
- **Google スプレッドシート**
- **Google Apps Script**  
ChatGPT（AI）によるコード補助を活用し、非エンジニアでも高度な処理を実現
- **Google Looker Studio**

---

## 利用対象者
- 広告運用に関わるメンバー（ディレクター、クリエイター、マネージャー等）
- 数値変化や成果を素早く把握したいマーケター
- 自社内で広告ダッシュボードの導入を検討している方

---

## 活用による効果
- 日別・媒体別の広告成果の把握が容易に
- プロモーション単位での成果比較が可能に
- 重要指標に絞った可視化で、定例レポート作成の工数削減
- 数値に基づいた意思決定の迅速化

---

## ファイル構成（GAS）

| ファイル名 | 内容 |
|----------------------|------------------------------------------|
| `mergeCampaignDataFromURLs.gs` | データ統合処理（`campaign_report` + `manual_input_sample` を統合し、Looker Studio 連携用に整形） |

---

## 実際のGoogle スプレッドシート・ダッシュボードリンク

- [Looker Studio ダッシュボード（閲覧用）](https://lookerstudio.google.com/s/oaAPTnja_gA)
- [Looker Studio 連携用統合整形データ（閲覧用）](https://docs.google.com/spreadsheets/d/1sXkrQnvFnpgZZ59Nj7ZZx31jHl2xG4sHTe-hNbiy4ho)
- [BigQueryより抽出した全広告データ（閲覧用）](https://docs.google.com/spreadsheets/d/1jVwHuKIRYZ4c2xTy48O6b-2bLQklpmPJ5-T4epUCFss)
- [広告キャンペーン別手入力データ（MCV・CV・売上・粗利）（閲覧用）](https://docs.google.com/spreadsheets/d/1sXkrQnvFnpgZZ59Nj7ZZx31jHl2xG4sHTe-hNbiy4ho)
