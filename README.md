# initphp
InitPHP是一款轻量级的PHP开源框架。InitPHP采用了BSD开源协议。
1、新建项目根目录：
	mkdir myproject/
	cd myproject
	mkdir conf
	touch comm.conf.php;
2、复制initphp框架主文件
	cp initphp ./myproject/
3、创建入口文件
touch index.php
4、配置入口文件
vim index.php
	//定义项目目录
	define('APP_PATH',dirname(__FILE__));
	//设置字符集内容类型
	header('Content-Type:text/html; charset=utf-8');
	//加载框架主文件
	require_once('./initphp/initphp.php');
	//加载应用目录下自定义配置文件
	require_once('./Application/conf/comm.conf.php');
	//初始化框架
	Initphp::init();
5、配置项目详细
	从主框架文件中initphp.conf.php中复制要配置的选项到./conf/comm.conf.php文件中；
	//配置站点，设置项目的目录
	$InitPHP_conf['url'] = 'http://localhost/initPhp/';
	//开启调试
	$InitPHP_conf['is_debug'] = true;
	//设置日志文件位置
	$InitPHP_conf['log_dir'] = 'Application/logs/';
	详细配置请看更多
6、配置好后浏览器输入localhost/myproject/index.php?c=controllerName&a=actionName访问
7、官方网址：http://initphp.com/
