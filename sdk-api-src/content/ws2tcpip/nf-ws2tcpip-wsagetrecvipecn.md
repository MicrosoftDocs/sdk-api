---
UID: NF:ws2tcpip.WSAGetRecvIPEcn
title: WSAGetRecvIPEcn
description: TBD (WSAGetRecvIPEcn)
ms.date: 11/13/2020
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2tcpip.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ws2tcpip.h
api_name:
 - WSAGetRecvIPEcn
f1_keywords:
 - WSAGetRecvIPEcn
 - ws2tcpip/WSAGetRecvIPEcn
dev_langs:
 - c++
---

## -description

Queries the current enablement of receiving the **IP_ECN** (or **IPV6_ECN**) control message via [LPFN_WSARECVMSG (WSARecvMsg)](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg). See [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) for more info.

For more info, and code examples, see [Winsock explicit congestion notification (ECN)](/windows/win32/winsock/winsock-ecn).

## -parameters

### -param Socket

Type: \_In\_ **SOCKET**

A descriptor that identifies the socket.

### -param Enabled

Type: \_Out\_ **[DWORD](/windows/win32/winprog/windows-data-types)\***

**TRUE** if the receipt of ECN codepoints is enabled; otherwise, **FALSE**.

## -returns

If the function succeeds, then the return value is 0. Otherwise, a value of **SOCKET_ERROR** is returned, and you can retreive a specific error code by calling 
[WSAGetLastError](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

## -remarks

> [!IMPORTANT]
> This API is deprecated. **WSAGetRecvIPEcn** does not properly support dual-stack sockets. Use the [**IP_ECN**](/windows/win32/winsock/ipproto-ip-socket-options) and [**IPV6_ECN**](/windows/win32/winsock/ipproto-ipv6-socket-options) socket options directly with [getsockopt](../winsock/nf-winsock-getsockopt.md) instead.

On a dual-stack socket, applications need to get both the **IP_ECN** (level **IPPROTO_IP**) and **IPV6_ECN** (level **IPPROTO_IPV6**) socket options separately, unless the socket is currently bound to an IPv4-mapped IPv6 address (for example, `::ffff:192.0.2.1`), in which case only the **IP_ECN** option applies.

## -see-also

* [Winsock explicit congestion notification (ECN)](/windows/win32/winsock/winsock-ecn)
* [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
