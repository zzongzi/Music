# Music
红岩网校移动开发部寒假作业

<br><br>
# APP介绍
## 1.功能

  APP使用了网易云的部分接口 目前实现了搜索音乐 播放音乐 通过SQ数据库储存最近播放音乐的功能 
  
  部分具体功能的介绍:
  在点击音乐时会跳转到含有该音乐相应信息的PlayActivity 若暂无音乐正在播放/正在播放的音乐ID与之不同 则会start service来播放该音乐 若该音乐已在播放中 则点击音乐后保持原service继续播放
  在PlayActivity中可进行 拖动进度条 暂停 上一首 下一首 等操作 
  当音乐播放时通知栏会有相应通知介绍 点击通知可跳转回APP中该音乐的PlayActivity
  播放的音乐若为网易云付费歌曲 会弹出提示试听的区间
  音乐播放完毕后会自动播放最近播放列表的下一首歌
  最近播放列表会实时刷新播放音乐顺序(注:用户在PlayActivity中点击上/下一首以及播放完毕后自动播放时采用的顺序是原列表中顺序 返回后会刷新顺序 )
## 2.设计思路
  使用MVP架构 在各个presenter里获得和处理数据 若要更新UI 则调用相应activity中接口方法进行数据的刷新
  具体实现方法就是通过网络请求获取需要的数据 存入Music对象中 在进行音乐信息的展示 播放等操作时 从Music对象中取出需要的数据进行操作
## 3.功能展示
![imager](gif/1613728598398.gif)

  
