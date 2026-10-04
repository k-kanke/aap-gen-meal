# aap-gen-meal

家族の昼食・夕食予定表。`ai-app-platform` の最初の Acceptance Test となるリファレンスアプリ。

- 家族4人 × 約10日 × 昼/夜 × ○/×/未回答。最後に入力された状態が正。
- スマホ向け UI、「みんなの一覧」で未回答が黄色で分かる。

## App Contract(ai-app-platform)

| 項目 | |
|---|---|
| 起動 | `npm start` |
| ポート | 環境変数 `PORT` |
| ヘルスチェック | `GET /healthz` |
| データ | `DATA_DIR`(= `/data`)の `meals.json` のみ |

```sh
npm test
PORT=8080 DATA_DIR=/tmp/meal-data npm start
```

`ai-app-platform/agent-runtime/templates/meal/` はこのリポジトリのコピー(スタブ Agent 用)。
