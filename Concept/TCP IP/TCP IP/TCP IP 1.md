# TCP/IP 寻址

Created: Feb 23, 2020 3:00 PM

---

TCP/IP 使用 32 个比特或者 4 组 0 到 255 之间的数字来为计算机编址。

---

## IP地址

每个计算机必须有一个 IP 地址才能够连入因特网。

每个 IP 包必须有一个地址才能够发送到另一台计算机。

在本教程下一节，您会学习到更多关于 IP 地址和 IP 名称的知识。

---

## IP 地址包含 4 组数字：

TCP/IP 使用 4 组数字来为计算机编址。每个计算机必须有一个唯一的 4 组数字的地址。

每组数字必须在 0 到 255 之间，并由点号隔开，比如：192.168.1.60。

---

## 32 比特 = 4 字节

TCP/IP 使用 32 个比特来编址。一个计算机字节是 8 比特。所以 TCP/IP 使用了 4 个字节。

一个计算机字节可以包含 256 个不同的值：

00000000、00000001、00000010、00000011、00000100、00000101、00000110、00000111、00001000 ....... 直到 11111111。

现在，您应该知道了为什么 TCP/IP 地址是介于 0 到 255 之间的 4 组数字。

---

## IP V6

IPv6 是 "Internet Protocol Version 6" 的缩写，也被称作下一代互联网协议，它是由 IETF 小组（Internet 工程任务组Internet Engineering Task Force）设计的用来替代现行的 IPv4（现行的）协议的一种新的 IP 协议。

我们知道，Internet 的主机都有一个唯一的 IP 地址，IP 地址用一个 32 位二进制的数表示一个主机号码，但 32 位地址资源有限，已经不能满足用户的需求了，因此 Internet 研究组织发布新的主机标识方法，即 IPv6。

在 RFC1884 中（RFC 是 Request for Comments document 的缩写。RFC 实际上就是 Internet 有关服务的一些标准），规定的标准语法建议把 IPv6 地址的 128 位（16 个字节）写成 8 个 16 位的无符号整数，每个整数用 4 个十六进制位表示，这些数之间用冒号（:）分开，例如：

    686E：8C64：FFFF：FFFF：0：1180：96A：FFFF

冒号十六进制记法允许零压缩，即一串连续的0可以用一对冒号取代，例如：

    FF05：0：0：0：0：0：0：B3可以定成：FF05：：B3

为了保证零压缩有一个清晰的解释，建议中规定，在任一地址中，只能使用一次零压缩。该技术对已建议的分配策略特别有用，因为会有许多地址包含连续的零串。

冒号十六进制记法结合有点十进制记法的后缀。这种结合在IPv4向IPv6换阶段特别有用。例如，下面的串是一个合法的冒号十六进制记法：

    0：0：0：0：0：0：128.10.1.1

这种记法中，虽然冒号所分隔的每一个值是一个16位的量，但每个分点十进制部分的值则指明一个字节的值。再使用零压缩即可得出：

    ：：128.10.1.1

---

## 域名

12 个阿拉伯数字很难记忆。使用一个名称更容易。

用于 TCP/IP 地址的名字被称为域名。runoob.com 就是一个域名。

当你键入一个像 http://www.runoob.com 这样的域名，域名会被一种 DNS 程序翻译为数字。

在全世界，数量庞大的 DNS 服务器被连入因特网。DNS 服务器负责将域名翻译为 TCP/IP 地址，同时负责使用新的域名信息更新彼此的系统。

当一个新的域名连同其 TCP/IP 地址一起注册后，全世界的 DNS 服务器都会对此信息进行更新。