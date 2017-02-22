# ssr-fs-svr-alpine
ssr-fs-svr-alpine
# usage
docker run -d -p 150:150/udp -p 8765:8765 -p 8766:8766 arctg70/ssr-fs-svr-alpine
# config.json
{
    "server":"0.0.0.0",
    "server_ipv6":"::",
    "local_address":"127.0.0.1",
    "local_port":1080,
    "port_password":{
        "8765":{"protocol":"origin", "password":"windyboy", "obfs":"http_simple_compatible", "obfs_param":""},
        "8766":{"protocol":"auth_aes128_md5", "password":"windyboy"}
    },
    "timeout":300,
    "method":"chacha20",
    "protocol": "auth_aes128_md5",
    "protocol_param": "",
    "obfs": "http_simple",
    "obfs_param": "",
    "redirect": "",
    "dns_ipv6": false,
    "fast_open": true,
    "workers": 1
}
