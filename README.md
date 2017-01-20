# VisualCryptography
<h1><img class="alignnone  wp-image-99" src="https://catmaoblog.files.wordpress.com/2016/10/6lqz4de.png" alt="Icon made by Freepik from www.flaticon.com" width="40" height="40" /> <a href="https://catmao1230.github.io/VisualCryptography/" target="_blank">點我前往</a></h1>
<h1><img class="alignnone  wp-image-99" src="https://catmaoblog.files.wordpress.com/2016/10/6lqz4de.png" alt="Icon made by Freepik from www.flaticon.com" width="40" height="40" /> <a href="https://catmaoblog.wordpress.com/2016/10/09/visualcryptography/" target="_blank">WordPress</a></h1>
<h1><img class="alignnone  wp-image-41" src="https://catmaoblog.files.wordpress.com/2016/10/3h9rzur.png" alt="3h9rzur" width="40" height="40" /> 視覺密碼介紹</h1>
將一張影像分解成為好幾份，每一份在外觀上看起來都是亂碼，要將全部重疊在一起，才能看到原本的影像。

視覺密碼有很多種，有黑白也有彩色，我這次寫的只有單純的黑白。

如下所示：

原本的圖片為 <img class="alignnone size-full wp-image-26" src="https://catmaoblog.files.wordpress.com/2016/10/lqdtuwc.png" alt="lqdtuwc" width="21" height="20" />

canvas1 <img class="alignnone size-full wp-image-29" src="https://catmaoblog.files.wordpress.com/2016/10/ioyrfky.png" alt="ioyrfky" width="42" height="40" /> + canvas2 <img class="alignnone size-full wp-image-31" src="https://catmaoblog.files.wordpress.com/2016/10/zrlj75j.png" alt="zrlj75j" width="42" height="40" /> = canvas3 <img class="alignnone size-full wp-image-33" src="https://catmaoblog.files.wordpress.com/2016/10/ojsql35.png" alt="ojsql35" width="42" height="40" />

如果將成果影印成投影片，兩張疊再一起就會出現圖案。

<img class="alignnone size-full wp-image-84" src="https://catmaoblog.files.wordpress.com/2016/10/rihlagu.png" alt="rihlagu" width="665" height="225" />

更多詳細介紹、原理請參考最下方資料來源。
<h1><img class="alignnone  wp-image-43" src="https://catmaoblog.files.wordpress.com/2016/10/ril6i6c.png" alt="ril6i6c" width="40" height="40" /> 程式碼</h1>
<ol>
	<li>將圖像畫在 canvas 上</li>
	<li>新產生的兩張圖片會為原本圖像大小的兩倍</li>
	<li>用 getImageData 讀取 canvas 上的像素資料</li>
	<li>將像素拆成兩張圖片，若為黑色則兩張圖片互補（例如：0 + 5、1 + 4），若為白色則兩張圖片相同</li>
	<li>2 * 2 的視覺密碼總共有六種圖形，每一點隨機取一種畫在 canvas1 和 canvas2 上
<img class="alignnone size-full wp-image-52" src="https://catmaoblog.files.wordpress.com/2016/10/cobrbkw.png" alt="cobrbkw" width="592" height="128" /></li>
	<li>畫在 canvas1 和 canvas2 的點都要畫在 canvas3（結果圖）上</li>
	<li>我畫點的方式為在座標上根據四個方框的起始座標畫上 1px 的正方形
<img class="alignnone size-full wp-image-53" src="https://catmaoblog.files.wordpress.com/2016/10/mywwwmn.png" alt="mywwwmn" width="184" height="170" /></li>
</ol>
 
<h1><img class="alignnone  wp-image-42" src="https://catmaoblog.files.wordpress.com/2016/10/tpodion.png" alt="tpodion" width="40" height="40" /> 參考資料</h1>
<ul>
	<li><a href="ftp://ftp.im.tku.edu.tw/Prof_Hou/%BCv%B9%B3%B3B%B2z%BBP%B8%EA%B0T%C1%F4%C2%C3/%B1m%A6%E2%B5%F8%C4%B1%B1K%BDX.ppt">[ PPT ] 彩色影像視覺密碼之製作 Visual Cryptography for Color Images / 淡江大學資訊管理系所侯永昌</a></li>
	<li><a href="http://libwri.nhu.edu.tw:8081/Ejournal/AV03010204.pdf" target="_blank">[ PDF ] 像素無擴展的彩色連續調影像視覺密碼研究 / 朱正民 邱創標 黃賦宇</a></li>
</ul>
