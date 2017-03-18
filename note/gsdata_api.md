# 清博API

1. 申请API权限，获得平台分配的APPID & APPKEY
  APPID:j976M9LNSF9VAMh3yC29
  APPKEY:83G1a02fqATcNdn47zQcgzVDz

2. 下载/应用SDK
  [gsdata-python-sdk](https://github.com/superalsrk/gsdata-python-sdk/blob/master/README.md)

  安装：`$ pip install -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com gsdata`

  使用:
  ```python
  from gsdata import Gsdata

  #创建客户端
  client = Gsdata("YOUR_APP_ID", "YOUR_APP_SECRET")

  #获取用户信息
  ret1 = client.sys_user_info('saber@stackbox.org')

  #用户名验证
  ret2 = client.sys_check_user('saber@stackbox.org')

  #其他API, 第一个参数为API地址, 第二个参数为请求参数字典(除去appid和appkey)
  ret3 = client.call('/api/wx/wxapi/wx_content', {'url':'http://mp.weixin.qq.com/s?__biz=MzAxOTEyMDI1MQ==&mid=400950548&idx=3&sn=cca852f541f93c53633a4e0069230313&3rd=MzA3MDU4NTYzMw==&scene=6#rd'})
    
  ```
















## Change logs
2017.03.12 Initial Draft by Zephyr
