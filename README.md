
# i茅台预约工具----GitHub Actions版

### 功能：
- [x] 集成Github Actions
- [x] 多账号配置
- [x] 账号有效期管控
- [x] 手机号加密保存
- [x] 自动获取app版本
- [x] 微信消息推送

### 原理：
```shell
1、登录获取验证码
2、输入验证码获取TOKEN
3、获取当日SESSION ID
4、根据配置文件预约CONFIG文件中，所在城市的i茅台商品
```


### 使用方法：

### 1、安装依赖
```shell
pip3 install --no-cache-dir -r requirements.txt
```

### 2、修改config.py，按照你的需求修改相关配置，这里很重要，建议每个配置项都详细阅读。


### 3、按提示输入 预约位置、手机号、验证码 等，生成的token等。很长时间不再需要登录。支持多账号，支持加密。
1. 第一次使用先清空`./myConfig/credentials`中的信息，或者直接删除`credentials`文件也可以
2. 再去配置环境变量 `GAODE_KEY`,再运行`login.py`.
```shell
python3 login.py
# 都选择完之后可以去./myConfig/credentials中查看
```

### 4、python3 main.py ,执行预约操作
```shell
python3 main.py
```

### 5、配置 Github actions，每日自动预约，省去自己买服务器的成本。
- 先Fork本项目，再去自己的项目中配置`PUSHPLUS_KEY`和和`PRIVATE_AES_KEY`

## 特别感谢
原作者：https://github.com/397179459/iMaoTai-reserve




