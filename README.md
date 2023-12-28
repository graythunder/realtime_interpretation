# realtime_interpretation
openaiのwhisperとchatgptを使ってリアルタイム音声翻訳を行うアプリケーションを作ってみました。(UIなど諸々雑ですがご了承ください)
英語->日本語の翻訳のみ対応していますが設定をいじれば他の言語でも動くと思います。

## 処理概要
1. ブラウザ上で音声を検知したら録音
2. openaiの音声認識API(whisper)に投げて文字起こし
3. 返ってきたテキストをchatGPTのAPIに投げて日本語に翻訳

## 実行手順
1. サーバーを起動
```
python3 whisper_server.py
```
2. ブラウザでlocalhost:9999(デフォルト)を開く
3. スピーカー等から音声を流すと音声認識結果(左)と翻訳結果(右)が表示される
- 注意: このアプリケーションと同じブラウザで音声を再生するとうまく音を拾えない場合があるので,別のブラウザで再生すると良さそう
<img width="1336" alt="スクリーンショット 2023-12-28 13 39 42" src="https://github.com/graythunder/realtime_interpretation/assets/28726854/031d0424-6897-4e00-9638-87267e2db9b3">
