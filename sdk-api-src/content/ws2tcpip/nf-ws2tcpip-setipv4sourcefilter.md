---
UID: NF:ws2tcpip.setipv4sourcefilter
title: setipv4sourcefilter function (ws2tcpip.h)
description: Sets the multicast filter state for an IPv4 socket.
helpviewer_keywords: ["setipv4sourcefilter","setipv4sourcefilter function [Winsock]","winsock.setipv4sourcefilter","ws2tcpip/setipv4sourcefilter"]
old-location: winsock\setipv4sourcefilter.htm
tech.root: WinSock
ms.assetid: C296D050-9195-42B5-8EBE-C6004F2DA855
ms.date: 12/05/2018
ms.keywords: setipv4sourcefilter, setipv4sourcefilter function [Winsock], winsock.setipv4sourcefilter, ws2tcpip/setipv4sourcefilter
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - setipv4sourcefilter
 - ws2tcpip/setipv4sourcefilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - setipv4sourcefilter
---

# setipv4sourcefilter function


## -description

The 
<b>setipv4sourcefilter</b> inline function  sets the multicast filter state for an IPv4  socket.

## -parameters

### -param Socket [in]

A descriptor that identifies a multicast socket.

### -param Interface [in]

The local IPv4 address of the interface or the interface index on which the multicast group should be joined or dropped. 

This value is in network byte order. If this member specifies an IPv4 address of 0.0.0.0, the default IPv4 multicast interface is used.

Any IP address in the 0.x.x.x block (first octet of 0) except IPv4 address 0.0.0.0 is treated as an interface index. An interface index is a 24-bit number, and the 0.0.0.0/8 IPv4 address block is not used (this range is reserved). 

To use an interface index of 1 would be the same as an IP address of 0.0.0.1.

### -param Group [in]

The IPv4 address of the multicast group.

### -param FilterMode [in]

The multicast filter mode for multicast group address.

### -param SourceCount [in]

The number of source addresses in the buffer pointed to by the <i>SourceList</i> parameter.

### -param SourceList [in]

A pointer to a buffer with the  IP addresses to associate with the multicast filter.

## -returns

On success,  <b>setipv4sourcefilter</b> returns NO_ERROR (0). Any nonzero return value indicates failure and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
Insufficient buffer space is available.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
</table>

## -remarks

The 
<b>setipv4sourcefilter</b> inline function is used to set the multicast filter state for an IPv4  socket.

This function is part of socket interface extensions for multicast source filters defined in RFC 3678. An app can  use these functions to retrieve and set the multicast source address filters associated with a socket. 

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2ipdef/ne-ws2ipdef-multicast_mode_type">MULTICAST_MODE_TYPE</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getipv4sourcefilter">getipv4sourcefilter</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getsourcefilter">getsourcefilter</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-in_addr">in_addr</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-setsourcefilter">setsourcefilter</a>