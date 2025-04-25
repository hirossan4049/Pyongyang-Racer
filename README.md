
# PYracer Archive

> Pyongyang Racer（平壌レーサー）をスタンドアロンでプレイするための非公式アーカイブです。  
> 本プロジェクトはオリジナル作者とは一切関係ありません。

https://ja.wikipedia.org/wiki/%E5%B9%B3%E5%A3%8C%E3%83%AC%E3%83%BC%E3%82%B5%E3%83%BC

---

## 📥 ダウンロード

| OS | バイナリ |
| --- | --- |
| Windows(PYracer.exe) | 👉 [最新ビルドをダウンロード](https://github.com/hirossan4049/Pyongyang-Racer/releases/download/1.0.0/PYracerWindows.zip) |
| macOS | 👉 [最新ビルドをダウンロード](https://github.com/hirossan4049/Pyongyang-Racer/releases/download/1.0.0/PYracerMacOS.zip) |

---

## 🛠️ ビルド方法

### 1. 証明書の作成

```bash
adt -certificate -cn DevCert 2048-RSA myCert.p12 pass1234
```

### 2. macOS アプリのビルド

```bash
adt -package \
  -storetype pkcs12 -keystore myCert.p12 -storepass pass1234 \
  -target bundle -arch x64 \
  PYracerBundle \
  PYracer-app.xml Preloader.swf PYracer.swf \
  1.dat common.dat common.txt info.txt PreGame.mp3 sound.dat symbol.dat \
  -C . icons
```

### 3. Windows アプリのビルド

```bash
adt -package \
  -storetype pkcs12 -keystore myCert.p12 -storepass pass1234 \
  -target exe -arch x64 \
  PYracer.exe \
  PYracer-app.xml Preloader.swf PYracer.swf \
  1.dat common.dat common.txt info.txt PreGame.mp3 sound.dat symbol.dat \
  -C . icons
```

---

## 📄 ライセンス

本ソフトウェアは **WTFPL**（Do What The F\*ck You Want To Public License）で提供されています。  
ただし、以下の事項をご確認ください。

- 日本国内での利用・配布は、日本の著作権法その他関連法規を遵守してください。  
- 画像・音声・テキストなど各種アセットの権利関係は利用者自身の責任で確認してください。  
- 北朝鮮由来のコンテンツを扱う場合、国際的制裁や各国法規に抵触するおそれがあります。

---

## ⚖️ 法的注意

日本国は朝鮮民主主義人民共和国（北朝鮮）を国家承認していません。  

- **最高裁平成23年（2011年）12月8日判決**  
  「日本は国家承認していない北朝鮮の著作物を著作権法上保護する義務を負わない」と判断（フジテレビ／日本テレビ勝訴）。  
  → 北朝鮮由来の映像・音楽・画像・テキスト等は、日本国内では著作権保護の対象外（事実上パブリックドメイン）。
<br/>

- 参考記事: [朝日新聞](https://www.asahi.com/special/08001/TKY201112080593.html)  
- 判例紹介: [newpon 判例紹介](https://www.newpon.com/tm/hanketsu/supreme/s111208_NorthKorea.html)  
- 特許庁ニュース: [2009-03 ニュース](https://www.hanketsu.jiii.or.jp/hanketsu/jsp/hatumeisi/news/200903news.html)
