<div align="center">
  <br>
  <img width="360" style="max-width:80%" src="resource/static/brand.svg" title="哪吒监控 Nezha Monitoring">
  <br>
  <small><i>LOGO not designed by me .</i></small>
  <br><br>
<img src="https://img.shields.io/github/actions/workflow/status/naiba/nezha/dashboard.yml?branch=master&label=Dash%20v0.15.1&logo=github&style=for-the-badge">&nbsp;<img src="https://img.shields.io/github/v/release/nezhahq/agent?color=brightgreen&label=Agent&style=for-the-badge&logo=github">&nbsp;<img src="https://img.shields.io/github/actions/workflow/status/nezhahq/agent/agent.yml?branch=v0.15.4&label=Agent%20CI&logo=github&style=for-the-badge">&nbsp;<img src="https://img.shields.io/badge/Installer-v0.15.0-brightgreen?style=for-the-badge&logo=linux">
  <br>
  <br>
  <p>:trollface: <b>Nezha Monitoring: Self-hostable, lightweight, servers and websites monitoring and O&M tool.</b></p>
  <p>Supports <b>monitoring</b> system status, HTTP (SSL certificate change, upcoming expiration, expired), TCP, Ping and supports <b>push alerts</b>, run scheduled tasks and <b>web terminal</b>.</p>
</div>

\>> Telegram Group: [Nezha Monitoring Global (English Only)](https://t.me/nezhamonitoring_global), [哪吒监控（中文群组）](https://t.me/nezhamonitoring)

\>> [Use Cases | 我们的用户](https://www.google.com/search?q=%22powered+by+Nezha+Monitoring%22+OR+%22powered+by+%E5%93%AA%E5%90%92%E7%9B%91%E6%8E%A7%22) (Google)  



## User Guide
获取 Github/Jihulab 的 Client ID 和密钥
哪吒监控接入 Github、Gitlab、Jihulab、Gitee 作为后台管理员账号

首先我们需要新建一个验证应用，以 Github 为例，登录 Github 后，打开 https://github.com/settings/developers ，依次选择“OAuth Apps” - “New OAuth App”
Application name - 随意填写
Homepage URL - 填写面板的访问域名，如："http://cdn.example.com"
Authorization callback URL - 填写回调地址，如："http://cdn.example.com/oauth2/callback"
点击 “Register application”
保存页面中的 Client ID，然后点击 “Generate a new client secret“，创建一个新的 Client Secret，新建的密钥仅会显示一次，请妥善保存

JihuLab 的应用创建入口为：https://jihulab.com/-/profile/applications
Redirect URL 中应填入回调地址
在下方范围中勾选 read_user 和 read_api
创建完成后，保存好应用程序 ID 和密码
在服务器中安装 Dashboard
在面板服务器中，运行安装脚本：
bash
curl -L https://raw.githubusercontent.com/lobbiaa/nezha/master/script/install.sh  -o nezha.sh && chmod +x nezha.sh && sudo ./nezha.sh

等待Docker安装完毕后，分别输入以下值：
OAuth提供商 - Github，Gitlab，Jihulab，Gitee 中选择一个
Client ID - 之前保存的 Client ID
Client Secret - 之前保存的密钥
用户名 - OAuth 提供商中的用户名
站点标题 - 自定义站点标题
访问端口 - 公开访问端口，可自定义，默认 8008
Agent的通信端口 - Agent与Dashboard的通信端口，默认 5555

输入完成后，等待拉取镜像
安装结束后，如果一切正常，此时你可以访问域名+端口号，如 “http://cdn.example.com:8008” 来查看面板

将来如果需要再次运行脚本，可以运行：

bash
./nezha.sh
来打开管理脚本

- [English](https://nezhahq.github.io/en_US/index.html)
- [中文文档](https://nezhahq.github.io/index.html)

## Screenshots

| Default Theme                                                                                 | DayNight [@JackieSung](https://github.com/JackieSung4ev)                                               | hotaru                                                                     |
| ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| ![Default Theme](resource/template/theme-default/screenshot.png)                              | <img src="resource/template/theme-daynight/screenshot.png" width="3000px"/>                            | <img src="resource/template/theme-hotaru/screenshot.png" width="1500px" /> |
| <div align="center"><b>Default modified <a href="https://ww.ws/43.html">[Guide]</a></b></div> | <div align="center"><b>Neko Mdui <a href="https://github.com/MikoyChinese">@MikoyChinese</a></b></div> |      <div align="center"><b>AngelKanade <a href="https://github.com/adminsama">@adminsama</a></b></div>         |
| ![默认主题魔改](https://fastly.jsdelivr.net/gh/idarku/img@main/me/1631120192341.webp)       | ![Neko Mdui](resource/template/theme-mdui/screenshot.png)                                              |        ![AngelKanade](resource/template/theme-angel-kanade/screenshot.png)            |

