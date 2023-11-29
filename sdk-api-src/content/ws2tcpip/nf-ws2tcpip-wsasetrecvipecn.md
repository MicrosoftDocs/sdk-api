---
UID: NF:ws2tcpip.WSASetRecvIPEcn
title: WSASetRecvIPEcn
description: Specifies whether the IP stack should populate the control buffer with a message containing the explicit congestion notification (ECN) codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.
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
 - WSASetRecvIPEcn
f1_keywords:
 - WSASetRecvIPEcn
 - ws2tcpip/WSASetRecvIPEcn
dev_langs:
 - c++
---

## -description

Specifies whether the IP stack should populate the control buffer with a message containing the explicit congestion notification (ECN) codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.

When you enable the receipt of ECN codepoints, the [LPFN_WSARECVMSG (WSARecvMsg)](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns optional control data containing the ECN codepoint of the received datagram. The returned control message type will be **IP_ECN** (or **IPV6_ECN**) with level **IPPROTO_IP** (or **IPPROTO_IPV6**). The control message data is returned as an **INT**. This option is valid only on datagram sockets (the socket type must be **SOCK_DGRAM**).

For more info, and code examples, see [Winsock explicit congestion notification (ECN)](/windows/win32/winsock/winsock-ecn). Also see [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn).

## -parameters

### -param Socket

Type: \_In\_ **SOCKET**

A descriptor that identifies the socket.

### -param Enabled

Type: \_In\_ **[DWORD](/windows/win32/winprog/windows-data-types)**

**TRUE** to enable the receipt of ECN codepoints; **FALSE** to disable.

## -returns

If the function succeeds, then the return value is 0. Otherwise, a value of **SOCKET_ERROR** is returned, and you can retreive a specific error code by calling 
[WSAGetLastError](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

## -remarks

## -see-also

* [Winsock explicit congestion notification (ECN)](/windows/win32/winsock/winsock-ecn)
* [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
