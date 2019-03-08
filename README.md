# expect-ssh-auto-sftp.exp

### expectを使ってSFTP通信シェルスクリプト

expectを使って対話式にAサーバとBサーバでSFTP通信を自動化します。

前提条件は、上記を参考にしてexpectをインストールしてください。

テストした環境では、yumでインストールしました。[CentOS release 6.10 (Final)]


> Linuxの対話がめんどくさい?そんな時こそ自動化だ！-expect編-  
> https://qiita.com/ine1127/items/cd6bc91174635016db9b


を参考にして作成。ありがとうございます！

[使い方]

(引数/戻り値)  
1：リモートホスト名  
2：パスワード  
3：リモートホストの公開ディレクトリ名  
4：取得するファイル名  
戻り値：標準出力で「end: sending "exit\n"」が出力される。

[コマンド例]

  sudo /usr/bin/expect /usr/local/src/expect-ssh-auto-sftp.exp user@xx.xx.xxx.xxx password path/to/remote wantedFileName
