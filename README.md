# simple_webrtc_server_demo
在原有另外一个大神开发的基础上实现了最简单的webrtc网关，可以实现群组通话。https://www.jianshu.com/p/61e3c9e13456


原有demo只能实现将一个服务端视频或语音文件，通过浏览器webrtc播放。这里增加了上行流，和流转发。


基础原理就是，将一个端收到的rtp包，取出编码数据，然后重新封包转发给其它用户。每个用户都有一个队列用户存放待发送的包。

