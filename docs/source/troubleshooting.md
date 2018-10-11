# トラブルシューティング

## Ubuntu MATEのロゴが出たまま起動しない

[動作確認](tutorial-operation-check-raspigibbon.html)にある終了方法に従って一度raspigibbon_standaloneを終了してください。

---

HDMI接続のディスプレイ接続時に[動作確認](tutorial-operation-check-raspigibbon.html)のようにraspigibbon_standaloneを起動すると起動処理が終わったと判断されず、Ubuntu MATEのロゴが出たままログイン画面に進みません。

v0.2で公開しているイメージファイルで発生する場合があります。

この問題はv0.3で修正されています。

## デバイスドライバがビルドできない・インストールできない

[v0.4のイメージ](https://github.com/rt-net/RaspberryPiGibbon/releases/tag/v0.4)を再インストールしてください。
書き込みの手順は[Wiki](tutorial-setup-raspberrypi.html)を参照してください。

最新版のデバイスドライバを取得するだけならば、[raspigibbon_driver_installer](https://github.com/Tiryoh/raspigibbon_driver_installer)をアップデートすることで対処できます。

---

Ubuntu MATE公式ではカーネルのヘッダファイルは配信されていません。
v0.3までのイメージではカーネルのヘッダファイルを手動で配置した状態で公開していました。

2017年2月にUbuntu MATEのカーネルがアップデートされました。これにより、カーネルのヘッダファイルと実際に起動しているカーネルのバージョンが一致せず、デバイスドライバがビルドできない・インストールできないあるいは正しく動作しないといった不具合が発生する場合があります。

v0.4でカーネルのヘッダファイルをダウンロードするスクリプト[`update-linux-headers`](https://github.com/Tiryoh/UbuntuMATE_image/blob/6b84068013b221bde67366258917eeefa5b12d60/scripts/update-linux-headers)を追加し、今後のバージョンアップにも対応できるようにしました。

v0.1,v0.2,v0.3で公開しているイメージファイルで発生する場合があります。

この問題はv0.4で修正されています。