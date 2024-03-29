## GCN-with-LSTM (Graph Convolutional Networks with LSTM)
グラフ構造を畳み込むGCNをLSTMを使って改良する\

参照論文\
https://arxiv.org/pdf/1609.02907.pdf

GCN ではグラフを隣接行列とラプラシアン行列として表現する.\
そこでで単にこれらの行列を畳み込むのではなく,まず出力と入力\
の次元が同じLSTMにこれらの行列を通せば、よりグラフのつながりを\
表現できるのではないかと考えた。

データセットとしてはnetworkXに付属しているkarate_clubを使っている\

結果は以下のとおり

![](GCN_lstm_loss.png)

lstmを組み込んだほうが大幅に損失の減少が早くなる.\

### 今後
GCNではラプラシアン行列を用いる関係上、有向グラフの表現が難しいが、\
LSTMを用いれば、それもうまく表現できるかもしれない
