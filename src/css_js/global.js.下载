/*
  function fold_1(tb, btn) {
	var tr = tb.getElementsByTagName("tr");
	for (let j=1; j<tr.length; j++)
	  tr[j].style.display = btn.innerText.trim() == "+" ? "table-row" : "none";
    btn.innerText = btn.innerText == "+" ? "-" : "+";
  }
*/
/* This shall be excuted at first */
  /* Judge browser */
var browser = {
      versions: function () {
          var u = navigator.userAgent, app = navigator.appVersion;
          console.log(u);
          return {//移动终端浏览器版本信息
              trident: u.indexOf('Trident') > -1, //IE内核
              presto: u.indexOf('Presto') > -1, //opera内核
              webKit: u.indexOf('AppleWebKit') > -1, //苹果、谷歌内核
              gecko: u.indexOf('Gecko') > -1 && u.indexOf('KHTML') == -1, //火狐内核
              mobile: !!u.match(/AppleWebKit.*Mobile.*/),// || !!u.match(/AppleWebKit/), //是否为移动终端
              //ios: !!u.match(/\(i[^;]+;( U;)? CPU.+Mac OS X/), //ios终端
              android: u.indexOf('Android') > -1 || u.indexOf('Linux') > -1, //android终端或者uc浏览器
              iPhone: u.indexOf('iPhone') > -1 || u.indexOf('Mac') > -1, //是否为iPhone或者QQHD浏览器
              iPad: u.indexOf('iPad') > -1, //是否iPad
              webApp: u.indexOf('Safari') == -1,//是否web应该程序，没有头部与底部
              google: u.indexOf('Chrome') > -1,
              weixin:u.match(/MicroMessenger/i)=="MicroMessenger"
          };
      }(),
      language: (navigator.browserLanguage || navigator.language).toLowerCase()
  };
  
  //console.log("language"+browser.language);
  //console.log('是否为移动端'+ browser.versions.mobile);
if (browser.versions.mobile) {
  let cur_url = window.location.href;
  let page = cur_url.split('/').pop().split('\\').pop().split('.')[0];
  window.location.href = './m/index.html#' + (page=='index' ? 'home' : page);
}


window.onload = function() {
	  
  var oDiv = document.getElementById("aside"), H = 0, Y = oDiv, l = Y.offsetLeft+'px', w = Y.clientWidth+'px',
      oDiv2 = document.getElementById("aside2"), H2 = 0, Y2 = oDiv2, l2 = Y2.offsetLeft+'px', w2 = Y2.clientWidth+'px', 
      temp2 = oDiv.offsetHeight+10,  rl = temp2+'px',
      ftr  = document.getElementById("footer"), bh = document.body.offsetHeight - ftr.offsetHeight, pnl = document.getElementById("panel");
  if (ftr.offsetTop < bh) pnl.style.minHeight = pnl.offsetHeight + document.body.offsetHeight - ftr.offsetTop - ftr.offsetHeight - 60 + 'px';
      //if (ftr.offsetTop < bh) pnl.style.height = document.body.offsetHeight - ftr.offsetHeight - document.querySelector('header').offsetHeight - 20 + 'px';
  while (Y) {
    H += Y.offsetTop;
    Y = Y.offsetParent;
  }
  while (Y2) {
    H2 += Y2.offsetTop;
    Y2 = Y2.offsetParent;
  }
  H2 += H;
  window.onscroll = function() { 
    var s = document.documentElement.scrollTop || window.pageYOffset || document.body.scrollTop;
    if(s>H) {
      oDiv.style = "position:fixed;top:0;left:"+l+";width:"+w;
      oDiv2.style = "position:fixed;top:" + rl + ";left:"+l2+";width:"+w2;
    } else {
      oDiv.style = ""
      oDiv2.style = ""
    }
  }
/*  
  var guestsTb = document.getElementById("guests").getElementsByTagName("table");
  console.log(guestsTb.length);
  var folderBtn = document.getElementsByClassName("fold");
  console.log(folderBtn.length);
  
  for (let i=0; i<folderBtn.length; i++) {
	var tr = guestsTb[i].getElementsByTagName("tr");
	if (i>0) {
	  for (let j=1; j<tr.length; j++)
	    tr[j].style.display = "none";
	}
	folderBtn[i].onclick=function(){fold_1(guestsTb[i], folderBtn[i])};
  }
*/
}