# liuchangyou
计181 2018310732 刘长有
实验目的 掌握字符串String及其方法的使用  掌握异常处理结构
业务要求  利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能函数，并运行。
达到如下功能：
      每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
      允许提供输入参数，统计古诗中某个字或词出现的次数
      考虑操作中可能出现的异常，在程序中设计异常处理程序

输入：汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝承欢侍宴无闲暇春从春游夜专夜后宫佳丽三千人三千宠爱在一身金屋妆成娇侍夜玉楼宴罢醉和春姊妹弟兄皆列士可怜光采生门户遂令天下父母心不重生男重生女骊宫高处入青云仙乐风飘处处闻缓歌慢舞凝丝竹尽日君王看不足渔阳鼙鼓动地来惊破霓裳羽衣曲九重城阙烟尘生千乘万骑西南行
输出：
汉皇重色思倾国，御宇多年求不得。
杨家有女初长成，养在深闺人未识。
天生丽质难自弃，一朝选在君王侧。
回眸一笑百媚生，六宫粉黛无颜色。
春寒赐浴华清池，温泉水滑洗凝脂。
侍儿扶起娇无力，始是新承恩泽时。
云鬓花颜金步摇，芙蓉帐暖度春宵。
春宵苦短日高起，从此君王不早朝。
…………

实验步骤：先利用代码写成可以调用后台文字的代码，然后将长恨歌储存到后台
String s1="";
之后利用分行系统分行。
for(int i=0;i<s1.length()/16;i++)
System.out.print(s1.substring(0+16*i,16+16*i)+"\n"); 
每七个字加一个逗号，因为七是奇数，所以利用if语句除七奇数加逗号偶数加句号
for(int i=0;i<x.length()/7;i++)
	      if(i%2==0)
	       s1=s1+x.substring(0+7*i,7+7*i)+",";
	      else
	       s1=s1+x.substring(0+7*i,7+7*i)+"。";
从后台中查询某字，代码会联系后台查询事先写好的文字也就是长恨歌，之后逐字查找某字
String y=args[0];
	    	String z=args[1];
			separateword(y);		
	int chaxun = 0;		
		String s2="";		
		int index;		
		while(y.contains(z))
		{			
			chaxun++;
		    index = y.indexOf(z);
		    s2 = y.substring(index + z.length());		
		    y= s2;			
流程图：![imag](https://github.com/LIUCHANGYOU6/liuchangyou/blob/master/%E6%B5%81%E7%A8%8B%E5%9B%BE.jpg)

运行截图：![imag](https://github.com/LIUCHANGYOU6/liuchangyou/blob/master/%E5%88%98%E9%95%BF%E6%9C%89.png)

实验心得：通过这次实验我熟练掌握了字符串的添加和查找某个字符出现的次数，
学会了length语句和substring语句，也遇到了一些困难，通过问同学和上网解决之后，更加熟悉了for循环。
我的长恨歌一开始写在代码里，之后改到后台，知道了可以灵活写java代码。
