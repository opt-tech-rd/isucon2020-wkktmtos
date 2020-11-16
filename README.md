# isucon2020-wkktmtos

## まずは

- `yarn install`
- `go build`
- `yarn format`

## ディレクトリ構成

```text
- middleware: ミドルウェア設定ファイル. Docker関係もここかな
- scripts: デプロイスクリプトとか. 作りはしたけど基本は package.json の scripts でまかないたい
- webapp: Webアプリのソースコード
```

いちいち middleware に行くのが面倒なので、 docker-compose.yml はルートに置きたい

## npm scripts tips

### npm-run-all

このパッケージのおかげで、format コマンドみたいな書き方ができる。

- run-s: 直列実行
- run-p: 並列実行

```json
"scripts": {
 "format": "run-s format:*",
 "format:prettier": "prettier --write .",
 "format:goreturn": "goreturns -l -w ."
},
```
