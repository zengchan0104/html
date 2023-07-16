
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>前端播放m3u8格式视频</title>
    <!--https://www.bootcdn.cn/video.js/-->
    <link href="https://cdn.bootcss.com/video.js/7.6.5/alt/video-js-cdn.min.css" rel="stylesheet">
    <script src="https://cdn.bootcss.com/video.js/6.6.2/video.js"></script>
    <!--https://www.bootcdn.cn/videojs-contrib-hls/-->
    <script src="https://cdn.bootcss.com/videojs-contrib-hls/5.15.0/videojs-contrib-hls.min.js"></script>

    <!-- //百度压缩版 -->
    <script src="http://libs.baidu.com/jquery/2.1.4/jquery.min.js"></script>
</head>
<body>
	<div class="wrapper">
			<div class="videocontent">
				<video id="myVideo" class="video-js vjs-default-skin vjs-big-play-centered vjs-16-9"  controls  height="auto" preload="auto"  data-setup='{}'>    
						  <source id="source" src="https://1080p.jszyplay.com/play/0dN2oXKd/index.m3u8"  type="application/x-mpegURL">
				</video>
			</div>
	</div>
</body>
<style>
body {
	padding: 0;
	margin: 0;
}
div.videocontent {
	width:100%;
}
div.wrapper {
	max-width:750px; 
	margin: 0 auto;
}
</style>
<script>    
    // videojs 简单使用  
    var myVideo = videojs('myVideo',{
        bigPlayButton : true, 
        textTrackDisplay : false, 
        posterImage: false,
        errorDisplay : false,
    })
    myVideo.play() // 视频播放
    myVideo.pause() // 视频暂停
</script>


</html>
