# 消息分发

开普勒消息分发

> 公告：由管理员在后台公告管理中，发布公告，可以选择接收对象（指定个人，指定业务线，全部）
>
> 通知：由项目操作事件时产生，如构建，回滚，删除应用等
>
> 告警：由prometheus发出，开普勒通过对外提供API，接收到告警信息，然后根据规则分发

**消息流程：**

消息产生后，先压到MQ对应的队列，消息中心定时分任务会时时从MQ队列取出消息，然后根据订阅配置和接收权限来分发给接收者。

**接收终端：**

站内信，邮件，微信，短信，其它方式

**订阅配置：**

接收者可以在用户中心->订阅配置里，自定义配置接收的事件类型和接收终端方式。

**分发流程图：**

![](http://source.qiniu.cnd.nsini.com/images/2019/08/53/cd/d5/20190819-839edadc08a45c5bd2eb78d7cd153514.jpeg?imageView2/2/w/1280/interlace/0/q/70)
