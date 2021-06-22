# 我的Surge 4配置

copy from [DivineEngine/Profiles](https://github.com/DivineEngine/Profiles)

没搞定vmess协议，还是需要先转换为订阅地址。


现在仓库配合Github Actions，可以输出替换后的配置。在`Settings-Secrets`中设置`SUB_URL1`，`SUB_URL2`  
可以全部设置相同的值，也可以根据个人情况设置为多个值。

```
[Proxy]
🌐Direct = direct
⛔️Reject = reject


[Proxy Group]
🧭Final = select, 🌑Proxy, 🌐Direct
🌑Proxy = select, 🧯Fallback, 🕹AutoTest
🎞Streaming = select, 🌑Proxy, 🕹AutoTest
🎞StreamingSE = select, 🌐Direct
🛡Guard = select, ⛔️Reject, 🌐Direct
🧯Fallback = fallback, policy-path=YOUR_SUB_URL1, url=http://www.gstatic.com/generate_204, interval=600, tolerance=50
🕹AutoTest = url-test, policy-path=YOUR_SUB_URL2, url=http://www.gstatic.com/generate_204, interval=600, tolerance=50
```


## 安装模块
- Modules/cron.sgmodule
- Modules/cookie.sgmodule
- [nzw9314/Script_ALL_in_one](https://raw.githubusercontent.com/nzw9314/Surge/master/Module/Script_All_in_one.sgmodule)


## 免责声明：
- ilaipi发布的Script项目中涉及的任何解锁和解密分析脚本仅用于资源共享和学习研究，不能保证其合法性，准确性，完整性和有效性，请根据情况自行判断.

- 间接使用脚本的任何用户，包括但不限于建立VPS或在某些行为违反国家/地区法律或相关法规的情况下进行传播, ilaipi 对于由此引起的任何隐私泄漏或其他后果概不负责.

- 请勿将Script项目的任何内容用于商业或非法目的，否则后果自负.

- 如果任何单位或个人认为该项目的脚本可能涉嫌侵犯其权利，则应及时通知并提供身份证明，所有权证明，我将在收到认证文件后删除相关脚本.

- ilaipi 对任何脚本问题概不负责，包括但不限于由任何脚本错误导致的任何损失或损害.

- 您必须在下载后的24小时内从计算机或手机中完全删除以上内容.

- 任何以任何方式查看此项目的人或直接或间接使用该Script项目的任何脚本的使用者都应仔细阅读此声明。ilaipi 保留随时更改或补充此免责声明的权利。一旦使用并复制了任何相关脚本或Script项目的规则，则视为您已接受此免责声明.

## 订阅地址转换

[id9](https://id9.cc/)

把自己协议的订阅地址，输入进去转换后，替换surge4.conf中“订阅地址”4个字（出现了几遍，最好都替换一下）。

转换的时候，可能需要勾选“输出为 Node List”
