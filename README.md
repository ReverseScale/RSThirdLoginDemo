# RSThirdLoginDemo
第三方登录 Demo, 支持微信、微博、QQ三种登录方式，根据网络资源整理（请根据实际情况配置参数）

---
![](https://img.shields.io/badge/platform-iOS-red.svg) 
![](https://img.shields.io/badge/language-Objective--C-orange.svg) 
![](https://img.shields.io/badge/download-77.3MB-brightgreen.svg)
![](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg) 

在 BTA 统治下的中国市场，一款 App 没有第三方登录都混不下去...

| 名称 |1.列表页 |2.展示页 |3.回调页 |
| ------------- | ------------- | ------------- | ------------- |
| 截图 | ![](http://og1yl0w9z.bkt.clouddn.com/17-9-15/56726393.jpg) | ![](http://og1yl0w9z.bkt.clouddn.com/17-9-15/72168859.jpg) | ![](http://og1yl0w9z.bkt.clouddn.com/17-9-15/24323494.jpg) |
| 描述 | 通过 storyboard 搭建基本框架 | 跳转至 QQ 授权 | 参数回调结果页 |

 
## Advantage 框架的优势
* 1.文件少，代码简洁
* 2.目录结构清晰，整理排布有序
* 3.具备较高自定义性


## Requirements 要求
* iOS 7+
* Xcode 8+


## Usage 使用方法
### 第一步 引入头文件
```
#import "SRThirdSocialManager.h"
```
### 第二步 简单调用
登录请求方法：
```
+ (void)loginRequest:(SRThirdSocialType)thirdSocialType loginSuccess:(SRThirdSocialLoginSuccess)loginSuccess loginError:(SRThirdSocialLoginError)loginError {
    
    switch (thirdSocialType) {
        case SRThirdSocialWX:
        {
            [SRWXManager loginRequestWithLoginSuccess:loginSuccess loginError:loginError];
            break;
        }
        case SRThirdSocialWB:
        {
            [SRWBManager loginRequestWithLoginSuccess:loginSuccess loginError:loginError];
            break;
        }
        case SRThirdSocialQQ:
        {
            [SRQQManager loginRequestWithLoginSuccess:loginSuccess loginError:loginError];
            break;
        }
    }
}
```

授权请求方法：
```
+ (void)authRequest:(SRThirdSocialType)thirdSocialType authSuccess:(SRThirdSocialAuthSuccess)authSuccess authError:(SRThirdSocialAuthError)authError {
    
    switch (thirdSocialType) {
        case SRThirdSocialWX:
        {
            [SRWXManager authRequestWithAuthSuccess:authSuccess authError:authError];
            break;
        }
        case SRThirdSocialWB:
        {
            [SRWBManager authRequestWithAuthSuccess:authSuccess authError:authError];
            break;
        }
        case SRThirdSocialQQ:
        {
            [SRQQManager authRequestWithAuthSuccess:authSuccess authError:authError];
            break;
        }
    }
}
```

使用简单、效率高效、进程安全~~~如果你有更好的建议,希望不吝赐教!


## License 许可证
RSThirdLoginDemo 使用 MIT 许可证，详情见 LICENSE 文件。


## Contact 联系方式:
* WeChat : WhatsXie
* Email : ReverseScale@iCloud.com
* Blog : https://reversescale.github.io
