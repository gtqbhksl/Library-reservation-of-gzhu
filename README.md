# Library-reservation-of-gzhu
由于云函数有免费额度，只能抛弃之。

在[原来大佬的基础](https://github.com/lighthookyu/gzhu-libbooking-master) 上改为了GitHub的工作流运行

为了保护各位的隐私，建议新建一个私人仓库（**Private**），然后Import code这个仓库

把config.json里面的username改为自己的学号、password改为密码

seat_id改为座位号，目前代码只允许预约101房间的位置（有想改的可以自己更改，只会copy的就按照代码来

workflows里面都写好了，每天6：31进行登录预约（想6：30预约的自己改

在settings里面开启actions功能（settings-actions-general-Allow all actions and reusable workflows-save）

就会按照已经写好的定时去执行了，也可以点击actions模块查看运行的结果

没有写提醒，因为预约成功企业微信自动会发通知

交友别摆鸿门宴，社会玩的是牌面--wangge

下面是原作者README

--------------------------------------------------
# gzhu-libbooking-master
图书馆自习室自动预约
`cfg.json`设置如下：  
```json
{
  "username": "账号",
  "password": "密码",
  "room": "101或者103",
  "habit": [
    {
      "seat_id": "101-001",
      "bt": "08:30:00",
      "et": "12:30:00"
    },
    {
      "seat_id": "101-001",
      "bt": "13:00:00",
      "et": "17:00:00"
    },
    {
      "seat_id": "101-001",
      "bt": "18:00:00",
      "et": "20:00:00"
    }
  ]
}
```
意思就是预定101-001座位的三次，可以根据需要自行删减。但格式一定要对。  

serverless分支：挂载在腾讯云函数，设置好触发器即可。
server分支：若你有服务器的话可以运行到服务器中实现自动签到。  
PS.工具是解放双手，预约座位后请按时入座，不要浪费资源。  
