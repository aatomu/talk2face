# talk2face

マイクの入力によって表情を変えるソフト

## 動作環境
nw.js : `v0.80.1`
chrome: `118.0.5993.70`
### How To Use(chrome Browser Like)
1. `config.json.js`を編集する
2. `index.html`を開く
3. 入力デバイスを指定する  
    *直接開いた場合は既定のマイクのみ
    *httpsなど暗号化されいる場合はほかのマイクも可能
4. (確認されたら)マイクを許可する
5. それだけ!

### How To Use(nw.js GUI like)
1. `config.json.js`を編集する
2. `nw .`でnw.jsで起動する
3. 入力デバイスを指定する
4. それだけ!

## config.json.js

- blink  
  主に瞬きについてのコンフィグ
  - cool_down_min/cool_down_min  
    瞬きの最小/最大 間隔[ms]
  - animation_time  
    瞬きの画像が変わるまでの時間[ms]
- mouth  
  主に瞬きについてのコンフィグ
  - attack  
    マイクの入力上限に対する口を開ける閾値[%]
  - animation_time  
    口の画像が変わるまでの時間[ms]
- voice_check  
  音量の確認をする間隔[ms]
- face  
  画像一覧 最大 10 こまで
  - normal  
    通常時の顔
  - mouth_half_open
    口が半開きの顔
  - mouth_full_open
    口が全開きの顔
  - eye_half_open
    目が半開きの顔
  - eye_full_open
    目が全閉じの顔

## キーコンフィグ

| キー        | 機能               |
| ----------- | ------------------ |
| Shift + ESC | ソフトを閉じる     |
| Shift + E   | 目を閉じっぱで固定 |
| Shift + M   | 口を開けっぱで固定 |
| 0-9         | 画像を変更         |
