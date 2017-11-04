# このソフトウェアについて

和音(和声音)パターンを29用意した。

# 対象ファイル名

ファイル名|説明
----------|----
MusicTheory/temperament/chords/ChordIntervals.py|各スケールの構成音を生成して音声ファイルを出力する

# 実行

```sh
 $ python ChordIntervals.py 
========== 和声音 ==========
----- 2和音 -----
(0, 7)
(0, 12)
----- 3和音 -----
(0, 4, 7)
(0, 3, 7)
(0, 4, 8)
(0, 3, 6)
----- 4和音 -----
(0, 4, 7, 10)
(0, 3, 7, 10)
(0, 4, 7, 11)
(0, 4, 8, 11)
(0, 3, 6, 10)
(0, 3, 7, 11)
(0, 4, 7, 9)
(0, 3, 7, 9)
----- 5和音 -----
(0, 4, 7, 10, 14)
(0, 4, 7, 10, 13)
----- その他の和音 -----
(0, 4, 7, 10, 14)
(0, 5, 7)
(0, 5, 7, 10)
(0, 4, 7, 10, 18)
(0, 4, 7, 11, 18)
(0, 4, 10, 21)
(0, 4, 10, 20)
(0, 4, 7, 14)
(0, 4, 5, 7)
(0, 4, 6)
(0, 4, 6, 10)
========== 非和声音（未実装） ==========
========== 名前一覧 ==========
29 ['Add4', 'Add9', 'Augmented', 'AugmentedSeventh', 'Dim5', 'Diminished', 'DiminishedSeventh', 'HalfDiminishedSeventh', 'Major', 'MajorNinth', 'MajorSeventh', 'MajorSeventhSharp11', 'MajorSix', 'Minor', 'MinorMajorSeventh', 'MinorSeventh', 'MinorSix', 'Ninth', 'Octave', 'Power', 'Seventh', 'Seventh13', 'SeventhAdd9', 'SeventhDim5', 'SeventhFlat13', 'SeventhSharp11', 'SeventhSus4', 'Sus2', 'Sus4']
```

`/res`ディレクトリ配下に音声ファイルが出力される。

# 課題

* 和音パターンを調査し網羅したい
    * 和声音でも未実装パターンがある
    * 非和声音は勉強不足。難しそう……
* 12平均律以外の音律でも構成音を算出したいが……
    * 純正律における中間の5音も算出したい。計算方法がよくわからない
* 純正律で綺麗な和音になる主要三和音とそれ以外の音痴な副和音を聴き比べてみたい
* ソースコードが整理できていない
    * 音楽理論がわからず、どうまとめていいのかもわからない

# 開発環境

* Linux Mint 17.3 MATE 32bit
* [libav](http://ytyaru.hatenablog.com/entry/2018/08/24/000000)
    * [各コーデック](http://ytyaru.hatenablog.com/entry/2018/08/23/000000)
* [pyenv](https://github.com/pylangstudy/201705/blob/master/27/Python%E5%AD%A6%E7%BF%92%E7%92%B0%E5%A2%83%E3%82%92%E7%94%A8%E6%84%8F%E3%81%99%E3%82%8B.md) 1.0.10
    * Python 3.6.1
        * [pydub](http://ytyaru.hatenablog.com/entry/2018/08/25/000000)
        * [PyAudio](http://ytyaru.hatenablog.com/entry/2018/07/27/000000) 0.2.11
            * [ALSA lib pcm_dmix.c:1022:(snd_pcm_dmix_open) unable to open slave](http://ytyaru.hatenablog.com/entry/2018/07/29/000000)
        * [matplotlib](http://ytyaru.hatenablog.com/entry/2018/07/22/000000)
            * [matplotlibでのグラフ表示を諦めた](http://ytyaru.hatenablog.com/entry/2018/08/05/000000)

# 参考

感謝。

## 和音

* https://ja.wikipedia.org/wiki/%E5%92%8C%E9%9F%B3
* http://www.piano-c.com/

## 音程

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E7%A8%8B
* https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q1365320628
* https://okwave.jp/qa/q6858420.html

## 440Hz, 432Hz

* http://tabi-labo.com/156689/music-a432

## 和音の生成

* http://ism1000ch.hatenablog.com/entry/2013/11/15/182442
* https://ja.wikipedia.org/wiki/%E4%B8%89%E5%92%8C%E9%9F%B3
* https://ja.wikipedia.org/wiki/%E3%83%91%E3%83%AF%E3%83%BC%E3%82%B3%E3%83%BC%E3%83%89

## 音名

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E5%90%8D%E3%83%BB%E9%9A%8E%E5%90%8D%E8%A1%A8%E8%A8%98

## 音階

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E9%9A%8E

### 五度圏

* http://dn-voice.info/music-theory/godoken/

## 音高の算出

* http://www.asahi-net.or.jp/~HB9T-KTD/music/Japan/Research/DTM/freq_map.html
* http://www.nihongo.com/aaa/chigaku/suugaku/pythagoras.htm

## サイン波のスピーカ再生

* http://www.non-fiction.jp/2015/08/17/sin_wave/
* http://aidiary.hatenablog.com/entry/20110607/1307449007
* http://ism1000ch.hatenablog.com/entry/2013/11/15/182442

# ライセンス

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

Library|License|Copyright
-------|-------|---------
[pydub](https://github.com/jiaaro/pydub)|[MIT](https://github.com/jiaaro/pydub/blob/master/LICENSE)|[Copyright (c) 2011 James Robert, http://jiaaro.com](https://github.com/jiaaro/pydub/blob/master/LICENSE)
[pygame](http://www.pygame.org/)|[LGPL](https://www.pygame.org/docs/)|[pygame](http://www.pygame.org/)

