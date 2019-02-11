# Takashi Ando Portfolio

## プロフィール

現在はヘルスケアサービスを提供するスタートアップ企業で、主にIoTデバイスファームウェア開発業務に従事。ソフトウェア開発のみならず、試作基板設計/実装、データ分析、ツール開発、生産管理等、幅広い業務を担当しています。

過去実績も含めた経験領域としては、ドライバポーティングや下位ミドルウェア、ツール開発、テスト、CI環境インフラ構築、工場生産ライン効率化等幅広く経験しており、常に人数×工数の削減を意識した効率化を念頭に置いて業務を遂行します。

Pythonを用いたデータ解析や機械学習、Flaskを用いたWebアプリケーション開発等、業務としては未経験の分野に対しても意欲を持ちながら学習を継続しています。

## 略歴

| Date range | Jobs |
|:----|:----|
| 2002.04-2006.06 | N社向け心電計開発 |
| 2006.09-2016.09 | T社 民生用映像機器等自社製品開発 |
| 2016.10-2018.03 | S社/O社向け 撮像装置開発 |
| 2017.09-2019現在 | S社 ヘルスケアIoT製品/サービス開発 |

## スキル

C/C++ / Python / TypeScript / Javascript / Node.js / Linux / Git / Mercurial / SVN / Plantuml / Circuit Prototyping / vim

## 主な個人的成果物

ほとんどがNode.jsやPythonで書いたものです。

### オリジナル太陽光発電監視システム

自宅の庭に架台を作り、太陽光パネルと蓄電池を設置しました。発電状況がWeb経由で監視できたら面白いのではないかと思い、充放電コントローラからデータを引き抜くPythonモジュールを作成し、Raspberry PiのデーモンがオンラインのDBにデータを記録、可視化したデータをブラウザで閲覧可能にしました。

下記は、太陽光パネル架台制作を手伝う娘の図。

![](https://farm1.staticflickr.com/778/23246846115_6b302c0b24_z_d.jpg)

#### Webモニタ (HTML/CSS/JavaScript)

収集した発電量データを可視化します。[リンク先](https://grid.uribou.tokyo/)にて閲覧可能です。

[![](https://farm5.staticflickr.com/4209/35086175820_e43aa99a9d_z_d.jpg)](https://grid.uribou.tokyo/)

#### データロガー (Python)

発電量データをDBに記録するデーモンです。[github](https://github.com/dodo5522/solar_monitor)に公開しています。

あるイベントをトリガーにして、接続機器の電源を自動OFFしたり、状況をTwitterに呟いたりする機能を後に追加しましたが、あまり役に立っていません…。

#### 充放電コントローラドライバ (Python)

以下のようなデータを充放電コントローラから抜き出すPythonモジュールです。[PyPi](https://pypi.org/project/tsmppt60-driver/)に公開しています。

```
{'Amp Hours': {'group': 'Counter', 'unit': 'Ah', 'value': 18097.9},
 'Array Current': {'group': 'Array', 'unit': 'A', 'value': 1.4},
 'Array Voltage': {'group': 'Array', 'unit': 'V', 'value': 53.41},
 'Battery Voltage': {'group': 'Battery', 'unit': 'V', 'value': 23.93},
 'Charge Current': {'group': 'Battery', 'unit': 'A', 'value': 3.2},
 'Heat Sink Temperature': {'group': 'Temperature', 'unit': 'C', ...},
 'Kilowatt Hours': {'group': 'Counter', 'unit': 'kWh', 'value': 237.0},
 'Target Voltage': {'group': 'Battery', 'unit': 'V', 'value': 28.6}}
```
