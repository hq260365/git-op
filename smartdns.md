# SmartDns设置
- - -
ssh到openwrt修改/etc/conffig/smartdns
_ _ _

    config smartdns
        option server_name 'smartdns'
        option prefetch_domain '1'
        option serve_expired '1'
        option coredump '0'
        option port '6053'
        option ipv6_server '0'
        option seconddns_port '5335'
        option seconddns_no_rule_addr '0'
        option seconddns_no_rule_nameserver '0'
        option seconddns_no_rule_ipset '0'
        option seconddns_no_rule_soa '0'
        option cache_size '20000'
        option enabled '1'
        option tcp_server '1'
        option dualstack_ip_selection '0'
        option redirect 'none'
        option seconddns_tcp_server '1'
        option seconddns_server_group 'us'
        option seconddns_no_speed_check '1'
        option seconddns_no_cache '1'
        option force_aaaa_soa '1'
        option seconddns_no_dualstack_selection '1'
        option rr_ttl_min '1800'
        option rr_ttl_max '86400'
        option seconddns_enabled '1'
        list old_redirect 'none'
        list old_port '6053'
        list old_enabled '1'

    config server
        option name '360'
        option type 'https'
        option ip 'doh.360.cn/dns-query'
        option server_group 'cn'
        option blacklist_ip '0'
        option spki_pin '/GZlA5nnRbCZE7Rr/U829+XnthuLLsQLA3HlcjSUQI8='
        option enabled '1'

    config server
        option name 'alidns'
        option type 'https'
        option ip 'dns.alidns.com/dns-query'
        option server_group 'cn'
        option blacklist_ip '0'
        option spki_pin 'ZwR21gnCMTzsM6VWtnb/azufgYegWWuhE9reP5tamWU='
        option enabled '1'

    config server
        option type 'https'
        option ip 'doh.pub/dns-query'
        option server_group 'cn'
        option blacklist_ip '0'
        option spki_pin '47DEQpj8HBSa+/TImW+5JCeuQeRkm5NMpJWZG3hSuFU='
        option enabled '1'
        option name '腾讯'

    config server
        option name 'cloudflare'
        option blacklist_ip '0'
        option spki_pin 'RKlx+/Jwn2A+dVoU8gQWeRN2+2JxXcFkAczKfgU8OAI='
        option type 'https'
        option ip 'cloudflare-dns.com/dns-query'
        option no_check_certificate '0'
        option server_group 'us'
        option enabled '1'

    config server
        option name 'google'
        option server_group 'us'
        option blacklist_ip '0'
        option spki_pin 'E0cSH4eMqOSf+8hwnp/q7Nrn/CbvK0PL6PWpKiv5alU='
        option ip 'dns.google/dns-query'
        option type 'https'
        option enabled '1'

    config server
        option ip 'dns.pub/dns-query'
        option type 'https'
        option enabled '1'
        option name '腾讯'
        option blacklist_ip '0'
        option spki_pin 'Q1JRqG379NbZYD6KcA+jl8co9wuQNhg/YmN4dLImQpM='
        option server_group 'cn'

    config server
        option ip '1.12.12.12/dns-query'
        option type 'https'
        option enabled '1'
        option name '腾讯'
        option blacklist_ip '0'
        option spki_pin 'U4NYL6C7pQ+cfN2VlEaIgHTHGVOKxbLBISdo3512Taw='
        option server_group 'cn'

    config server
        option ip '120.53.53.53/dns-query'
        option type 'https'
        option enabled '1'
        option name '腾讯'
        option blacklist_ip '0'
        option spki_pin '9liKx1b0W78tpaZMYTSUjaLXZZMc3/Ce5spOoWBlMJA='
        option server_group 'cn'


* * *

- - -
修改/etc/smartdns／address.conf
_ _ _

    address /dns.alidns.com/223.5.5.5
    address /doh.pub/119.29.29.29
    address /sm2.doh.pub/119.29.29.29
    address /dns.pub/162.14.21.56
    address /dns.pub/162.14.21.178
    address /doh.360.cn/101.226.4.6
    address /cloudflare-dns.com/1.1.1.1
    address /dns.google/8.8.8.8




