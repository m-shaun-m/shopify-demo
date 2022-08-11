# shopify-demo
shopifyの環境構築をする

- Shopifyで推奨されているCLIは、「Shopify Theme Kit」「Shopify CLI」の2つ
- Shopify CLIは、「Shopify Theme kit」に「Online Store 2.0」対応を加えたもの
- Online Store2.0に対応したテーマを開発する想定のため、「Shopify CLI」を採用する

## Shopify CLI インストール
```
brew tap shopify/shopify
brew install shopify-cli
```

## バージョン確認
```
shopify version
```

## ストア接続
```
shopify login --store [ストア名].myshopify.com
```

## テーマのダウンロード
※ 作業ディレクトリの作成・移動しておく
```
shopify theme pull
```

現在のストアに存在しているテーマの一覧が表示される
選択してEnter！！
```
? Select a theme to pull from (Choose with ↑ ↓ ⏎, filter with 'f')
> 1.  Dawn [live]
```

## テーマのプレビュー
```
shopify theme serve
```
> Serving .  
┃  
┃ Please open this URL in your browser:  
┃ http://127.0.0.1:9292  
┃  
┃ Customize this theme in the Online Store Editor:  
┃ https://[ストア名].myshopify.com/admin/themes/128486244595/editor  
┃  
┃ Share this theme preview:  
┃ https://[ストア名].myshopify.com/?preview_theme_id=128486244595  
┃  
┃ (Use Ctrl-C to stop)

上から順に、
1. 開発テーマリンク。リアルタイムで変更をプレビューできる
2. オンラインストアエディターへのリンク
3. プレビューリンク。他の人に共有することが可能

## テーマのアップロード
```
shopify theme push
```

## 参考
[Shopify CLIでローカル開発環境を構築する - ヒャクシル](https://siru.100you.co.jp/shopify-local-development/)