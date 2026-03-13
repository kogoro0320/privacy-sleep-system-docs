## 動作環境

本ギミックは、以下の環境で開発・動作確認を行っています。

- Unity: 2022.3.22f1
- VRChat SDK - Base: 3.10.2
- VRChat SDK - Worlds: 3.10.2

## 1. unitypackageのインポート

[商品ページ](https://kogostore.booth.pm/items/8062290) より最新バージョンの商品ファイルをダウンロードし、中にある PrivacySleepSystem_ver[バージョン番号].unitypackage をプロジェクトにインポートしてください。

## 2. prefabの配置

以下のprefabファイルをSceneに配置してください。

- Assets/KogoStore/PrivacySleepSystem/Prefab/PrivacySleepSystem.prefab

## 3. 本体位置の調整

配置した <u>**PrivacySleepSystem**</u> を選択し、Inspector より Transform の <u>**Position Y が 0**</u> となっていることを確認してください。

0 になっていない場合は、0 に設定してください。

!!! warning "注意"
    床の高さ(Y)が 0 の位置を想定していますので、床の高さが 0 ではない場合、床の高さに合わせて設定してください。
    デフォルトでは、範囲( TransformObject )の下部が少し床にめり込むように設定しています。（位置ずれによる検出漏れ防止のため）

## 4. 範囲位置の調整

PrivacySleepSystem 内にある <u>**TransformObject**</u> の Transform を、お好みに合わせて調整してください。

!!! tip "推奨設定"
    TransformObject 内にある各オブジェクトの Transform や Box Collider の範囲は個別に調整せず、できるだけ TransformObject の Transform を調整するようにしてください。
    各機能ごとの指定範囲がずれてしまい、十分な機能提供ができなくなる可能性があります。

## 5. テレポート位置の調整

PrivacySleepSystem 内にある <u>**TeleportPoint**</u> のTransformを、お好みに合わせて調整してください。

!!! warning "注意"
    無限テレポートや連続侵入となる可能性がありますので、TransformObject から離れた位置にしてください。

## 6. UI位置の調整

PrivacySleepSystem > UI内にある <u>**InsideUI と OutsideUI**</u> のTransformを、お好みに合わせて調整してください。

!!! tip "推奨設定"
    InsideUI は TransformObject の範囲内への設置を推奨します。OutsideUI は TransformObject の範囲外に設置してください。