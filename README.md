<!--
 * @Author: v_polixiong v_polixiong@tencent.com
 * @Date: 2022-08-23 09:35:50
 * @LastEditors: v_polixiong v_polixiong@tencent.com
 * @LastEditTime: 2022-08-23 10:48:52
 * @Description:
-->

# daily_reminder

自动化定时推送微信天气

## 操作流程

1.  [查看git链接](https://github.com/Mumu991/weather)
2. 直接fork、然后修改config.txt里面的内容
3. 需要用到的api地址
   1. [微信公众平台测试接口](https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login) ps: 能获取到 appID、appsecret、用户微信号、模板ID
      1. 用户微信号需要接受消息的用户扫描测试号二维码
      2. 模板ID需要 新增测试模板（模板内容见文末）
   2. [和风天气apikey](https://dev.qweather.com/) ps: 需要注册 -> 控制台 -> 应用管理 -> 创建应用

4. actions测试是否可以接收
5. 因为git定时任务不准时 || 有时候不执行 需要使用云函数提供cron调度服务 [地址](https://blog.csdn.net/l1937gzjlzy/article/details/117753465)

模板内容如下：

{{date.DATA}} 

当前城市：{{region.DATA}} 

天气(白天 / 晚上)：{{weatherDay.DATA}} 

气温(最高 / 最低)：{{temp.DATA}} 

风向：{{wind_dir.DATA}} 

温馨提示(穿衣)：{{dresses.DATA}} 

温馨提示(紫外线)：{{uv.DATA}} 

今天是我们相识的第{{love_day.DATA}}天 

{{birthday1.DATA}} 

明天天气：{{tomDay.DATA}} 

明天气温：{{tomTemp.DATA}} 

{{note_ch.DATA}} 

{{note_en.DATA}}
