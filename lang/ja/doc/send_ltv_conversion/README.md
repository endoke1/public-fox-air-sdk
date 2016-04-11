## LTV成果計測の詳細

######<アプリ内でLTV計測を行う（広告主端末IDあり）><br>
アプリ内部の成果に、広告主端末ID（会員IDなど）を含める事ができ、これを基準とした成果計測が行えます。

	ad.sendLtvWithAdid(成果地点ID, “広告主端末ID”);


成果地点ID(必須)：管理者より連絡します。その値を入力してください。

	ad.addParameter(“パラメータ名”, “値”);


▼ オプション

|パラメータ名|概要|
|:------|:------|
|AdLtvManager.PARAM_SKU|Stock Keeping Unit(商品管理コード)<br>（半角英数字32文字まで）<br>商品の在庫管理する際に使用してください|
|AdLtvManager.PARAM_PRICE|Price<br>（整数値　日本円）<br>売上額を管理する際に使用してください。|
|AdLtvManager.PARAM_CURRENCY|Currency<br>（半角英字3文字の通貨コード）<br>通貨別で課金額を集計する際に使用してください。<br>通貨が設定されていない場合、PriceをJPY(日本円)として扱います。|
|任意でパラメータを加える事も可能です。|ad.addParameter (“任意のパラメータ名”, 値);<br>※1アンダースコア（”_”）をパラメータ名の先頭に記述しないでください。<br>※2同一パラメータ名を記述した場合は、後者が有効となります。<br>※3 半角英数字以外は使用できません。|

＜オプションの使用例＞

```as3
	ad.addParameter (AdLtvManager.PARAM_SKU, “ABC1234”);
```

---
[トップ](/lang/ja/README.md)