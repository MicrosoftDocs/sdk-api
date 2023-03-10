---
UID: NS:ws2ipdef.in_pktinfo
title: IN_PKTINFO (ws2ipdef.h)
description: The in_pktinfo structure is used to store received packet address information, and is used by Windows to return information about received packets and also allows specifying the local IPv4 address to use for sending packets.
helpviewer_keywords: ["*PIN_PKTINFO","IN_PKTINFO","IN_PKTINFO structure [Winsock]","PIN_PKTINFO","PIN_PKTINFO structure pointer [Winsock]","_win32_in_pktinfo_2","in_pktinfo","in_pktinfo structure [Winsock]","winsock.in_pktinfo_2","ws2ipdef/PIN_PKTINFO","ws2ipdef/in_pktinfo","ws2tcpip/PIN_PKTINFO","ws2tcpip/in_pktinfo"]
old-location: winsock\in_pktinfo_2.htm
tech.root: WinSock
ms.assetid: a20cb3ff-38fb-471d-b940-7265c114e209
ms.date: 12/05/2018
ms.keywords: '*PIN_PKTINFO, IN_PKTINFO, IN_PKTINFO structure [Winsock], PIN_PKTINFO, PIN_PKTINFO structure pointer [Winsock], _win32_in_pktinfo_2, in_pktinfo, in_pktinfo structure [Winsock], winsock.in_pktinfo_2, ws2ipdef/PIN_PKTINFO, ws2ipdef/in_pktinfo, ws2tcpip/PIN_PKTINFO, ws2tcpip/in_pktinfo'
req.header: ws2ipdef.h
req.include-header: Ws2tcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IN_PKTINFO, *PIN_PKTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - in_pktinfo
 - ws2ipdef/in_pktinfo
 - PIN_PKTINFO
 - ws2ipdef/PIN_PKTINFO
 - IN_PKTINFO
 - ws2ipdef/IN_PKTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
 - Ws2tcpip.h
api_name:
 - IN_PKTINFO
---

# IN_PKTINFO structure


## -description

The 
<b>in_pktinfo</b> structure is used to store received packet address information, and is used by Windows to return information about received packets and also allows specifying the local IPv4 address to use for sending packets.

## -struct-fields

### -field ipi_addr

The destination IPv4 address from the IP header of the received packet when used with the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a> function. The local source IPv4 address to set in the IP header when used with the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a> function.

### -field ipi_ifindex

The interface on which the packet was received when used with the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a> function. The interface on which the packet should be sent  when used with the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a> function.

## -remarks

If the <a href="/windows/desktop/WinSock/ip-pktinfo">IP_PKTINFO</a> socket option is set on a socket of type <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>, one of the control data objects returned by the <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a> function will contain an 
<b>in_pktinfo</b> structure used to store received packet address information.

On an IPv4  socket of type  <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>, an application can specific  the local IP address to use for sending with the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a> function. One of the control data objects passed in the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure to the <b>WSASendMsg</b> function may contain an 
<b>in_pktinfo</b> structure used to specify the local IPv4 address to use for sending.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>in_pktinfo</b> structure is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The  <i>Ws2ipdef.h</i>  header files should never be used directly.

## -see-also

<a href="/windows/desktop/WinSock/dual-stack-sockets">Dual-Stack Sockets for IPv6 Winsock Applications</a>



<a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IPPROTO_IP Socket Options</a>



<a href="/windows/desktop/WinSock/ipv6-pktinfo">IPV6_PKTINFO</a>



<a href="/windows/desktop/WinSock/ip-pktinfo">IP_PKTINFO</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-in6_pktinfo">in6_pktinfo</a>