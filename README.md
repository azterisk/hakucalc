# がいよう
東方二次創作ゲーム[ハクレイフロンティア](sitappa.com/hakurei_ss/)の便利(?)ツールです。
ステータスやダメージを計算してくれます。
アプリケーションは[こちら](https://azterisk.github.io/hakucalc/)

# つかいかた

## ざっくり

1. デッキ内のステータス修正カード（Pアイテムとか）の枚数を入力します。
2. キャラクタを登録するとHP、Power、ダメージなどが表示されます。
3. 必要に応じてPower修正のイベントやスキル・スペルの修正値、自機やエクステンドの有無を設定します。
4. "一括再計算"、"再計算"ボタンを押すとステータスやダメージの再計算が行われます。再計算をしないとカード枚数やイベントの変更が反映されません。

## Power修正イベントについて

スキルカードとエクステンド以外のPower修正を登録する入力エリアです。
エクステンドを適用する場合は代わりにキャラクタの"エクステンド"チェックを変更してください。
修正値は左上から順に適用されます。順番を変えたい場合は再入力してください。修正する予定は（今のところ）ないです。

"追加"ボタンを押すと、修正値を入力するエリアが追加されます。
基本的にはカードに記載の修正値を指定してください。（例："白狼天狗の太刀"の場合は"10"を指定）
"頼りになる弟狸"の計算はツールが勝手にやってくれます。
修正を自機にのみ適用する場合は"自機"チェックを変更してください。

"追加(倍率)"ボタンを押すと、修正値を％形式で入力するエリアが追加されます。
チルノや左扇などN倍するタイプの修正に使うことができます。
内部処理の都合上、以下のように指定してください。
- "チルノ"や"左扇"（Powerが2倍）は"+100%"を指定
- "日焼けしたチルノ"（Powerが1.5倍）は"+50%"を指定

"反撃"など修正値が不定の場合はがんばって計算してください。

## キャラクタについて

"HP"、"Power"、"Spell"に表示される値はステータス修正カードが適用されたあとの値です。
"Speed"は現状特に用法はないですがなんとなく表示してます。ステータス比較に使ってください。

"通常ダメージ"はPower修正に関わるすべての修正（イベント修正、スキル修正）が適用されたあとのダメージ値です。
下のカッコ書きは左から順に（Powerの値、スキルによる修正、イベントの修正（左上から））となります。
"スペルダメージ"は通常ダメージにスペル威力、スペル補正を加えたダメージ値です。
下のカッコ書きは左から順に（通常ダメージ、Spellの値、スペル修正）となります。

"スキル修正"にはスキルカードで適用される修正を入力してください。
内部処理が実際の処理と一部異なりますが、（これを書いてるVer0.24現在では）特に問題はないのでそのままにしてます。問題が出たら直します。
スキルフェイズに適用されるスキル以外のPower修正は現状エクステンドのみのはずなので違ってたら教えてください。直します。

"スペル修正"にはスペルの能力で適用される威力の修正値を入力してください。
基本的には"スペル攻撃力 = ?"のキャラクタの計算用に使います。
Ver0.24現在で関係あるのは"すみれこ"、"パチュリー"、"ゆゆこ(青、紫)"のはずです。
"ひな"も"スペル攻撃力 = ?"ですが（たぶん）関係ないです。そもそも検証していないのでよく分かりません。誰か検証してください。
使用時にPower修正されるタイプのスペル（"じょおん"など）の場合は代わりに"Power修正イベント"を使用してください。
