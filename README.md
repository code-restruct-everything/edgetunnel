# 🚀 edgetunnel 2.1
![后台页面](./img.png)

[![Stars](https://img.shields.io/github/stars/cmliu/edgetunnel?style=flat-square&logo=github)](https://github.com/cmliu/edgetunnel/stargazers)
[![Forks](https://img.shields.io/github/forks/cmliu/edgetunnel?style=flat-square&logo=github)](https://github.com/cmliu/edgetunnel/network/members)
[![License](https://img.shields.io/github/license/cmliu/edgetunnel?style=flat-square)](https://github.com/cmliu/edgetunnel/blob/main/LICENSE)
[![Telegram](https://img.shields.io/badge/Telegram-Group-blue?style=flat-square&logo=telegram)](https://t.me/CMLiussss)
[![YouTube](https://img.shields.io/badge/YouTube-Channel-red?style=flat-square&logo=youtube)](https://www.youtube.com/watch?v=LeT4jQUh8ok)
[![zread](https://img.shields.io/badge/Ask_Zread-_.svg?style=flat-square&color=00b0aa&labelColor=000000&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTYiIGhlaWdodD0iMTYiIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQuOTYxNTYgMS42MDAxSDIuMjQxNTZDMS44ODgxIDEuNjAwMSAxLjYwMTU2IDEuODg2NjQgMS42MDE1NiAyLjI0MDFWNC45NjAxQzEuNjAxNTYgNS4zMTM1NiAxLjg4ODEgNS42MDAxIDIuMjQxNTYgNS42MDAxSDQuOTYxNTZDNS4zMTUwMiA1LjYwMDEgNS42MDE1NiA1LjMxMzU2IDUuNjAxNTYgNC45NjAxVjIuMjQwMUM1LjYwMTU2IDEuODg2NjQgNS4zMTUwMiAxLjYwMDEgNC45NjE1NiAxLjYwMDFaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00Ljk2MTU2IDEwLjM5OTlIMi4yNDE1NkMxLjg4ODEgMTAuMzk5OSAxLjYwMTU2IDEwLjY4NjQgMS42MDE1NiAxMS4wMzk5VjEzLjc1OTlDMS42MDE1NiAxNC4xMTM0IDEuODg4MSAxNC4zOTk5IDIuMjQxNTYgMTQuMzk5OUg0Ljk2MTU2QzUuMzE1MDIgMTQuMzk5OSA1LjYwMTU2IDE0LjExMzQgNS42MDE1NiAxMy43NTk5VjExLjAzOTlDNS42MDE1NiAxMC42ODY0IDUuMzE1MDIgMTAuMzk5OSA0Ljk2MTU2IDEwLjM5OTlaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik0xMy43NTg0IDEuNjAwMUgxMS4wMzg0QzEwLjY4NSAxLjYwMDEgMTAuMzk4NCAxLjg4NjY0IDEwLjM5ODQgMi4yNDAxVjQuOTYwMUMxMC4zOTg0IDUuMzEzNTYgMTAuNjg1IDUuNjAwMSAxMS4wMzg0IDUuNjAwMUgxMy43NTg0QzE0LjExMTkgNS42MDAxIDE0LjM5ODQgNS4zMTM1NiAxNC4zOTg0IDQuOTYwMVYyLjI0MDFDMTQuMzk4NCAxLjg4NjY0IDE0LjExMTkgMS42MDAxIDEzLjc1ODQgMS42MDAxWiIgZmlsbD0iI2ZmZiIvPgo8cGF0aCBkPSJNNCAxMkwxMiA0TDQgMTJaIiBmaWxsPSIjZmZmIi8%2BCjxwYXRoIGQ9Ik00IDEyTDEyIDQiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSIxLjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPgo8L3N2Zz4K&logoColor=ffffff)](https://zread.ai/cmliu/edgetunnel)
[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/cmliu/edgetunnel)

---

## 📖 项目简介

**edgetunnel** 是一个基于 Cloudflare Workers/Pages 的边缘代理方案，提供：

- 多协议支持：VLESS、Trojan、Shadowsocks
- 可视化后台：配置管理、日志与状态查看
- 订阅生成与转换：适配 Clash、Sing-box、Surge 等客户端
- 代理增强：支持 `PROXYIP`、SOCKS5/HTTP/HTTPS 上游
- 跨平台：Windows / Android / iOS / macOS / 路由器固件

Demo: [https://EDT-Pages.github.io/admin](https://EDT-Pages.github.io/admin)

---

## 💡 快速部署

详细图文教程：<https://cmliussss.com/p/edt2/>

### 1) Workers 部署（文字版）

1. 在 Cloudflare Workers 新建 Worker。
2. 将仓库里的 [_worker.js](./_worker.js) 内容粘贴到 Worker 编辑器并部署。
3. 在 Variables 中添加环境变量 `ADMIN`（后台登录密码）。
4. 在 Bindings 中绑定 KV 命名空间，变量名写 `KV`。
5. 可选绑定自定义域名，访问 `https://你的域名/admin` 登录后台。

### 2) Pages 上传部署（推荐）

1. 下载项目 zip（或直接上传当前目录文件）到 Pages 项目。
2. 在 Pages Variables 中添加 `ADMIN`。
3. 在 Pages Bindings 中绑定 KV 命名空间，变量名 `KV`。
4. 重新部署后访问 `https://你的域名/admin`。

### 3) Pages + GitHub 部署

1. Fork 项目并连接到 Cloudflare Pages。
2. 在构建设置中添加 `ADMIN`。
3. 在 Bindings 中绑定 `KV`。
4. 完成部署后访问 `https://你的域名/admin`。

---

## 🔑 环境变量说明

| 变量 | 必填 | 示例 | 说明 |
| :--- | :---: | :--- | :--- |
| `ADMIN` | ✅ | `123456` | 后台登录密码 |
| `KEY` | ❌ | `CMLiussss` | 快速订阅路径密钥 |
| `UUID` | ❌ | `90cd4a77-141a-43c9-991b-08263cfe9c10` | 固定 UUID（需 UUIDv4） |
| `PROXYIP` | ❌ | `proxyip.cmliussss.net:443` | 全局反代 IP |
| `URL` | ❌ | `https://cloudflare-error-page-3th.pages.dev` | 主页伪装地址 |
| `GO2DIRECT` | ❌ | `youtube.com,*.youtube.com` | 命中直连，其余走上游代理 |
| `DEBUG` | ❌ | `1` 或 `true` | 开启调试日志 |
| `OFF_LOG` | ❌ | `1` 或 `true` | 关闭日志记录 |
| `BEST_SUB` | ❌ | `1` 或 `true` | 开启优选订阅生成模式 |

---

## 📌 GO2DIRECT 分流

1. 先启用上游代理（SOCKS5/HTTP/HTTPS）。
2. 再设置 `GO2DIRECT` 域名列表（逗号分隔，支持 `*` 通配符）。
3. 命中 `GO2DIRECT` 直连，未命中走上游。
4. `GO2DIRECT` 只匹配目标主机名，请勿填写 `http://`、`https://`、路径或端口。
5. 推荐写法：`主域 + 子域 + 该站常见 CDN 域名`。

基础示例：

```env
GO2DIRECT=youtube.com,*.youtube.com,netflix.com,*.netflix.com,tiktok.com,*.tiktok.com
```

常见视频网站增强模板（可直接作为 `GO2DIRECT` 值）：

```env
GO2DIRECT=youtube.com,*.youtube.com,youtu.be,*.youtu.be,googlevideo.com,*.googlevideo.com,ytimg.com,*.ytimg.com,youtube-nocookie.com,*.youtube-nocookie.com,
netflix.com,*.netflix.com,nflxvideo.net,*.nflxvideo.net,nflximg.net,*.nflximg.net,nflximg.com,*.nflximg.com,nflxext.com,*.nflxext.com,nflxso.net,*.nflxso.net,nflxsearch.net,*.nflxsearch.net,
disneyplus.com,*.disneyplus.com,disney-plus.net,*.disney-plus.net,bamgrid.com,*.bamgrid.com,
primevideo.com,*.primevideo.com,amazonvideo.com,*.amazonvideo.com,aiv-cdn.net,*.aiv-cdn.net,pv-cdn.net,*.pv-cdn.net,
hulu.com,*.hulu.com,max.com,*.max.com,hbomax.com,*.hbomax.com,tv.apple.com,*.tv.apple.com,paramountplus.com,*.paramountplus.com,peacocktv.com,*.peacocktv.com,
crunchyroll.com,*.crunchyroll.com,vrv.co,*.vrv.co,twitch.tv,*.twitch.tv,ttvnw.net,*.ttvnw.net,jtvnw.net,*.jtvnw.net,twitchcdn.net,*.twitchcdn.net,
tiktok.com,*.tiktok.com,tiktokcdn.com,*.tiktokcdn.com,tiktokv.com,*.tiktokv.com,byteoversea.com,*.byteoversea.com,ibytedtos.com,*.ibytedtos.com,
vimeo.com,*.vimeo.com,vimeocdn.com,*.vimeocdn.com,dailymotion.com,*.dailymotion.com,dailymotion-video.net,*.dailymotion-video.net,rumble.com,*.rumble.com,
bilibili.com,*.bilibili.com,bilivideo.com,*.bilivideo.com
```

如果你还想继续提高命中率，建议用下面流程补齐：

1. 临时开启 `DEBUG=1`。
2. 播放目标视频网站内容，看 Worker 日志里实际访问到的域名。
3. 把漏掉的域名按 `主域 + *.主域` 追加到 `GO2DIRECT`，重新部署即可。

---

## 🧪 代理参数路径示例

### 指定 `PROXYIP`

```url
/proxyip=proxyip.cmliussss.net
/?proxyip=proxyip.cmliussss.net
```

### 指定 `SOCKS5`

```url
/socks5=user:password@127.0.0.1:1080
/?socks5=user:password@127.0.0.1:1080
/socks5://user:password@127.0.0.1:1080
```

### 指定 `HTTP/HTTPS`

```url
/http=user:password@127.0.0.1:8080
/https=user:password@127.0.0.1:8443
/http://user:password@127.0.0.1:8080
/https://user:password@127.0.0.1:8443
```

---

## 🧭 可复现代理部署（落地 + 中转，匿名示例）

本文按可复现顺序整理：`落地 SOCKS` -> `中转链式 SOCKS` -> `systemd 常驻` -> `验证` -> `故障排查`。  
所有示例均使用占位符，不包含个人隐私信息。

### 1) 部署拓扑与目标

```text
Cloudflare Worker -> 中转机 SOCKS(1080, gost) -> 落地机 SOCKS(1080, danted) -> 目标站点
```

必要软件（建议先执行）：

```bash
sudo apt update
sudo apt install -y curl wget tar ca-certificates ufw
```

目标效果：

- 落地机看到的来源 IP 是中转机 IP（不是 Cloudflare 出口 IP）。
- 目标站点看到的出口 IP 是落地机 IP。

占位符：

- `RELAY_PUBLIC_IP`：中转机公网 IP
- `LANDING_PUBLIC_IP`：落地机公网 IP
- `RELAY_USER` / `RELAY_PASS`：中转机 SOCKS 认证

### 2) 落地机（Ubuntu/Debian）创建 SOCKS5（Dante）

```bash
sudo apt update
sudo apt install -y dante-server
```

#### 方案 A：无密码 + IP 白名单（仅允许中转机进入）

```bash
IFACE=$(ip route get 1.1.1.1 | awk '{print $5; exit}')
RELAY_IP_A="RELAY_PUBLIC_IP"
RELAY_IP_B="RELAY_PUBLIC_IP_2"   # 没有第二个可删除对应规则

sudo tee /etc/danted.conf >/dev/null <<EOF
logoutput: /var/log/danted.log
internal: 0.0.0.0 port = 1080
external: ${IFACE}

clientmethod: none
socksmethod: none

user.privileged: root
user.notprivileged: nobody

client pass {
  from: ${RELAY_IP_A}/32 to: 0.0.0.0/0
}
client pass {
  from: ${RELAY_IP_B}/32 to: 0.0.0.0/0
}
client block {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}

socks pass {
  from: ${RELAY_IP_A}/32 to: 0.0.0.0/0
}
socks pass {
  from: ${RELAY_IP_B}/32 to: 0.0.0.0/0
}
socks block {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}
EOF
```

#### 方案 B：用户名密码认证 + IP 白名单（推荐）

先创建专用代理用户（禁止 shell 登录）：

```bash
sudo useradd -M -s /usr/sbin/nologin relay_worker
sudo passwd relay_worker
```

再写 Dante 配置：

```bash
IFACE=$(ip route get 1.1.1.1 | awk '{print $5; exit}')
RELAY_IP_A="RELAY_PUBLIC_IP"
RELAY_IP_B="RELAY_PUBLIC_IP_2"   # 没有第二个可删除对应规则

sudo tee /etc/danted.conf >/dev/null <<EOF
logoutput: /var/log/danted.log
internal: 0.0.0.0 port = 1080
external: ${IFACE}

clientmethod: none
socksmethod: username

user.privileged: root
user.notprivileged: nobody

client pass {
  from: ${RELAY_IP_A}/32 to: 0.0.0.0/0
}
client pass {
  from: ${RELAY_IP_B}/32 to: 0.0.0.0/0
}
client block {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}

socks pass {
  from: ${RELAY_IP_A}/32 to: 0.0.0.0/0
}
socks pass {
  from: ${RELAY_IP_B}/32 to: 0.0.0.0/0
}
socks block {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}
EOF
```

说明：密码错误或用户名错误时，SOCKS5 认证会失败，无法建立代理连接。

#### 方案 C：任意来源 IP 可访问（公网开放）

仅建议配合用户名密码认证使用；不建议“无密码 + 任意来源”。

```bash
IFACE=$(ip route get 1.1.1.1 | awk '{print $5; exit}')

sudo tee /etc/danted.conf >/dev/null <<EOF
logoutput: /var/log/danted.log
internal: 0.0.0.0 port = 1080
external: ${IFACE}

clientmethod: none
socksmethod: username

user.privileged: root
user.notprivileged: nobody

client pass {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}
client block {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}

socks pass {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}
socks block {
  from: 0.0.0.0/0 to: 0.0.0.0/0
}
EOF
```

```bash
sudo systemctl restart danted || sudo systemctl restart sockd
sudo systemctl enable danted || sudo systemctl enable sockd
sudo systemctl status danted --no-pager || sudo systemctl status sockd --no-pager
```

方案 A/B（白名单）防火墙示例：

```bash
sudo ufw allow from RELAY_PUBLIC_IP to any port 1080 proto tcp
sudo ufw allow from RELAY_PUBLIC_IP_2 to any port 1080 proto tcp
sudo ufw deny 1080/tcp
```

方案 C（任意来源）防火墙示例：

```bash
sudo ufw allow 1080/tcp
```

### 3) 中转机创建链式 SOCKS（gost）

`apt install gost` 可能是同名不兼容程序（仅支持 `-v`，不支持 `-L/-F`），建议使用官方 `ginuerzh/gost` v2。

```bash
sudo apt remove -y gost
sudo apt purge -y gost
sudo apt autoremove -y
```

```bash
cd /tmp
wget -O gost.tar.gz https://github.com/ginuerzh/gost/releases/download/v2.12.0/gost_2.12.0_linux_amd64.tar.gz
tar -xzf gost.tar.gz
chmod +x gost
sudo mv gost /usr/local/bin/gost
/usr/local/bin/gost -V
```

```bash
/usr/local/bin/gost -L socks5://RELAY_USER:RELAY_PASS@0.0.0.0:1080 -F socks5://LANDING_PUBLIC_IP:1080
```

### 4) systemd 常驻服务（中转机）

```bash
sudo tee /etc/systemd/system/gost-relay.service >/dev/null <<'EOF'
[Unit]
Description=GOST SOCKS relay to landing SOCKS
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
ExecStart=/usr/local/bin/gost -L socks5://RELAY_USER:RELAY_PASS@0.0.0.0:1080 -F socks5://LANDING_PUBLIC_IP:1080
Restart=always
RestartSec=3
LimitNOFILE=1048576

[Install]
WantedBy=multi-user.target
EOF
```

```bash
sudo systemctl daemon-reload
sudo systemctl enable --now gost-relay
sudo systemctl restart gost-relay
sudo systemctl status gost-relay --no-pager
```

可选：同机再开一个非链式代理（2080，仅中转机直出）：

```bash
sudo tee /etc/systemd/system/gost-socks-2080.service >/dev/null <<'EOF'
[Unit]
Description=GOST standalone SOCKS5 on 2080
After=network-online.target
Wants=network-online.target

[Service]
Type=simple
ExecStart=/usr/local/bin/gost -L socks5://RELAY_USER2:RELAY_PASS2@0.0.0.0:2080
Restart=always
RestartSec=3
LimitNOFILE=1048576

[Install]
WantedBy=multi-user.target
EOF

sudo systemctl daemon-reload
sudo systemctl enable --now gost-socks-2080
```

### 5) Worker 侧填写示例

- 非全局：`socks5=RELAY_USER:RELAY_PASS@RELAY_PUBLIC_IP:1080`
- 全局：`socks5://RELAY_USER:RELAY_PASS@RELAY_PUBLIC_IP:1080`

行为说明：

- 非全局（`socks5=`）：命中直连名单时直连，未命中走上游代理（不同版本细节可能略有差异，请以当前 `_worker.js` 逻辑为准）。
- 全局（`socks5://` 或显式全局参数）：所有流量都走上游代理。

### 6) 验证命令

说明：方案 A/B 请优先在“被落地机白名单允许的中转机”上测试。若在其他来源 IP 机器上测试被拒绝，属于预期行为。方案 C 可在任意来源测试。

```bash
curl -v --socks5-hostname RELAY_USER:RELAY_PASS@127.0.0.1:1080 https://ifconfig.me
```

```bash
curl -v --socks5-hostname RELAY_USER2:RELAY_PASS2@127.0.0.1:2080 https://ifconfig.me
```

```bash
journalctl -u gost-relay -n 80 --no-pager
sudo tail -n 80 /var/log/danted.log
```

### 7) 已踩坑与修复（实战总结）

1. `flag provided but not defined: -L`  
   原因：安装了不兼容同名 `gost`。  
   修复：卸载 apt 版并安装官方 v2，使用 `/usr/local/bin/gost`。

2. `gost-relay.service` 启动失败 `status=2/INVALIDARGUMENT`  
   原因：`-L socks5://user:pass@:1080` 中 `@` 后主机为空。  
   修复：改为 `@0.0.0.0:1080`。

3. 密码含 `@` 等保留字符导致解析失败  
   修复：URL 编码（例如 `@` -> `%40`）。

4. `curl: (97) Can't complete SOCKS5 connection to ifconfig.me`  
   原因：SOCKS 服务端到目标失败（规则/防火墙/网卡）。  
   修复：重点检查 `client pass`、`socks pass`、`external` 网卡、云安全组与 UFW。

5. `needrestart` 提示重启系统服务  
   结论：系统更新常见提示，不代表 Dante/gost 配置失败。

6. `client pass` 与 `socks pass` 来源 IP 配置不一致  
   现象：连接建立但代理请求被拒绝。  
   修复：允许的中转 IP 必须同时出现在 `client pass` 和 `socks pass` 两组规则中。

7. Windows/Linux 打开 README 出现乱码  
   原因：终端或编辑器未按 UTF-8 显示，或文件被错误编码保存。  
   修复：
   - VS Code：右下角编码切换为 `UTF-8`，并将默认编码设置为 `utf8`。
   - Windows PowerShell 显示乱码时先执行：`chcp 65001`，再执行 `$OutputEncoding = [Console]::OutputEncoding = [Text.Encoding]::UTF8`。
   - 若文件已被错误编码保存，优先从 Git 恢复正确版本后再以 UTF-8 保存。
   - 本仓库建议保留 `.editorconfig` 的 `charset = utf-8` 与 `.gitattributes` 的换行规则，避免跨平台再次出现编码/换行混乱。

---

## 🧩 客户端适配

| 平台 | 推荐客户端 |
| :--- | :--- |
| Windows | v2rayN / FlClash / Clash Verge Rev / mihomo-party |
| Android | ClashMetaForAndroid / FlClash / v2rayNG |
| iOS | Surge / Shadowrocket / Stash |
| macOS | FlClash / Clash Verge Rev / Surge / mihomo-party |

---

## ⚠️ 免责声明

1. 本项目仅用于教育、研究和合法的安全测试用途。  
2. 使用者需遵守所在地区法律法规。  
3. 项目作者及贡献者不对任何滥用行为及其后果负责。  
4. 建议在测试完成后及时清理不再使用的部署资源。  
