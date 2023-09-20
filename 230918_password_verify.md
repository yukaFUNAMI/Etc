
## パスワードがハッシュ値で保存されているサイトのSQLインジェクションによる認証回避の練習問題
https://qiita.com/ockeghem/items/787f74801a24e1fc6960#%E7%99%BA%E5%B1%95%E5%95%8F%E9%A1%8C2023918%E8%BF%BD%E8%A8%98

こちらの問題をやってみた。

![1](https://github.com/yukaFUNAMI/Etc/assets/6504854/c530d024-8356-44d2-93c9-5183e4c1a57b)

うーん、まだSQLiをちゃんとわかってない。

あとは解答で勉強するぞー！



## パスワードがペッパー付きハッシュ値で保存されているサイトのSQLインジェクションによる認証回避の練習問題
https://qiita.com/ockeghem/items/0f3b09a0f413bdd39bd5

おかわりが出たのでそちらもやってみた。
Sqlmapでダンプをとるとこのようになっている。（３ユーザ自前で追加）

![image](https://github.com/yukaFUNAMI/Etc/assets/6504854/1aaad090-c5ee-4ff0-948f-17ec83b9f75f)

![image](https://github.com/yukaFUNAMI/Etc/assets/6504854/9fa650cb-1791-4d15-a07c-9b2eed06f9d1)

Interceptしてno1のadminのHash値でno2のtestのパスワードでOK。アドミンのSessionがくる。

![image](https://github.com/yukaFUNAMI/Etc/assets/6504854/3e7cc844-1315-49fa-bb59-a7f252e7acab)

![image](https://github.com/yukaFUNAMI/Etc/assets/6504854/713c23be-cd27-41fd-8143-49c311650cdb)

普通に複文で全部TestのHashにUPDATEすればいいとおもったが、できなかった。（全員同じパワードになるので楽）
