# scripts

下列脚本只用于授权渗透测试或安全自测，勿用于非法攻击


ssh-public-key_login_scan
用途：Linux服务器免密登录扫描
用法：
    bash ssh-public-key_login_scan # 根据实际情况不同耗时几秒到几分钟不等
注意事项：
    timeout 7s ssh -oStrictHostKeyChecking=no `whoami`@$i pwd > /dev/null 2&>1 && echo $i >> success.list
    经测试，超时时间为7秒为最佳，当时间设置较短时，有一些免密登录的服务器并不能被发现
    如用于内网机器，可适当调整超时时间，加快脚本执行速度
输出：
    root@tencent-hk-3M3Y:~# cat success.list
    111.231.138.xxx
    165.227.108.xxx
    192.99.2.xxx
    23.95.230.xxx
    69.12.89.xxx
    91.121.88.xxx
    xxx.pub
    xxx.win
    list.xxx.win
    s1.xxx.win
    vi4.t.xxx.win

