# Yahoo知恵袋 順位チェッカー

検索キーワードでYahoo知恵袋が10位以内に表示されるかをチェックするツールです。

## 🚀 使い方

### 1. Google Custom Search APIの設定

1. [Google Cloud Console](https://console.cloud.google.com/) にアクセス
2. プロジェクトを作成または選択
3. Custom Search API を有効化
4. APIキーを作成
5. [Programmable Search Engine](https://programmablesearchengine.google.com/) で検索エンジンを作成
   - "Search the entire web" を選択
   - 検索エンジンID (cx) をメモ

### 2. ツールの使用

1. `chiebukuro-rank-checker.html` をブラウザで開く
2. APIキーと検索エンジンIDを入力
3. チェックしたいキーワードを1行に1つずつ入力
4. 「チェック開始」ボタンをクリック

## 📊 機能

- **複数キーワード一括チェック**: 複数のキーワードを一度にチェック
- **リアルタイム結果表示**: チェック中に結果をリアルタイム表示
- **統計情報**: チェック済み数、狙い目キーワード数、成功率を表示
- **CSV出力**: 結果をCSVファイルでダウンロード
- **レスポンシブデザイン**: PC・スマホ両対応

## 🎯 判定基準

- **◎ 狙い目**: Yahoo知恵袋が10位以内に表示
- **圏外**: Yahoo知恵袋が10位以内に見つからない

## 📝 出力形式

- キーワード
- 順位（1-10位 または 圏外）
- ステータス（◎ 狙い目 または 圏外）
- 該当するYahoo知恵袋のURL

## ⚠️ 注意事項

- Google Custom Search APIは1日100回まで無料
- APIキーはローカルでのみ使用（セキュリティ上、公開サイトでは使用しないでください）
- レート制限により、リクエスト間に100ms の間隔を設けています

## 🔧 今後の拡張予定

- Bing Search API対応
- SerpAPI対応
- サーバーレス化（APIキー隠蔽）
- スプレッドシート連携
- 自動定期実行機能
