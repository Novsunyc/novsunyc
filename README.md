[custom]
;不要随意改变关键字，否则会导致出错
;acl4SSR规则

;去广告：支持
;自动测速：支持
;微软分流：支持
;苹果分流：支持
;增强中国IP段：支持
;增强国外GFW：支持

;设置规则标志位
ruleset=🛑 广告拦截,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/Advertising/Advertising.list
ruleset=🎰 Binance,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/Binance/Binance.list
ruleset=🛢 YuTube,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/YouTube/YouTube.list
ruleset=🎸 Spotify,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/Spotify/Spotify.list
ruleset=📱 Telegram,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/Telegram/Telegram.list
ruleset=🗽 国外手动,[]DOMAIN-SUFFIX,googleapis.cn
ruleset=🗽 国外手动,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/Global/Global.list
ruleset=🍁 国内手动,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/China/China.list
ruleset=🍁 国内手动,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Clash/ChinaMax/ChinaMax.list
ruleset=🐟 漏网之鱼,[]FINAL
;设置分组标志位
custom_proxy_group= 🎰 Binance`select`[]🇸🇬 Singapore`[]🇹🇼 Taiwan`[]🇰🇷 South Korea`[]🇺🇸 America`[]🇯🇵 Japan`[]🇭🇰 Hong Kong
custom_proxy_group=🛢 YuTube`select`[]🇸🇬 Singapore`[]🇹🇼 Taiwan`[]🇰🇷 South Korea`[]🇺🇸 America`[]🇯🇵 Japan`[]🇭🇰 Hong Kong
custom_proxy_group=🎸 Spotify`select`[]🇸🇬 Singapore`[]🇹🇼 Taiwan`[]🇰🇷 South Korea`[]🇺🇸 America`[]🇯🇵 Japan`[]🇭🇰 Hong Kong
custom_proxy_group=🌎 Google`select`[]🇸🇬 Singapore`[]🇹🇼 Taiwan`[]🇰🇷 South Korea`[]🇺🇸 America`[]🇯🇵 Japan`[]🇭🇰 Hong Kong
custom_proxy_group=📱 Telegram`select`[]🇸🇬 Singapore`[]🇹🇼 Taiwan`[]🇰🇷 South Korea`[]🇺🇸 America`[]🇯🇵 Japan`[]🇭🇰 Hong Kong
custom_proxy_group= 🍁 国内手动`select`[]⚡ 国内自动`[]⚡ 国外自动`[]DIRECT
custom_proxy_group=🗽 国外手动`select`[]⚡ 国外自动`[]🇸🇬 Singapore`[]DIRECT
custom_proxy_group=⚡ 国内自动`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:江苏|湖北|广西|广东|福建|重庆|扬州|海南|长沙|贵州|济南|沈阳|成都|武汉|昆明|联通|移动|电信|BGP|广州|湖南|镇江|温州|四川|安徽|宿迁|河南)).*$)`http://connect.rom.miui.com/generate_204`300,50
custom_proxy_group=⚡ 国外自动`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:香港|新加坡|日本|东京|美国|韩国|首尔|台湾|隧道|德国|荷兰|土耳其|阿根廷|加拿大|狮城|南朝鲜|SG|JP|KR|HK|TW|叙利亚|英国)).*$)`http://www.gstatic.com/generate_204`300,50
custom_proxy_group=🐟 漏网之鱼`select`[]🗽 国外手动`[]🍁 国内手动`[]DIRECT
custom_proxy_group=🛑 广告拦截`select`[]REJECT`[]DIRECT
custom_proxy_group= 🇺🇸 America`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:美|美国|波特兰|达拉斯|俄勒冈|凤凰城|费利蒙|硅谷|拉斯维加斯|洛杉矶|圣何塞|圣克拉拉|西雅图|芝加哥|United States)).*$)`http://www.gstatic.com/generate_204`300,50
custom_proxy_group=🇸🇬 Singapore`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:新加坡|坡|狮城|SG|Singapore)).*$)`http://www.gstatic.com/generate_204`300,50
custom_proxy_group=🇯🇵 Japan`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:日本|川日|东京|大阪|泉日|埼玉|沪日|深日|JP|Japan)).*$)`http://www.gstatic.com/generate_204`300,100
custom_proxy_group=🇭🇰 Hong Kong`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:港|香港|HongKong|HK|Hong Kong)).*$)`http://www.gstatic.com/generate_204`300,50
custom_proxy_group=🇹🇼 Taiwan`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:台|新北|彰化|TW|Taiwan)).*$)`http://www.gstatic.com/generate_204`300,50
custom_proxy_group=🇰🇷 South Korea`url-test`(^(?!.*x(?:[2-9]|[1-9][0-9]))(?=.*(?:KR|Korea|KOR|首尔|韩|韓))`http://www.gstatic.com/generate_204`300,50

;设置分组标志位

enable_rule_generator=true
overwrite_original_rules=true
skip_failed_links=true

#过滤节点，正则匹配
exclude_remarks=(IPV6|重置|流量|用户|本站|漏洞|永久虚通路|车|邀|免翻|邀请|eevpn|域名|机场|刷新|禁止|备用登录|计划|面板|忘记|到期|套餐|官网|更多|关注|25倍率|http|增加|持续|渠道|购买|QQ|Ins|二手)

;luck
