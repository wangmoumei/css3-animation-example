# css3-animation-example
<p>an example for animation in css3</p>
<p>练习css3 animation用</p>
<pre>
#wine-height{
	-webkit-animation: 3s water linear infinite;
	-moz-animation: 3s water linear infinite;
	animation: 3s water linear infinite;
}
@-webkit-keyframes water {
  0% { background-position:0 0; }
  100% { background-position:200px 0; }
}
@-moz-keyframes water {
  0% { background-position:0 0; }
  100% { background-position:200px 0; }
}
@keyframes water{
  0% { background-position:0 0; }
  100% { background-position:200px 0; }
}
</pre>
<p>用起来比js动画舒服，支持了很多属性。</p>
<p>下面js动画</p>
<pre>
fx = function (f,t,fn,end,tm,pow){
		var D=Date;
		var d=new D;
		var e;
		var c=tm||240;
		var pow=pow||2;
		return e=setInterval(function (){
			var z=Math.min(1,(new D-d)/c);
			(false===fn(+f+(t-f)*Math.pow(z,pow),z)||z==1) && end && end(clearTimeout(e));
		},10);
	}

</pre>
