# Project setup :
## 1 node.jsのインストール
下記URLのインストーラーからインストールする。(LTS版)

https://nodejs.org/en/

## 2 yarnのインストール
下記コマンドを実行。

`npm install -g yarn`

## 3 Watchmanのインストール
下記コマンドを実行。

`brew update`

`brew install watchman`

## 4 expoのアカウント作成
下記URLでアカウントを作成する

https://expo.dev/signup

別途配布するURLのQRコードを読み込めば実機で確認できる。

`expo publish` でQR発行。

ただ、iosはプロジェクト作成アカウントでログインしていないと表示できない。

androidは確認可能。

プロジェクト用のアカウントを用意するか、プロジェクト作成者のアカウントでログインすることで全員が確認できる。（要相談）

個人から組織用のアカウントに切り替えも可能。


## 5 Xcodeのインストール
AppStoreでXcodeと検索し、入手をクリック。

XcodeをインストールしたらCommand Line Toolsを設定する。

Xcodeを実行して上部のメニューでXcode > setting > Locationsを押して、

Command Line Toolsが設定されているか確認します。（空で無いことを確認）

空だった場合は下記コマンドを実行し、xcodeを再起動。

`xcode-select --install`

Open Developer Tool > Simulatorでシュミレータが立ち上がればOK。

## 6 Android Studioのインストール
下記URLからインストールする。

https://developer.android.com/studio

起動して、Customize > Configureをクリック。

設定画面が開いたら、 Appearance & Behavior > System Settings > Android SDKをクリック。

右側の画面のSDK Toolsをクリックし、33.0.0を選択し、インストールする。

右側に表示されているAndroid SDK Locationのパスをコピーする。

ターミナルで

`vim ~/.bash_profile `

または、 

`vim ~/.zshrc`

で環境変数を設定する

vimがやりづらい場合で、VScodeが入っている方は、ターミナルでルートディレクトリに移動し、code .　を叩くとVScodeで開ける。

下記を設定する。

`export ANDROID_SDK_ROOT=/Users/ユーザネーム/Library/Android/sdk`

`export PATH=$ANDROID_SDK_ROOT/platform-tools:$PATH`

`export PATH=$ANDROID_SDK_ROOT/emulator:$PATH`

Android Studioに戻り、More Actions > Virtual Device Managerをクリック。

新しいWindowが開けたら、Create deviceをクリック。

デバイスはなんでもいいがPixelが安定しているらしい。

デバイスを選択後、OSを選択する。（指定無し）

設定を終え、emulatorが起動したら完了。

## 7 プロジェクト起動

プロジェクトディレクトリまで移動し、下記コマンドを実行。

`npx expo start`

サーバーが立ち上がったら、

`i`を実行するとSimulatorが起動される。

`a`が実行するとemulatorが起動される

