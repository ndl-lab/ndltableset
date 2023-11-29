# NDLTableSet

NDLTableSetは以下のURLから公開しています。<br/>
現在(2023年11月)の最新バージョンは1.0であり、750画像分のデータセットとなります。<br/>

ICDAR2019_cTDaR形式：
https://lab.ndl.go.jp/dataset/ndltableset/icdar/NDLTabNet_ICDAR2019_cTDaRformat_ver1.zip

PascalVOC形式：
https://lab.ndl.go.jp/dataset/ndltableset/pascalvoc/NDLTabNet_PascalVOCformat_ver1.zip


## 1. データセットの説明

NDLTableSetは、国立国会図書館デジタルコレクション[*http://dl.ndl.go.jp/*](http://dl.ndl.go.jp/)が提供している、
著作権保護期間満了資料の画像データの中から自動的に切り出された表画像に対して、表の構造を記述したアノテーション情報を付与して公開したデータセットです。

NDLTableSetを機械学習に利用することで、紙の資料を撮影した画像（非ボーンデジタルな資料）に含まれる表領域に対して、表構造推定用モデルを開発することができます。

利用例については、[ndltsr](https://github.com/ndl-lab/ndltsr)のリポジトリを参照してください。

先行研究である[ICDAR2019_cTDaR](https://github.com/cndplab-founder/ICDAR2019_cTDaR)データセットのアノテーション方法に倣った「ICDAR2019_cTDaR形式」と、
よりアノテーションツールや機械学習分野で汎用的に使われているフォーマットとして、利活用を容易にするために加工した「PascalVOC形式」の2通りの形式で配布しています。

***ICDAR2019_cTDaR形式の抜粋***
```
<?xml version="1.0" ?>
<document filename="1016581_112_0.jpg">
  <table>
    <Coords points="0,0 0,732 1122,0 1122,732"/>
    <cell end-col="2" end-row="2" start-col="2" start-row="2">
      <Coords points="679,172 679,204 773,172 773,204"/>
    </cell>
    <cell end-col="1" end-row="4" start-col="1" start-row="4">
      <Coords points="432,291 432,322 475,291 475,322"/>
（以下略）
```
***PascalVOC形式の抜粋***
```
<annotation>
  <filename>img/1016581_112_0.jpg</filename>
(中略)
  <object>
    <name>cell</name>
    <truncated>0</truncated>
    <occluded>0</occluded>
    <difficult>0</difficult>
    <bndbox>
      <xmin>679.0</xmin>
      <ymin>172.0</ymin>
      <xmax>773.0</xmax>
      <ymax>204.0</ymax>
    </bndbox>
    <attributes>
      <attribute>
        <name>end-col</name>
        <value>2.0</value>
      </attribute>
      <attribute>
        <name>end-row</name>
        <value>2.0</value>
      </attribute>
      <attribute>
        <name>start-col</name>
        <value>2.0</value>
      </attribute>
      <attribute>
        <name>start-row</name>
        <value>2.0</value>
      </attribute>
      <attribute>
        <name>rotation</name>
        <value>0.0</value>
      </attribute>
    </attributes>
  </object>
（以下略）
```
## 2. データセットの権利
「PDM（パブリック・ドメイン・マーク）」&lt; https://creativecommons.org/publicdomain/mark/1.0/deed.ja &gt;

※本データセットは著作権保護期間満了資料のみを加工して作成しています。

NDLTableSetデータセットは、自由な二次利用が可能です。ただし、二次利用に際しては、次の事項へのご配慮をお願いいたします。これらのお願いは法的な契約ではありませんが、できる限りご留意の上でご利用くださるよう、ご協力をお願いします。

- データを編集・加工等して利用する場合は、それを行ったことを記載してください。編集・加工等を、元となる作品・原資料の作者や当館が行なったかのような態様で公表しないようご留意ください。
- 当該データが自由に二次利用可能であることの表記を保持してください。
- 元となる作品や、その作者の名声を傷つける形での利用は行わないようご留意ください。また、元となる作品に関わる文化やコミュニティへの配慮を行ってください。
- 著作権以外の権利（著作者人格権、著作隣接権、肖像権、パブリシティ権、プライバシー権、商標権等）にも留意し、関連法令を遵守してください。
- 論文等に利用する場合には、先行研究や後続研究と比較を容易にするためNDLTableSetデータセットとバージョンの明記にご協力ください。

## 3. データセットに含まれる画像の出典情報
[metadata.csv](./metadata.csv)を確認してください。
