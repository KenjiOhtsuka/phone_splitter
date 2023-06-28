* 固定電話の番号を市外局番と市内局番に分ける時に、市外局番がどこまでかを表すJSONです。
* 0120(着信課金機能), 050(特定IP電話番号)などの特殊な電話番号は含んでいません。
* 固定電話番号に自動的にハイフンを入れる目的で作成しました。

## 使い方

電話番号10桁のうち、市外局番がどこまでかを調べたい場合、以下のようにアクセスします。

たとえば、 033233XXXX が電話番号になっている場合、先頭の市外局番・市内局番の合計6桁をスラッシュで区切り、以下のようにアクセスします。

```
https://kenjiohtsuka.github.io/phone_splitter/0/3/3/2/3/3.json
```

次のような値が返ります。

```json
{"area_code":"03","area_code_length":2}
```

- area_code: 市外局番
- area_code_length: 市外局番の桁数

## 使用しているデータ

総務省のこちらのページで紹介されている固定電話の電話番号データを使用しています。
https://www.soumu.go.jp/main_sosiki/joho_tsusin/top/tel_number/number_shitei.html
