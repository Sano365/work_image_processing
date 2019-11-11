# kadai2 階調数と疑似輪郭
- ２階調，４階調，８階調の画像を生成せよ。
- 原画像を図1に示す。
  
<div align="center">
<img src="img/f_fox.png" width="300"><br>
図1,原画像
</div>

 - 画像の読み込みは以下のコードを実行した。
```m
ORG=imread('f_fox.png'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
```
 - 2行目より、RGB画像をグレースケールに変換している。
 - 変換は8bitの数値配列に変換している。

## 2階調画像
- 以下のコードを実行した。
```m
IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;
```
 - 1行目より、グレースケールの1画素の数値が128より大きい部分が白となる。
 - 結果は図2のようになった。

