#NichanBbsConnector

##概要
にちゃんねる互換BBSのsubject.txtやdatの取得を外部クラスライブラリ化するためのテストアプリ兼クラスライブラリのサンプルアプリ。
後日、クラスライブラリをDLLとして配布予定


##趣旨
* したらばドメイン移転で発生した各種ツールでの読み込み不全を解消することをミニマムサクセスとし、以下の機能実装を予定しています。

  - 実装済み
     - データ取得のURL、subject.txt、datファイル定義の外部XML化
     - Webアクセス部分の非同期化
     - インスタンス内にsubject.txtとdatファイルの内容を保管
     - 差分レス取得
     - 更新チェック

  - 未実装
     - データ取得部分のクラスライブラリ化
     - 取得完了イベントの実装(非同期コール出来るので不要？)
     - レス書き込み
     - 書き込みエラーチェック

  - 要望があれば
     - 取得データのパーシング機能の単体提供


##更新履歴

* 2014/3/8 α2版ソース  
  - datファイルのリストへの格納  
  - dat取得時のGzip対応  
  - サンプルUIに板履歴を追加(イベントは未実装)  
  - readmeを整理  

* 2014/3/4 α版ソース  
  - URL解析(板URL or スレッドURLからの解析)
  - datURLの生成  
  - スレッドURLからスレッドIDを抜いたURL
  - 板名の取得
  - スレタイの取得
  - subject.txtの取得およびリストへの格納  
  - XMLより板定義情報を取得する機能を実装(ID周りのみ未実装)
  - URL解析部分の非同期化
  - 上記機能を使用するサンプルアプリの実装
