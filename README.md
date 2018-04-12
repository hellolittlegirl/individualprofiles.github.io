<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>个人简历</title>
	<link rel="stylesheet" type="text/css" href="bootstrap.min.css">
	<script type="text/javascript" src="skills.js"></script>
	<style type="text/css">
		*{
			padding: 0;
			margin: 0;list-style: none;font-size: 16px;
		}
		body{
			font-family: Arial,"Microsoft YaHei",sans-serif;
			
		}
		html,body{
			height: 100%;
			overflow: hidden;
			min-width: 1000px;
			min-height: 650px;
		}
		nav{position: fixed;top:0;left: 0;z-index: 1000;line-height: 40px;width:100%;background-color: #d2d4d5;opacity: 0.5;overflow: hidden;}
		nav ul li{margin-right: 2%;}
		nav ul li a{text-decoration: none;color: #333;}
		#container,.sections,.section{

			height: 100%;
			position: relative;
		}
		#section0,
		#section1,
		#section2,
		#section3,
		#section4{
			background-color: #000;
			background-size: cover;
			background-position: 50% 50%;
		}
		#section0{
			background-image: url(images/1.jpg);
			color: #CCFF99;
			text-shadow:1px 1px 1px #333;
		}
		#section1{
			color: #fff;
			text-shadow:1px 1px 1px #333;
			background-image: url(images/2.jpg);
		}
		#section2{
			background-image: url(images/3.jpg);
			color: #fff;
			text-shadow:1px 1px 1px #666;
		}
		#section3{
			color: #008283;
			background-image: url(images/4.jpg);
			text-shadow:1px 1px 1px #fff;
		}
		#section4{
			color: #008283;
			background-image: url(images/2.jpg);
			text-shadow:1px 1px 1px #fff;
		}
		#section2{
			color: #666;
		}
		.left{
			float: left;
		}
		.right{
			float: right;
		}
		h1{
			font-size: 4em;
			font-weight: normal;
		}
		#section2 span{color: #f00;}
		.intro{
			position: absolute;
			top: 50%;
			width: 100%;
			-webkit-transform: translateY(-50%);
			transform: translateY(-50%);
			text-align: center;
		}
		.pages{
			position:fixed;
			list-style: none;
		}
		.vertical.pages{
			right: 10px;
			top: 50%;
		}
		.horizontal.pages{
			left: 50%;
			bottom: 10px;
		}
		.pages li{
			width: 8px;
			height: 8px;
			border-radius: 50%;
			background: #fff;
			margin: 10px 5px;
			cursor: pointer;
		}
		.horizontal.pages li{
			display: inline-block;
			vertical-align: middle;
		}
		.pages li.active{
			width: 14px;
			height: 14px;
			border: 2px solid #FFFE00;
			background: none;
			margin-left: 0;
		}
		#section0 .title{
			-webkit-transform: translateX(-100%);
			transform: translateX(-100%);
			-webkit-animation: sectitle0 1s ease-in-out 100ms forwards;
			animation: sectitle0 1s ease-in-out 100ms forwards;
		}
		#section0 .container div{
			-webkit-transform: translateX(100%);
			transform: translateX(100%);
			-webkit-animation: sec0 1s ease-in-out 100ms forwards;
			animation: sec0 1s ease-in-out 100ms forwards;
		}
		@-webkit-keyframes sectitle0{
			0%{
				-webkit-transform: translateX(-100%);
				transform: translateX(-100%);
			}
			100%{
				-webkit-transform: translateX(0);
				transform: translateX(0);
			}
		}
		@keyframes sectitle0{
			0%{
				-webkit-transform: translateX(-100%);
				transform: translateX(-100%);
			}
			100%{
				-webkit-transform: translateX(0);
				transform: translateX(0);
			}
		}
		@-webkit-keyframes sec0{
			0%{
				-webkit-transform: translateX(100%);
				transform: translateX(100%);
			}
			100%{
				-webkit-transform: translateX(0);
				transform: translateX(0);
			}
		}
		@keyframes sec0{
			0%{
				-webkit-transform: translateX(100%);
				transform: translateX(100%);
			}
			100%{
				-webkit-transform: translateX(0);
				transform: translateX(0);
			}
		}
		.con-nav{position:absolute;bottom:0;left:50%;margin-left:-10%; width:20%;height: 14px;line-height: 20px;}
		.about div{border: 2px dashed #CCC;height: 160px;width: 160px;border-radius: 50%;margin:10% 2%;position: relative;}
		#adout-my{color: #0099CC;font-size: 2rem;}
		.about div:hover{width: 200px;height: 200px; border: 4px dashed #CCFF99;}
		.about div:hover span{width:200%;font-size: 3rem;margin-left: -50%;color: #999;}
		.about div:hover img{width: 200px;height: 200px;}
		.about div span{position: absolute;top:40%;width: 100%;left: 0%;text-align: center;}
		.about div img{width: 160px;height: 160px;position: absolute;left: 0;border-radius: 50%;}
		.skills{width: 70%;overflow: hidden;margin:5% 15%;text-align: center;border: 1px solid #000;border-radius: 10px;transition:all 0.2s ease-in-out;}
		.skills li{width: 15%;height: 240px;overflow: hidden;}
		.skills li a{display: block;width:100%;height: 240px;position: relative;overflow: hidden;}
		.skills li a .skills-con{width: 100%;height: 100%;margin-top: 50%;color: #006600;font-size: 2.5rem;}
		.skills li a .skills-js{margin-top: 5%;transform:translateX(40px);}
		.skills li a .line{position: absolute;right: 0;top:0;width: 0;height:240px;border-right: 1px dashed #000;}
		.skills li a .mask{width: 100%;height: 100%;background-color: #CCC;opacity: 0.3;position: absolute;top: 0;left: 0;}
		.skills li.big{width: 25%;}
		.skills li.big a .skills-con{width: 40%;height: 100%;margin-top: 30%;font-size:2rem;}
		.skills li.big a .skills-js{width: 60%;height: 100%;text-shadow:none;font-weight: bold;color: #555;}
		.skills li.big a:hover .skills-js{transform:translateX(0);transition:transform 0.1s ease-in-out  0.5s;-o-transform:translateX(0);-o-transition:transform 0.1s ease-in-out  0.5s;-webkit-transform:translateX(0);-webkit-transition:transform 0.1s ease-in-out  0.5s;-moz-transform:translateX(0);-moz-transition:transform 0.1s ease-in-out  0.5s;-ms-transform:translateX(0);-ms-transition:transform 0.1s ease-in-out  0.5s;}
		.skills li.big a .mask{opacity: 0;}
 		.work{overflow: hidden;margin-top: 4%;}
		#work-con{display: table-cell;vertical-align: middle;margin-top: 2rem;}
		.reels{width: 100%;height:100%;overflow: hidden;position: relative;}
		.reels-con{overflow: hidden;width: 100%;height: 100%;position: absolute;top: 0;left: 0;}
		.reels-con li{width: 100%;height: 100%;float: left;padding-top: 10%;}
		.reels h1{position: absolute;top: 10%;left: 36%;z-index: 1000;}
		.reels-con li .reels-con-img{overflow: hidden;height: 100%;padding-top: 10%;padding-left: 10%;position: relative;}
		.reels-con li .reels-con-txt{padding-top: 5%;}
		.reels-con li .reels-con-txt p{width:70%;color: #333;}
		.reels-con li .reels-con-img img{width: 70%;height: 300px;} 
		.reels-con li .reels-con-img img:hover{transform:scale(1.2,3);transition:all 0.5s ease-in-out 0.2s;z-index: 10000;position: absolute;} 
		.reels-con li .reels-con-img img:nth-of-type(1){position: absolute;left: 5%;top: 5%;}
		.reels-con li .reels-con-img img:nth-of-type(2){position: absolute;left: 10%;top: 15%;}
		.reels-con li .reels-con-img img:nth-of-type(3){position: absolute;left: 15%;top: 25%;}
		.reels-con li .reels-con-img img:nth-of-type(4){position: absolute;left: 20%;top: 35%;}
		.reels-con li .reels-con-img img:nth-of-type(5){position: absolute;left: 25%;top: 40%;}
		#reels-2{}
		#reels-3{}
		#reels-nav{position: absolute;left: 45%;bottom: 10%;}
		#reels-nav a{display: block;width: 16px;height: 16px;border: 1px solid #CCC;border-radius: 50%;background-color: #383cf1;opacity: 0.5;margin: 0 10px;}
		.contact{width: 80%;border: 2px solid #FFF;border-radius: 10px;padding: 10%;margin-left: 10%;margin-top: 4%;overflow: hidden;}
		.contact-txt li{line-height: 3rem;}
		.contact-txt li a{font-size: 2rem;}
		#contact-img{width: 16rem;height: 16rem;overflow: hidden;}
		#contact-img img{width: 16rem;height: 16rem;}
	</style>
</head>
<body>
	<nav>
		<ul>
			<li class="left"><a href="#section0">关于我</a></li>
			<li class="left"><a href="#section1">专业技能</a></li>
			<li class="left"><a href="#section2">工作经历</a></li>
			<li class="left"><a href="#section3">作品集</a></li>
			<li class="left"><a href="#section4">联系我</a></li>
		</ul>
	</nav>
	<div id="container" data-PageSwitch>
		<div class="sections">
			<div class="section active" id="section0">
				<div class="intro">
					<h1 class="title">ABOUT ME</h1>
					<div class="container about">
						<div class="text-center left">
							<span>年龄/25</span>
						</div>
						<div class="text-center left">
							<span>姓名/张雨夜</span>
						</div>
						<div class="text-center left" style="border:none">
							<img src="../pc/images/me.png">
						</div>
						<div class="text-center left">
							<span>学历/本科</span>
						</div>
						<div class="text-center left">
							<span>专业/计算机科学<br>与技术</span>
						</div>
					</div>
					<p id="adout-my">天才是不足恃的，聪明是不可靠的，要想顺手拣来的伟大科学发明是不可想象的。</p>
				</div>
			</div>
			<div class="section" id="section1">
				<div class="intro">
					<h1 class="title">PROFESSIONAL SKILLS</h1>
					<div>
						<ul class="skills" id="skills">
							<li class="left big">
								<a href="###">
								<div class="skills-con left">
									HTML<br>
									<span>85%</span>
								</div>
								<div class="skills-js left">
									<p class="text-left">熟练HTML标记语言</p>
									<p class="text-left">深刻理解web标准</p>
									<p class="text-left">熟练HTML熟悉盒模型和各类布局方式、能够根据设计图实现页面布局和交互效果</p>
									
								</div>
								<i class="line"></i>
								<i class="mask"></i>
								</a>
							</li>
							<li class="left">
								<a href="###">
								<div class="skills-con left">
									CSS<br>
									<span>85%</span>
								</div>
								<div class="skills-js left">
									<p class="text-left">熟练运用css及css新特性</p>
									<p class="text-left">熟悉css3标准，能够解决常见兼容性问题</p>
								</div>
								<i class="line"></i>
								<i class="mask"></i>
								</a>
							</li>
							<li class="left">
								<a href="###">
								<div class="skills-con left">
									JavaScript<br>jQuery
								</div>
								<div class="skills-js left">
									<p class="text-left">
										原生js基础扎实，对闭包，作用域，对js面向对象编程的思想有一定的了解
									</p>
									<p class="text-left">
										熟悉js dom,event,ajax能够编写js原生代码
									</p>
									<p class="text-left">熟练掌握jQuery</p>
									<p class="text-left">注重javascript的性能优化</p>
									<p class="text-left" >正在深入学习angular</p>
								</div>
								<i class="line"></i>
								<i class="mask"></i>
								</a>
							</li>
							<li class="left">
								<a href="###">
								<div class="skills-con left">
									CSS3/HTML5
								</div>
								<div class="skills-js left">
									<p class="text-left">对HTML5 移动web应用有一定的了解</p>
									<p class="text-left" >正在深入学习angular</p>
								</div>
								<i class="mask"></i>
								<i class="line"></i>
								</a>
							</li>
							<li class="left">
								<a href="###">
								<div class="skills-con left">
									Bootstrap
								</div>
								<div class="skills-js left">
									<p class="text-left">掌握BootStrap框架，实践过响应式布局</p>
								</div>
								<i class="line"></i>
								<i class="mask"></i>
								</a>
							</li>
							<li class="left">
								<a href="###">
								<div class="skills-con left">
									skills
								</div>
								<div class="skills-js left">
									<p class="text-left" >熟练使用firebug，chrome调试工具调试代码</p>
									<p class="text-left" >了解网页中 SEO 的一些基本理念</p>
									<p class="text-left" >熟练使用ps,sublime,DW等工具进行前端页面手工式开发</p>
								</div>
								<i class="mask"></i>
								</a>
							</li>
						</ul>
					</div>	
				</div>
			</div>
			<div class="section" id="section2">
				<div class="intro">
					<h1 class="title1">WORK EXPERIENCE</h1>
					 <div class="work">
						<div class="col-md-5 text-right col-sm-6 col-xs-12">
							<h2>北京军颐中医医院</h2>
							<span>网络部/seo优化、修图及页面开发</span>
							<section>学习利用长尾关键词优化文章，提高百度、360等文章收录、提高网站权重<br>利用ps修改网站上banner图<br>简单的页面开发，改版</section>
						</div>
						<div class="col-md-2 col-sm-6 col-xs-12" id="work-con">2016/02<br>|<br>2016/6</div>	
					</div>
					<div style="clear:both"></div>
					<div class="work">
						<div class="col-md-2 col-md-push-5 col-sm-6 col-xs-12" id="work-con">2016/07<br>|<br>至今</div>
						<div class="col-md-5 col-md-offset-5 text-left col-sm-6 col-xs-12">
							<h2>中国民族建筑研究会</h2>
							<span>战略发展部/前端工程师</span>
							<section>负责官网页面设计、制作和维护，PSD切图后高度还原设计图<br>利用CSS3、JS、jQuery实现动画、特效，让页面更充实丰富。<br>把页面代码上传到服务器，并用标签语言调用后台数据，实现网站上线。</section>
						</div>
					</div>
				</div>
			</div>
			<div class="section" id="section3">
				<div class="reels">
					<h1 class="title">SAMPLE REELS 3</h1>
					<ul class="reels-con">
						<li class="left" id="reels-1">
							<div class="col-md-6 reels-con-img">
								<img src="../pc/images/qywz1.png">
								<img src="../pc/images/qywz2.png">
							</div>
							<div class="col-md-6 reels-con-txt">
								<h3>中国民族建筑研究会企业网站</h3>
								<p>技术实现：HTML、CSS3、javaScript、Bootstrap</p>
								<p>项目描述：使用HTML及CSS3对页面进行搭建，并实现动画交互，与开源后台用标签进行绑定，实现整个网站的上线</p>
								<p>实现技术：根据产品需求分析并给出最优的网页前端结构解决方案并完成效果实现。利用CSS+HTML以及Bootstrap框架将页面实现，高度还原设计图。用js、jQuery对页面进行特效制作</p>
								<p>项目收获：使用HTML CSS3对页面进行制作。熟练使用javascript、jQuery插件。对项目的前端流程有了一定的认识，为以后的项目积累了经验</p>
							</div>
						</li>
						<li class="left" id="reels-2">
							<div class="col-md-6 reels-con-img">
								<img src="../pc/images/dswz1.png">
								<img src="../pc/images/dswz2.png">
								<img src="../pc/images/dswz3.png">
								<img src="../pc/images/dswz4.png">
								<img src="../pc/images/dswz5.png">
							</div>
							<div class="col-md-6 reels-con-txt">
								<h3>电商网站</h3>
								<p>技术实现：HTML、CSS3、javaScript</p>
								<p>项目描述：根据效果图高度还原商品列表页、商品详情页、订单页，登录注册页、筛选页等</p>
								<p>实现技术：利用CSS3+HTML等将页面实现，高度还原设计图。用js、jQuery对页面进行特效制作</p>
								<p>项目收获：熟练使用HTML CSS对页面进行制作，效果显著。熟练原生javascript、jQuery的使用。</p>
							</div>
						</li>
						<li class="left" id="reels-3">
							<div class="col-md-6 reels-con-img">
									<img src="../pc/images/wz1.png">
									<img src="../pc/images/wz2.png">
									<img src="../pc/images/wz3.png">
								</div>
								<div class="col-md-6 reels-con-txt">
									<h3>企业网站</h3>
									<p>技术实现：HTML、CSS3、javaScript、Bootstrap</p>
									<p>项目描述：临摹简单的企业网站，网站结构使用HTML及CSS对页面进行搭建，用js、jQuery实现动画</p>
									<p>实现技术：利用CSS+HTML以及Bootstrap框架将页面实现。用js、jQuery对页面进行特效制作</p>
									
							</div>
						</li>
					</ul>
					<ul id="reels-nav">
						<a class="left" href="#reels-1"></a>
						<a class="left" href="#reels-2"></a>
						<a class="left" href="#reels-3"></a>
					</ul>
						
					
				</div>
			</div>
			<div class="section" id="section4">
				<div class="intro">
					<h1 class="title">CONTACT ME</h1>
					<div class="contact">
						<ul class="col-md-6 text-right">
							<div id="contact-img">
								<li id="tel"><img src="images/tel.png"></li>
								<li id="qq"><img src="images/weixin.png"></li>
								<li id="wx"><img src="images/weixin.png"></li>
								<li id="yx"><img src="images/email.png"></li>
								<li id="wb"><img src="images/email.png"></li>
							</div>
						</ul>
						<ul class="contact-txt col-md-6 list-group text-left">
							<li class="list-group-item-primary text-left"><a href="#tel">电话：17735552370</a></li>
							<li class="list-group-item-primary text-left"><a href="#qq">Q Q：1433711422</a></li>
							<li class="list-group-item-primary text-left"><a href="#wx">微信：z1433711422</a></li>
							<li class="list-group-item-primary text-left"><a href="#yx">邮箱：17735552370@163.com</a></li>
							<li class="list-group-item-primary text-left"><a href="#wb">微博：17735552370</a></li>
						</ul>
						
					</div>
				</div>
			</div>
		</div>
	</div>
	<script type="text/javascript" src="jquery-1.11.2.min.js"></script>
	<script type="text/javascript" src="pageswitch.js"></script>

	<!--<script type="text/javascript">
	$("#container").PageSwitch({
		direction : "horizontal"
	});
	</script>-->
</body>
</html>
