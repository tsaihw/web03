
#160403
在safari看會是滿版，在ipad看會歪掉
#160404
改字型 不能用ttc檔 記得回到css上層
@font-face {
  font-family: 'jasmine';
  src: url('../fonts/font.ttf');
}
#160404
用fontforge改字型成功啦
#160404
one page scroll好像不錯
http://www.thepetedesign.com/demos/onepage_scroll_demo.html
http://alvarotrigo.com/fullPage/
http://www.cssdesignawards.com/articles/15-excellent-jquery-plugins-to-spice-up-your-sites/44/
#160406
可以捲回最上方的按鈕jquery.backTop.min.js及backTop.css
#160422
放圖片 用透明背景好
把<link href="css/bootstrap.min.css" rel="stylesheet">換成<link href="css/bootstrap.css" rel="stylesheet">因為圖片無法對齊下面的問題要從bootstrap.css改，以後再重新編譯

加了pull-down js讓圖片可對齊下方==>用手機根本悲劇
<script type="text/javascript">
//for each element that is classed as 'pull-down', set its margin-top to the difference between its own height and the height of its parent
$('.pull-down').each(function() {
  var $this=$(this);
  $this.css('margin-top', $this.parent().height()-$this.height())
});</script>
</body>

#160422-2
新增
img-responsive
img-responsive-tall
img-responsive-short
讓圖片在大螢幕置底(增加上方padding)
用@media (max-width: 978px) {
    .img-responsive{
      padding:0;
      margin:0;
    }
    .img-responsive-tall {
      padding:0;
      margin:0;
    }
    .img-responsive-short {
      padding:0;
      margin:0;
    }
}讓小裝置不會有padding

#160428
新footer
<p class="copyright">版權所有 暖暖心理治療所 © 2016<span style="float:right;">網頁製作 <a href="http://www.wordpress.org/">Guppy Squad</a></span></p>
新增兩張圖片
拿掉<hr class="section-heading-spacer">比較好調整padding
調整padding
治療所介紹那邊調
<div class="col-lg-6 col-sm-6">
<div class="col-lg-5 col-lg-offset-1 col-sm-6">讓圖大一點

#160430
新增公告用alert
<div class="col-lg-12 col-sm-6">
<div class="alert alert-warning fade in">
  <a href="#" class="close" data-dismiss="alert" aria-label="close">&times;</a>
  <strong>公告：</strong> 暖暖心理治療所春節期間暫停營業。
</div>
</div>
詳細資訊可以考慮用modal或Popovers
http://www.w3schools.com/bootstrap/bootstrap_modal.asp
http://www.w3schools.com/bootstrap/bootstrap_popover.asp

/*限制寬度*/
.container{
  max-width:1080px
}

blockquote {
  padding: 0px 0px 0px 30px;
  margin: 20px 0px 20px 0px;
  border-left: 3px solid #eee; }
}

整理&刪除一些多餘css

讓list格式好一點
ul.A{
  letter-spacing: 0.3px;
  margin:10px 0px 0px 0px;
  line-height: 1.5;
  list-style-type: none;
}
ul.B{
  letter-spacing: 0.3px;
  margin:10px 0 0 5px;
  line-height: 1.6;
  list-style-type: disc;
}
自動更新年份
<script type="text/javascript">
document.write(new Date().getFullYear());
</script>
