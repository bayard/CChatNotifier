<<<<<<< HEAD
# CChatNotifier
A WoW Classic addon that can be used to filter chat for custom keywords. It will then notify you whenever it finds them in chat messages.

This is my minimalistic idea of a "LFG" addon. I don't want to look at chat 24/7 but also don't want to miss relevant messages. The more elaborate LFG addons are imho overkill, and at the same time not flexible enough, I don't need a list or anything, I just don't want to miss a message containing arbitrary things if it pops up. This solves that problem just fine, at least its ugly predecessor I had for vanilla pservers did.

## Features
* Create custom keyword groups to be looked for in chat (channels, say and yell).
* GUI to manage everything.
* If a word is found it will notify you in chat, optionally plays a sound too.
* Chat window for notification can be chosen, tab will flash when not shown.
* Name in notification can be clicked to open /whisper.
* Individual keyword groups or whole addon can be toggled on/off.

![The UI](images/ui.png)

![Word found](images/found.png)

#### Note
Not tested in classic yet, notification sound probably throws an error, settings button texture probably missing. Otherwise *should* work. Will test and fix once I have access to the game again.

=======

# 汉化版额外添加功能

* 添加了防刷屏机制
* 支持职业色显示
* 搜索关键字支持组合和过滤
    * aaa 直接搜索包含aaa的信息, 如 "血色" 将匹配 "血色自强" "血色aa队" 等等...
    * aaa&bbb 搜索同时包含aaa和bbb的信息, 如 "zul&自强" 可匹配 "zul来人,自强任务队"
    * aaa-bbb 搜索包含aaa 但不包含bbb的信息, "血色-aa" 匹配包含的 "血色"的信息,但会过滤掉如"血色来人,aa队"...
    * -aaa 以减号开头,不包含&的字段, 这算是全局过滤, 会对其他所有搜索结果 都过滤掉包含"aaa"的信息. 例如 如果根本不想看到任何AA队,那搜索的时候不必像"zul-aa" "深渊-aa" "监狱-aa" 这样 每一个搜索字段都加一个"-aa"尾巴, 而只要单独添加一个"-aa", 即可从本插件转发的所有消息中过滤掉"aa".
    * &和-的字段可以任意组合, "黑石&任务-aa&自强" 将匹配同时包含"黑石""任务""自强" 但不包含"aa"的信息
    * 以上字段,可以用逗号隔开 编成一组, 就是图中插件界面上的一行, 受同一组功能按钮的控制(添加,编辑,删除,暂停和启用)

[NGA贴子](https://bbs.nga.cn/read.php?&tid=18499801)

========
2020.05.04 支持 Global Ignore List

