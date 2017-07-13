# app与云平台之间的接口

## 总接口文档
http://114.215.90.83:8093/v1/swagger-ui.html

## 给app使用的接口列表
说明：从登录登出外，其他接口如何使用，均参照“总接口文档”
```
0、登录  
/v1/login  POST   FormData username: zoujian, password:zj

http://114.215.90.83:8093/v1/login


1、退出登录
/v1/logout   GET

http://114.215.90.83:8093/v1/logout


2、获取站点列表
/stations  GET


3、获取某个站点的某个变量组
/stations/{station_sn}/vargroups/{name}  GET

站点总监控页面， 变量组的名字，暂约定为：M_TWO_MOST_IMPORTANT

各个站点概览页， 变量组1的名字，约定为：M_关键数据
各个站点概览页， 变量组1的名字，约定为：M_实时曲线
各个站点概览页， 变量组3的名字，约定为：M_发电贡献


4、获取某个变量组其变量的实时值
/vargroups/{id}/VarRealtimeDatas  GET


5、获取某个变量组其变量的统计值，即某个时间段的所有值。
/vargroups/{id}/VarStatisticalDatas  GET


6、获取该用户下，所有相关的事件信息（用户所有相关站点的所有事件信息）
/stations/events   GET  支持条件过滤


7、获取某个站点下的设备列表
/stations/{station_sn}/devices GET 
TODO：当前还有没 状态 字段。


8、获取某个站点下某个设备 的 一些关键指标变量，TODO，待分析
```
