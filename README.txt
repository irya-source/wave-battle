ウェーブバトル（スマホアプリ版・PWA）

■ 使い方（いちばん簡単）
1. このフォルダの中身を、HTTPSで公開できる場所に置きます
   （例: Netlify Drop / GitHub Pages / Cloudflare Pages など。ファイルをドラッグして公開するだけ）
2. 公開されたURLをスマホで開きます
3. iPhone: Safariの共有 →「ホーム画面に追加」／ Android(Chrome): メニュー →「アプリをインストール」
→ ホーム画面のアイコンから全画面のアプリとして起動し、オフラインでも遊べます。
※ セーブデータは端末のブラウザ内（localStorage）に保存されます。

■ ストア配布用のアプリ（APK / IPA）にしたい場合
Node.js が入ったPCで、Capacitor を使って包みます。
  npm init -y
  npm i @capacitor/core @capacitor/cli @capacitor/android @capacitor/ios
  npx cap init ウェーブバトル com.example.wavebattle --web-dir=www
  mkdir www && cp index.html manifest.json sw.js icon-*.png www/
  npx cap add android   （iOSは npx cap add ios）
  npx cap open android  （Android Studio / Xcode でビルド）
画面向きは縦固定にしてください。ストア公開にはデベロッパー登録が必要です。
