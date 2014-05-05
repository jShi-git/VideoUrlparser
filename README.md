VideoUrlparser
==============

分析优酷、土豆等视频网站的播放页面，获取视频标题、视频截图、M3U8地址以及插入页面的swf地址。

Usage
========

require_once "VideoUrlParser.class.php";
$urls[] = "http://v.youku.com/v_show/id_XMjI4MDM4NDc2.html";
$urls[] = "http://www.tudou.com/programs/view/ufg-A3tlcxk/";

foreach($urls as $url){
     $info = VideoUrlParser::parse($url);
     echo "<a href='{$info['url']}' target='_new'>{$info['title']}</a>";
     echo "<br />";
     echo $info['object'];
     echo "<br />";
}
