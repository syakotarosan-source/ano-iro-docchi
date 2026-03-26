# ano-iro-docchi[README.md](https://github.com/user-attachments/files/26263056/README.md)
# ギャングカラー検索＆作業カウンター

GitHub Pages ですぐ公開できる、単一 HTML のアプリです。

## 入っている機能

- ギャング名、色名、別名、略称での検索
- 修理カウンター
  - 1台ごとに 1〜8か所で記録
- 色替えカウンター
  - 1台ごとに 1〜4か所で記録
- 修理／色替えの内訳表示
- 合計台数、合計か所数の表示
- 履歴表示
- ひとつ戻す
- リセット
- localStorage 保存
  - ブラウザを閉じても記録が残ります

## GitHub Pages で公開する手順

1. GitHub で新しい Repository を作成
2. このフォルダの `index.html` をアップロード
3. Repository の `Settings` を開く
4. 左メニューの `Pages` を開く
5. `Build and deployment` の `Source` を `Deploy from a branch` にする
6. Branch を `main`、Folder を `/ (root)` にする
7. `Save` を押す
8. 数分後に公開 URL が発行されます

## データを追加する場所

`index.html` の中にある `gangData` を編集してください。

```js
const gangData = [
  {
    name: 'Fisher（青ギャング）',
    primary: 'アノダイズドブルー（カメレオン）',
    secondary: '未設定',
    pearl: '未設定',
    wheel: '未設定',
    keywords: ['fisher', 'フィッシャー', '青', 'ブルー']
  }
];
```

## データ追加例

```js
{
  name: '新しいギャング名',
  primary: 'メインカラー',
  secondary: 'サブカラー',
  pearl: 'パールカラー',
  wheel: 'ホイールカラー',
  keywords: ['検索用ワード1', '検索用ワード2', '略称']
}
```

## 補足

- 検索は部分一致です
- 例: `青`, `ブルー`, `Fisher` でもヒットします
- さらに検索ワードを増やしたい場合は `keywords` に追加してください

