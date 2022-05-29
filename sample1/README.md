# 概要
マインクラフトのサンプルアドオン開発方法についてと非常に単純なサンプル


# 前提
この手順はWindows10でのMinecraft統合版1.19.10で実施しています。


# 詳細
「Windowsボタン + R」で以下のパスへと移動します。
%localappdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang


上記フォルダを開くと開発中の下記リソースを配置できます。
- リソースパック
  - development_resource_packs
- ビヘイビアパック
  - development_behavior_packs 

上記フォルダには最初は何も存在していません。

開発時は名称は特に気にせずに適当に
リソースパックのフォルダにadditem_BPを、ビヘイビアパックのフォルダにadditem_RPを配置します。(additem_BPのadditem_RPに対する依存はuuidで記載されています。)

これだけでマインクラフトを再起動すれば利用できるようになります(あくまでも開発中の場合です。)

アドオンを試す場合には、 「新しく世界を作る」で作成します。
- 「ホリデークリエイターの特徴」にチェックを入れます。
- 「クリエイターモード」にします。
- プラグインで「リソースパック」と「ビヘイビアパック」から該当のアイコンを「有効化」できます。

あとはコマンドモードから以下のように呼び出すことで、今回アドオンで追加したアイテムを自分自身に付与することができます。
```
/give @s additem:ultrahard_steel 5
```

# TODO
- 名称を適切に変更
- 画像の解像度を適切に変更
- デバッグ方法が不明なので要調査


# 参考
以下を参考にしています
- https://www.youtube.com/watch?v=Q8fXI7xzc9E


# See Also
- https://docs.microsoft.com/en-us/minecraft/creator/documents/gettingstarted
