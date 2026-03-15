Anyconnect VPN 一键安装管理脚本  原始来自ToyoDAdoubiBackup，由于版本太低，所以在此基础上添加了ocserv最新版本选择。
安装链接：sudo wget -N --no-check-certificate https://raw.githubusercontent.com/jscat01/maxdo/master/anyconnect/ocserv.sh && chmod +x ocserv.sh && bash ocserv.sh


可能会提示 ocser.sh无权限运行,手动添加权限。
sudo chmod +x ocserv.sh

lab@labopenclaw:~$ sudo ./ocserv.sh
[sudo] password for lab: 

 ocserv 一键安装管理脚本 [v1.1.2]
  -- Jscat01 | github.com/jscat01/maxdo --
  
 0. 升级脚本
————————————
 1. 安装 ocserv
 2. 卸载 ocserv
————————————
 3. 启动 ocserv
 4. 停止 ocserv
 5. 重启 ocserv
————————————
 6. 设置 账号配置
 7. 查看 配置信息
 8. 修改 配置文件
 9. 查看 日志信息
————————————

 当前状态: 已安装 并 已启动

 请输入数字 [0-9]:


 [信息] 自动获取 ocserv 最新版本号（核心功能)...
 正在获取 ocserv 最新版本号...
 检测到官网最新稳定版：1.4.1

 请选择要安装的 ocserv 版本：
  1) 使用最新版：1.4.1（推荐）
  2) 使用自定义版本（手动输入，如 0.11.8）
  3) 使用备用稳定版：1.3.0
  请输入选择（1/2/3，默认1）：

最后添加正面的防火墙策略，实现代理上网。
iptables -t nat -I POSTROUTING -s 192.168.1.0/24 -j MASQUERADE

