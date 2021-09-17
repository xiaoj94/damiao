# 剑网3插件集 数据下载仓库


## 仓库说明
> 根仓库名称为"JX3_LR_DATA"，如果你没有这个仓库，请查看该仓库根目录下的"建立数据仓库教程.docx"，查看如何新建数据下载仓库
> #### 懒人团队面板相关
> > 1. 懒人团队面板数据存放目录为根目录下的`\LR_TEAM_GRID`，插件会读取该目录下的info.txt文件，解析数据文档的下载相关配置  
> > 2. info.txt文件编码必须为UTF8格式，不然，插件内会显示为乱码
> > 3. info.txt文件格式说明,info.txt内容为一段json代码，请按照json代码的格式进行编写
> >    ```
> >     {"rss_name":"xx","szText":"默认数据55","author":"华契@电一 蝶恋花","desc":"懒人插件团队面板数据","data":[
> >     {"title":"副本数据","family":"dungeon","version":"v20191224","update_time":"20191224","desc":"默认副本数据","file":"DungeonData.jx3dat"},
> >     {"title":"自定义数据","family":"custom","version":"v20191223","update_time":"20191223","desc":"默认数据","file":"CustomData.jx3dat"},
> >     {"title":"边角指示器数据","family":"edge","version":"v20191223","update_time":"20191223","desc":"默认数据","file":"EdgeIndicatorData.jx3dat"}
> >     ]} 
> >     说明：
> >     第一行中，
> >     rss_name：后面填写你的rss订阅名称，通常为你的码云用户名，该字段用于验证订阅可靠性。
> >     szText：用于插件内名称的显示。
> >     author：填写作者名称，用于插件内显示
> >     desc：填写描述信息，用于插件内显示
>
> >     第二行开始，每行为一个数据文件的描述信息，仅以第二行进行说明
> >     title：数据的标题，用于插件内显示
> >     desc：数据描述，用于插件内显示
> >     family：家族，重要！每个rss订阅号中的数据，同名的family只能存在一个，多余的会自动滤除。
> >          该字段用于插件更新的检验。当使用的数据更新时，同rss订阅号下同family名，但version不一致的数据会提示“新！”
> >     version：插件版本，可随意写，用于插件数据的更新检验。建议有序递增
> >     update_time：更新日期，用于插件内显示
> >     file：文件名称，用于数据下载。两种格式：1)只有文件名，游戏内则会自动补全地址到`JX3_LR_DATA\LR_TEAM_GRID\zhcn/zhtw)'，此时限制文件大小为1M。2)包含'http'的完整路径地址，此时会采用完整路径地址进行下载，适合数据为码云发行版地址中的文件地址或者外部网站数据的地址。
> >
> >     ```
> >     4. 国服的团队数据文件请放在`JX3_LR_DATA\LR_TEAM_GRID\zhcn`下，台服文件请放在`JX3_LR_DATA\LR_TEAM_GRID\zhtw`下
> >     5. 数据文件的名字请和info.txt文件中的file对应
> >     6. 团队面板数据下载缓存地址：`interface\LR_Plugin@DATA\LR_TeamGrid\BUFF\WebDown`，注意，相同rss订阅号下的同一个family，同一个version的文件只会下载一次

