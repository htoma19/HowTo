# AndroidSturdio開発環境構築
- 以下の手順を順番に実行
## ステップ 1：古いプロジェクトファイルの完全削除
- ターミナルをすべて閉じます。
- エクスプローラー（ファイルマネージャー）で、現在のプロジェクトフォルダ（C:\Users\touma\MyKakeiboApp）へ移動します。
- このフォルダ全体を完全に削除してください。

## ステップ 2：新規プロジェクトの作成
- プロジェクトをクリーンな状態から再生成します。
- 削除したフォルダが存在していた親ディレクトリに移動します。
- ターミナルを開き、以下のコマンドを実行して、新しいプロジェクトを作成します。
-- npx react-native init MyKakeiboApp

## ステップ 3：依存関係のインストール
- 新しい MyKakeiboApp フォルダに入り、必要なライブラリを一度にインストールします。
- プロジェクトフォルダに移動
-- cd MyKakeiboApp
--- 必要なすべてのライブラリをインストール このコマンドには、ナビゲーション、UI、アイコン、カレンダー、永続化に必要なものがすべて含まれています。
-- npm install @react-navigation/native @react-navigation/bottom-tabs react-native-paper react-native-vector-icons @react-native-community/datetimepicker @react-native-async-storage/async-storage react-native-gesture-handler
--- TypeScriptの型定義ファイルをインストール
-- npm install --save-dev @types/react-native-vector-icons

## ステップ 4：アプリの再実行
- Androidのビルドクリーンアップ
-- cd android
-- ./gradlew clean
-- cd ..
-アプリの実行
-- npx react-native run-android
