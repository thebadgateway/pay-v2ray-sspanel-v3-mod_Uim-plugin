```
// TCP example
domain;non-zero;2;tcp

// TCP + TLS example
domain;non-zero;2;tcp;tls

// WS
domain;8080;2;ws;;path=/v2ray|host=You can use the domain name with CDN added here.

// WS + CDN
domain;8080;2;ws;;path = / v2ray | server = here with the domain name added CDN | host = here with the domain name added CDN

// WS + TLS (automatic configuration)
domain;non-zero;2;tls;ws;path=/v2ray|host=non-CDN and TLS domain name|inside_port=10550


// WS + TLS (automatic configuration) + CDN
domain;non-zero;2;tls;ws;path = / v2ray | host = here with the domain name added CDN | inside_port = 10550 | server = here with the domain name plus CDN

// WS + TLS (provided by Caddy)
domain;0;2;tls;ws;path=/v2ray|host=non-CDN and TLS domain name|inside_port=10550|outside_port=443

// WS + TLS (provided by Caddy) + CDN
domain;0;2;tls;ws;path = / v2ray | host = here with the domain name added CDN | inside_port = 10550 | outside_port = 443 | server = here with the domain name plus CDN


// nat🐔 ws
domain;non-zero;2;ws;;path=/v2ray|host=You can use the domain name with CDN added here.

// nat🐔 ws + tls (automatic configuration), because some merchants do not provide 80 & 443 access, so please consider manually requesting an SSL certificate
domain;non-zero;2;tls;ws;path = / v2ray | host = tls domain name


// nat🐔 ws + tls (automatic configuration) + CDN, because some merchants do not provide 80 & 443 access, so please consider manually applying for SSL certificate
domain;non-zero;2;tls;ws;path = / v2ray | host = here with the domain name added CDN | server = here with the domain name plus CDN


// nat🐔 ws + tls (provided by Caddy), as some merchants do not provide 80 & 443 access, so please consider manually requesting an SSL certificate.
domain;0;2;tls;ws;path=/v2ray|host=tls domain name|inside_port=10550|outside_port=11120



// nat🐔 ws + tls (provided by Caddy) + CDN, because some merchants do not provide 80 & 443 access, so please consider applying for SSL certificate manually.
domain;0;2;tls;ws;path = / v2ray | host = here with the domain name added CDN | inside_port = 10550 | outside_port = 11120 | server = here with the domain name added CDN


// The following is a KCP sample section that supports all V2Ray types:

// none: The default value, no masquerading, the data sent is a packet with no features.
domain;non-zero;2;kcp;noop

// srtp: Disguised as an SRTP packet, it is recognized as video call data (such as FaceTime).
domain;non-zero;2;kcp;srtp

// utp: Disguised as a uTP packet, it will be recognized as BT download data.
domain;non-zero;2;kcp;utp

// wechat-video: A packet masquerading as a WeChat video call.
domain;non-zero;2;kcp;wechat-video

// dtls: Disguised as a DTLS 1.2 packet.
domain;non-zero;2;kcp;dtls

// wireguard: Disguised as a WireGuard packet (not a true WireGuard protocol).
domain;non-zero;2;kcp;wireguard
```
