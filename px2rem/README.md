npm install px2rem-loader //^0.1.9

build => utils.js => cssLoaders => const px2remLoader = {loader: 'px2rem-loader', options: {remUnit: 75 //默认75，即1rem=75px，是按设计图的比例设置1个rem的大小 remunit = device-width/html-font-size}}

build => utils.js => generateLoaders => [cssLoader, px2remLoader] : [cssLoader, px2remLoader]

option： remUnit => 一个rem单位的大小（默认75px） remPrecision => 精确小数位（默认8）

如果不想被转化，如font-size，可以把px改成大写（修改UI框架样式），也可以在px后面加/* no */

html =>

      (function(){
        var html = document.documentElement;
        var width = html.getBoundingClientRect().width;

        html.style.fontSize = width/10 + 'px';
      })();

