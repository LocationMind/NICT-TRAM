# NICT-TRAM project
- 研究開発課題名： **ウイルス等感染症対策に資する情報通信技術の研究開発**
- 課題C: アフターコロナ社会を形成するICT
- 副題: 多様な都市活動を支援する予測情報共有型 時空間リソース有効活用技術の研究開発

## member 
- （代表研究者）　株式会社アイ・トランスポート・ラボ
- （研究分担者）　東京大学
- （研究分担者）　東北大学
- （研究分担者）　LocationMind株式会社

## Purpose
- 本研究開発項目では，疑似的に人々の移動のビッグデータを作成する手法を開発する
- 疑似的なデータではあるものの，既存統計データとの比較等を通じて，どのような特徴をマッチングすべきか，応用技術開発への影響等を考慮して評価しながら作成する
- 最終的には，仮想な都市活動のオープンなシミュレーションデータベースを構築し，研究者・事業者の応用的分析技術の開発加速に貢献

## Direction 
```
人流ビッグデータから構築された生成AIを用いて、人の流動や滞留状況（パーソナルモビリティデータ）を疑似的に生成する
その際、人口分布や交通ネットワークデータなどを組み合わせ、充分なリアリティを持つ疑似データを生成する
```

1. 個人属性（年齢性別など）とその分布を表現する夜間人口分布データを所与とする当面、合成データ作成では、利用可能なビッグデータの制約から、個人属性を考慮せず単純な夜間人口分布データを利用する
2. 生成AIを利用して、個々の人々の移動（トリップ）・滞留行動を一定時間間隔で生成する. その際、上記夜間人口分布データを基に居住地を決定する
3. なお、生成AIは、個々の人々の移動（トリップ）・滞留行動のパターンを、人流ビッグデータから学習する
4. 移動・滞留行動には、通勤・通学、買物等のような日常的な活動内容と合わせて、出張や観光などの頻度の低い移動も含まれる（生成されるケースも少ない）。移動目的は、訪問頻度、訪問施設（地区）のタイプなどから推定されるが、当面は、データの前処理にかけられる時間の制約から、通勤通学、その他の2分類となっている。
5. 移動行動（トリップ）に対して、移動ルートと利用交通モードが推定される. 移動ルートや交通モードは、当該トリップ（OD）に対応した実際の人流データを元に推定される

## Generated Data
- data specification 
  - 5000 samples 
  - 1 hour interval
  - CSV text 
  - header: 1 row
  - delimiter: comma
- CSV layout 
  1. uid (string) 
  2. lat (double)
  3. lon (double) 
  4. tiime (timestamp) 
- download (gz) 
  - [sample file](pseudo_data_sample.csv.gz)

## License 
- CC BY-SA 
- 生成モデルの学習データ提供元：ジオテクノロジーズ株式会社
