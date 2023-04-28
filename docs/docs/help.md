# 详细帮助

## 功能一览

- 发言数据统计
- Quote(载入史册)
- 群内文字命令互动
- 获取群头衔/互赠头衔
- 开发中...

## 命令

| 命令   | 说明              |
| ------ | ----------------- |
| /help  | 显示帮助信息      |
| /start | 开始使用          |
| /q     | 载入史册          |
| /d     | 移出史册          |
| /c     | 清空史册          |
| /t     | 获取头衔/互赠头衔 |
| /setqp | 设置发名言概率      |
| /rank  | 群统计信息        |

## 数据统计

Kmua 会对自己收到的消息进行记录和统计, 每个群聊(Chat)和用户(User)都会有自己的数据

在群内发送 /rank 可获取当前的统计信息

![群组统计](./images/grouprank.png)

私聊 Kmua 可获取自己的数据统计信息

![个人统计](./images/userrank.png)

## Quote

使用 `/q` 回复一条消息, Kmua 将会把这条消息置顶并记录到一个列表中, 每个群聊之间的列表相互独立

如果这条消息属于文字消息, Kmua 将会生成一张图片, 示例如下(右下角是用户名,此处被码掉了)

![quote图片示例](./images/quoteexp.png)

当收到新消息时, Kmua 有概率从列表中随机选择一条被记录的消息, 并转发

这个概率可以通过 `/setqp` 来设置, 默认为 0.1 , 范围是 [0,1] 的小数

### 内联查询

在任意输入栏艾特 Kmua 即可查询自己的名言

当不输入其他内容时, 最多随机显示十条

![InlineQuery](./images/inlinequery.png)

支持搜索

![InlineQueryWithQuery](./images/inlinequerywithquery.png)


## 群内互动

使用斜杠加文字 回复一条消息, 即可与所回复消息的发送者互动

示例:

![interact1](./images/interact1.png)

![interact2](./images/interact2.png)

使用反斜杠可以主客(攻受)互换:

![interact3](./images/interact3.png)

如果不回复消息, 则是对自己使用:

![interact4](./images/interact4.png)

![interact5](./images/interact5.png)

如果你的互动内容中含有会被识别成 Bot 命令的内容(如 /rua 会被当作一个命令), 为了避免混乱, 此时 kmua 不会对其响应.

你可以使用两个斜杠避免这个问题 ( //rua )

## 获取与互赠群头衔

为 Kmua 赋予足够的管理员权限, 群员可以使用 `/t` + 自定义内容 获取自定义头衔

如不指定自定义内容, 则默认为用户的用户名

可以互相赠予头衔, 使用 `/t` + 自定义内容 回复一条消息即可, Kmua 会将头衔赋予被回复者(如果已经有头衔, 则更改)

互赠时, Kmua 发送的内容是 "{当前用户}把{被回复用户}变成了{自定义头衔}!"

当然, 你可以自己回复自己

## 更多

开发中...