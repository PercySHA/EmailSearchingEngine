<<<<<<< HEAD
# bool查询和语义检索
## 语言
python 3.7.3<br>
## bool查询
=======
# Email Searching Engine
## introduction
An email searching engine based on Enron Email Database, which provides bool search and semantic search.<br>
Maintained by <br>
[Yunhao Sha](https://github.com/PercySHA/)([percy@mail.ustc.edu.cn](mailto:percy@mail.ustc.edu.cn))<br>
[Shuyi Zhang](https://github.com/iridiumine)([iridiumine@mail.ustc.edu.cn](mailto:iridiumine@mail.ustc.edu.cn))<br>
## Language
python3<br>
## bool search
>>>>>>> 3bbc526683b615bdc4bd2fa6624cb945d612de47
### 预处理文件
每个文件用两个16进制数编号，前2位是所在的第一路径，后两位是所在的第二路径，并生成文件编号和文件路径的字典文件，记为文件1<br>
修改文件，仅保留主题和正文，主题：subject->’\n’ 正文：空行后到EOF，并生成文件路径和文件主题的字典文件，记为文件2<br>
### 分词处理 
存储：字典<br>
正排表：文档编号 包含的词，记为文件3<br>
建立倒排索引表：词 所在的文档编号，记为文件4<br>
### 完成bool查询
输入一个词，查询其在文件4中的文件编号，并利用文件编号，在文件1中搜索文件路径，最后用文件路径，在文件2中搜索其对应的主题，输出主题集合，完成查询<br>
