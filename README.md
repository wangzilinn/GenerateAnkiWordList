# BingOnlineDictToAnkiWordList
从在线必应词典爬取信息生成Anki可用的单词本
#### 第一版示例:
![image](https://github.com/wangzilinn/BingOnlineDictToAnkiWordList/blob/master/example.gif)
#### 第二版示例
![image](https://github.com/wangzilinn/BingOnlineDictToAnkiWordList/blob/master/example2.0.gif)
### 最近这几天每天都在背单词，发现了按照记忆曲线复习的单词本anki，觉得简直是神器，几天下来背单词的效率提高了不少。
### 但是每天把单词添加到单词本要花费不少时间，其典型过程是：
1. 找到要背的单词
2. 去百度/谷歌/必应搜索释义、例句等
3. 把搜索到的东西粘贴到单词本上
为了加深印象，很多步骤都是手打，而不是直接复制（后来发现并没有什么卵用）
### 为了节省时间，又拿起了许久不用的python写了个带图形界面的脚本，界面很简单，包括：
1. 单词查询控件
2. 确认按钮
3. 查询结果区
4. 生成单词本按钮
### 操作方法：
1. 将要添加的单词放入单词查询控件
2. confirm
3. 所有单词添加完毕后，output
### 程序流程：
1. 获取用户单词
2. 去必应词典网站爬取该单词的释义与例句
3. 格式化爬取数据
4. 输出到文件
### 使用时注意：
1. 源码已经放上了，需要一些不是自带的的库，没有的话自己去装吧
2. 输出文件的路径是我自己的，需要自己修改
3. 如果查询单词输入错误，bing返回了信息（该单词存在），把查询结果区的新添加的部分删除即可（注意格式上下一致）
4. 如果查询单词输入错误，bing未返回信息（该单词不存在），会在后面的控制台输出错误信息，不过程序不会奔溃，输入新单词即可
### 修改源码时注意：
1. 源码已经放上了，需要一些不是自带的的库，没有的话自己去装吧
2. 输出文件的路径是我自己的，需要自己修改
3. 未使用百度和google的原因是他们网站都做了处理（混淆和ajax），图省事用了bing
4. anki输出需要utf-8格式的输出，所以普通的打开文件操作是不行滴，要使用import codecs库
