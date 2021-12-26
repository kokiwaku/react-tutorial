# React.js のチュートリアルをやってみた
https://ja.reactjs.org/tutorial/tutorial.html


## ローカルで動作させるまでの手順

1. Dockerコンテナ立ち上げる
```
$ docker-compose up -d
```

2. Dockerコンテナに入る

```
// コンテナIDを取得
$ docker ps

// コンテナに入る
$ docker exec -it コンテナID sh
```

3. npm start 実行  
```
// コンテナ内で以下コマンド
# cd /app/my-app
# npm start

// コンパイルに成功すると、以下のようなコマンドが出力される。
Compiled successfully!

You can now view my-app in the browser.

  Local:            http://localhost:3000
  On Your Network:  http://172.21.0.2:3000

Note that the development build is not optimized.
To create a production build, use npm run build.

asset static/js/bundle.js 1.49 MiB [emitted] (name: main) 1 related asset
asset index.html 1.67 KiB [emitted]
asset asset-manifest.json 190 bytes [emitted]
cached modules 1.38 MiB [cached] 104 modules
runtime modules 28.3 KiB 14 modules
./src/index.js 6.06 KiB [built]
webpack 5.65.0 compiled successfully in 17228 ms
```

4. ブラウザからhttp://localhost:3000にアクセス
