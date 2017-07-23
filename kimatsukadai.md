# 課題3レポート    17EC039 小林崇寛

ひよこの画像を原画として使用する.この画像は縦1066画素,横1600画素のディジタルカラー画像である.

ORG=imread('chick.png'); % 原画像の入力   
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換    
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

により,原画の読み込み,白黒濃淡画像への変換,及び表示した結果を図1に示す.

![白黒ひよこ](http://uploader.sakura.ne.jp/src/up162883.png?raw=true)  

 図1　白黒濃淡色の原画像

白黒にした画像の輝度値が64に満たない画素を0（黒）,64以上の値を持つ画素を1（白）とするように処理する.このような処理において基準となる値を閾値,元の画像を白と黒だけの画像にする処理を2値化という.

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

![64ひよこ](http://uploader.sakura.ne.jp/src/up162884.png?raw=true)  

図2　輝度値64での2値化画像

同様に,輝度値96,128,192にして処理を行う.

IMG = ORG > 96;
imagesc(IMG); colormap(gray); colorbar;

IMG = ORG > 128;
imagesc(IMG); colormap(gray); colorbar;

IMG = ORG > 192;
imagesc(IMG); colormap(gray); colorbar;

これらの処理によって出た結果を図3~5に示す.

![96ひよこ](http://uploader.sakura.ne.jp/src/up162885.png?raw=true)

図3　輝度値96での2値化画像

![128ひよこ](http://uploader.sakura.ne.jp/src/up162886.png?raw=true)

図4　輝度値128での2値化画像

![192ひよこ](http://uploader.sakura.ne.jp/src/up162887.png?raw=true)

図5　輝度値192での2値化画像

輝度値を増加させることにより,元の白黒画像に近づけることができる.



