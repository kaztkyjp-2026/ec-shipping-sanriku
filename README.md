# EC出荷オペレーションツール（ec-shipping-sanriku）

Amazon FBM（自己発送・2店舗）と楽天市場の出荷業務を1つの画面で処理するブラウザツールです。

**🔗 ツール：https://kaztkyjp-2026.github.io/ec-shipping-sanriku/**

## 対応モール

- **Amazon**（FBM・2店舗）
- **楽天市場**

## 主な機能

| タブ | 機能 |
|---|---|
| STEP 1 | Amazon未出荷注文レポート（TSV）→ ヤマトB2クラウド取込用CSV生成 |
| STEP 1 | ピッキングリスト・梱包発送明細の印刷とPDF保存（total＋注文別を1ファイルに） |
| STEP 1 | ネコポス以外（ssa-ship-method）の自動除外・警告表示 |
| STEP 2 | B2クラウド発行済みデータCSV → Amazon出荷通知TXT生成 |
| STEP 1（楽天市場） | RMS通常購入データCSV → 楽天市場ピッキングリスト（印刷／PDF保存）＋B2クラウド取込用CSVへ統合 |
| STEP 1（楽天市場） | Amazon MCF注文（ひとことメモ CONSUMER-）の自動除外・警告表示 |
| STEP 2（楽天市場） | 発送完了報告用テンプレート × B2発行済みデータ → 楽天市場発送完了報告CSV生成 |

- 出力ファイルはすべてブラウザのダウンロードとして直接保存（フォルダ選択なし）
- Shift-JIS の入出力に完全対応（クオート内改行を含むRMS CSVにも対応）
- 商品サムネイル（sku-images.json）付きピッキングリスト（Amazon／楽天市場とも）
- G番号は接頭辞でモールを区別（Amazon: A-001 ／ 楽天市場: R-001。B2記事欄も同形式）
- 各STEP内の「Amazon／楽天市場」スイッチでモールを切り替え（タブは3つ）

## 動作環境

Chrome / Edge。ブラウザ完結・サーバー不要（入力データは外部に送信されません）。

## 使い方

[📖 使い方マニュアル](https://kaztkyjp-2026.github.io/ec-shipping-sanriku/manual.html)

## 由来

[ec-tools-jp/fbm-tool](https://github.com/ec-tools-jp/fbm-tool)（MIT License）をベースにした三陸フーズ仕様版です。
旧リポジトリ fbm-tool-sanriku から移送（楽天市場対応を機に改称）。

## ライセンス

MIT License © 2026 ec-tools-jp / kaztkyjp-2026
