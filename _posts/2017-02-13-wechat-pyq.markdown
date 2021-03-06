---
layout:     post
title:      "朋友圈发复制粘贴的长文字时 显示'全文'按钮"
subtitle:   "强迫症必看"
date:       2017-02-13
author:     "Doupeng"
header-img: "img/post-bg-wechat-pyq.jpg"
tags:
    - 微信
    - 朋友圈
---

> 你肯定云见过这种事情，当你看到某页面精彩的一段话时，想发到朋友圈，你发现我复制过来时明明是分行得很规矩，为什么点击发送后任然是归结为一行，而不是显示'全文'点击按钮呢

## 一、先来看一下令我苦恼的事情！

- 我们复制粘贴过来的文字 (随意粘贴过来的，测试啦)

![img](/img/wechat-pyq-1.jpg)

- 朋友圈中的效果

![img](/img/wechat-pyq-2.jpg)

- 想看全部内容的效果

![img](/img/wechat-pyq-3.jpg)

- 以上结果令我很不满意 😫😫😫

## 二、简单说一下朋友圈的机制

> 可能不对啦!(猜测😅😅😅)

```
是否显示`全文`或者显示为`一行`有两个标准：`6行文字`,`400字符(200字)`
1 手写，超过6行就会出现`全文`按钮
2 复制，超过6行，但字符长度小于400(200字)，出现`全文`按钮
3 复制，字符长度大于400(200字)，显示为`一行`
```

大概就是这个样子啦！😉😉😉

## 三、回顾一件事

这是之前微信的一个bug，大家玩的都很嗨😁😁😁

![img](/img/wechat-pyq-4.jpg)

如果你现在按照网上的教程再试一遍就会得到以下的提示了,因为bug修复了

![img](/img/wechat-pyq-5.jpg)

虽然这个不能使用了但是我们可以实现以下效果

使用这组标签我们发出去的文字在我们的手机上的显示效果是这样的

![img](/img/wechat-pyq-7.jpg)

但是好友接受的信息是正常的，是不是很炫酷，这样我们在公共场合也不怕别人偷窥我们的手机屏幕了，或者我们发送游戏账号密码，别人翻我们的手机看到的密码也是倒着的

![img](/img/wechat-pyq-6.jpg)

由此可见，可以想象，当你复制字符长度大于400(200字)时，朋友圈应该会生成某些标签把你的文字压缩显示成一行。(这些是猜测啦)

## 四、怎么解决

- 1.我们先手动输入一句话，比如`我喜欢@猿来如此`
- 2.然后选取`我喜欢@猿来如此`中的`欢@猿来`复制粘贴替换掉
- 3.最后在删掉头部的`我喜`和尾部的`如此`

如果失败请重复1,2,3 因为我成功了😈😈😈

有什么好的建议请留言
