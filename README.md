# 实现空间搜索遇到的问题和解决方案

# 12-18-17
经过2个月的lbs软件开发(服务器代码两个个星期, 剩下都是前端的活), 
目前在优化空间搜索这个事儿, 
============================================================================================
开始用的是 : 
经纬度转成geohash, 然后存数据库, 查周围9个框用where in like "?%" 查出来(百度查出来的),

因为当时测试不够精准, 感觉够用代码也容易写, 但是现在发现无法实现像美团或者探探那样,
按照距离排序, 
============================================================================================
我上google查了一下发现这个https://www.plumislandmedia.net/mysql/haversine-mysql-nearest-loc/
这个哥写的比较有逻辑, 

实现方法总结 : 就是把距离转换成经纬度, where between 一下

原文说 :  takes advantage of your latitude and longitude indexes and works efficiently.
不过我不信, 美国的数据跟中国数据量不能比, 我准备实验一下, 毕竟能实现距离排序
============================================================================================

