# Curriclum Vitae

最終更新 2019/11/12

## Basic

|key|value|
|---|-----|
|Name|清水　陽平 (Yohei Shimizu)|
|Qiita|https://qiita.com/digineko|
|GitHub|https://github.com/diginecorona|

## School/Job history

- 履歴書参照

## Summary

- 機械学習エンジニア
- 機械学習システムの開発、その他データベース周辺のバックエンド開発がメイン
- 現在株式会社iettyで機械学習エンジニアとして活動中（3社目）
- 元々はメカトロニクスエンジニア（電子工学）であり、医療機器の開発を行っていた
- 学生時代も医用工学分野に身を置き、主に糖尿病について研究していた

## Skills

- **言語**
  - Python
  - Ruby
  - Go
  - MySQL
  - JavaScript / Node.js
- **フレームワーク**
  - Ruby on Rails

- **ツール、その他**
  - Amazon Web Services
      - CodeBuild
      - CodeCommit
      - RDS
      - VPC
      - Lambda
  - Google Cloud Platform
    - Compute Engine
  - Docker
  - Re:dash
  - Node-RED
  - JupyterLab
  - Slack
  - GitHub
- **自然言語**

  - 日本語
    - ネイティブ
  - 英語
    - かんたんな日常会話ができる
    - 言語、ライブラリ等のドキュメントを英語原文で読解

## Storong points

- 自己評価
    - 興味を持って何事もやってみるという姿勢がある
- 周囲からの評価
    - フットワークが軽い
    - 物事を細部まで突き詰める姿勢がある
    - 試行錯誤のサイクルが速いので成長が速い

## Job details

### 株式会社ietty: 2019/04~

| 期間                        | 内容                                                         |
| :-------------------------- | :----------------------------------------------------------- |
| 2019/04<br />~<br />2019/06 | 1. 自社サービス用API作製<br />2. 機械学習モデル改良<br />3. 機械学習周辺システム構築、データ出し<br /> |
| 2019/07<br />~<br />2019/09 | 4. 賃貸物件棟名寄せ<br />5. 自社サービスデータ取得用クエリ作製<br /> |
| 2019/10<br />~              | 6. 物件データパース用batch処理作製                           |

#### 概要

2019年4月に機械学習エンジニアとして中途入社。

機械学習分野を中心に、データベース周辺のバックエンドエンジニアリングの業務にも幅広く携わる。

##### 各業務の概要

1. **自社サービス用API作製（使用スキル: Ruby / Ruby on Rails）**

   自社サービスチャット接客アプリに下記の改良を加えた。

   - 物件最寄り駅の希望駅数を増加
   - ユーザーへの提案物件に詳細条件（希望する設備）を追加

2. **機械学習モデル改良（使用スキル: Python）**

   従来の家賃価格予測モデルに特徴量を追加して予測精度を改良した。

3. **機械学習周辺システム構築、データ出し（使用スキル: Python）**

   家賃価格予測モデルを利用して「物件家賃シミュレーション機能」を果たせるシステムを構築した。

   また、駅、築年数、間取りを軸にした家賃予測価格データを作成し、マーケティングチームの交渉材料として使用した。

4. **賃貸物件棟名寄せ（使用スキル: Python/CodeBuild）**

   ユーザーの希望条件に合致した賃貸物件を自動に複数提案するサービスにおいて、棟（建物）ごとのグルーピングを行っていなかった。同じ棟の違う部屋番号の賃貸物件を連続して提案し、ユーザーの満足度を低下させていた。その対応策として、棟のグルーピングを行った。

   データベース上の物件データの表記揺れが多数あったため、文字列操作や住所、座標を組み合わせてグルーピングを行った。名寄せの結果をCodeBuildを使ってDB上に書き込む定期batch処理を作製した。

5. **自社サービスデータ取得用クエリ作製（使用スキル: MySQL / Re:dash）**

   法人ユーザー向けの物件検索サービスを構築する中で、検索物件に関連するデータ（類似物件など）を出力するクエリを作製した。

6. **物件データパース用batch処理作製（使用スキル: Go / Docker）**

   住所データを位置情報取得APIに送り、レスポンスデータをパースしデータベースに保存するbatch処理を作製した。また、CodeBuild上で使用するDockerイメージを作製した。

##### その他

定期的な業務として下記に取り組んでいた。

- データベースを改造するためのマイグレーションファイル作製（使用スキル: Ruby/Ruby on Rails）
- サービスデータ集計のためのクエリ作製使用スキル: MySQL/Re:dash）

基礎研究として、下記に取り組んでいた。

- 設備画像解析による画像カテゴライズ

### 株式会社セラク: 2018/10 ~ 2019/03 

| 期間                        | 内容                                   |
| --------------------------- | -------------------------------------- |
| 2018/10<br />~<br />2019/03 | 1. 【設備LCMサービス】開発プロジェクト |

#### 概要

データサイエンティストとして中途入社。

#### 各業務の概要

1. **【設備LCMサービス】開発プロジェクト（使用スキル: JavaScript / Node.js / Node-RED）**

   冷蔵庫から稼働情報を取得する大手コンビニストア向けIoTシステム開発に携わった。

   担当セクションは、詳細設計 / 実装。

   システムの下記フローの通りに稼働する。

   1. Node-REDがインストールされたLinuxマシンに冷蔵庫から稼働状況を示すバイナリデータが送信される

   2. Node-RED上ではNode.jsが稼働しており、Node.js上でバイナリデータの解析を解析し数値・文字列に変換する
   3. 変換した結果をクラウドサーバーに送信する

## 業務外活動

- Kaggle
