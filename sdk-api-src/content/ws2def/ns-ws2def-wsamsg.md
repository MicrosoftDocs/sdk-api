---
UID: NS:ws2def._WSAMSG
title: WSAMSG (ws2def.h)
description: Used with the WSARecvMsg and WSASendMsg functions to store address and optional control information about connected and unconnected sockets as well as an array of buffers used to store message data.
helpviewer_keywords: ["*LPWSAMSG","*PWSAMSG","LPWSAMSG","LPWSAMSG structure pointer [Winsock]","MSG_BCAST","MSG_CTRUNC","MSG_MCAST","MSG_PEEK","MSG_TRUNC","PWSAMSG","PWSAMSG structure pointer [Winsock]","WSAMSG","WSAMSG structure [Winsock]","_win32_wsamsg_2","mswsock/LPWSAMSG","mswsock/PWSAMSG","mswsock/WSAMSG","winsock.wsamsg_2","ws2def/LPWSAMSG","ws2def/PWSAMSG","ws2def/WSAMSG"]
old-location: winsock\wsamsg_2.htm
tech.root: WinSock
ms.assetid: 105a6e2c-1edf-4ec0-a1c2-ac0bcafeda30
ms.date: 11/13/2020
ms.keywords: '*LPWSAMSG, *PWSAMSG, LPWSAMSG, LPWSAMSG structure pointer [Winsock], MSG_BCAST, MSG_CTRUNC, MSG_MCAST, MSG_PEEK, MSG_TRUNC, PWSAMSG, PWSAMSG structure pointer [Winsock], WSAMSG, WSAMSG structure [Winsock], _win32_wsamsg_2, mswsock/LPWSAMSG, mswsock/PWSAMSG, mswsock/WSAMSG, winsock.wsamsg_2, ws2def/LPWSAMSG, ws2def/PWSAMSG, ws2def/WSAMSG'
req.header: ws2def.h
req.include-header: Winsock2.h
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
req.typenames: WSAMSG, *PWSAMSG, *LPWSAMSG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSAMSG
 - ws2def/_WSAMSG
 - PWSAMSG
 - ws2def/PWSAMSG
 - WSAMSG
 - ws2def/WSAMSG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
 - Mswsock.h
api_name:
 - WSAMSG
---

## -description

The 
<b>WSAMSG</b> structure is used with the 
<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a> and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a> functions to store address and optional control information about connected and unconnected sockets as well as an array of buffers used  to store message data.

## -struct-fields

### -field name

Type: <b>LPSOCKADDR</b>

A pointer to a 
<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structure that stores information about the remote address. Used only with unconnected sockets.

### -field namelen

Type: <b>INT</b>

The length, in bytes, of the 
<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structure pointed to in the <b>pAddr</b> member. Used only with unconnected sockets.

### -field lpBuffers

Type: <b>LPWSABUF</b>

An array of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures used to receive the message data. The capability of the <b>lpBuffers</b> member to contain multiple buffers enables the use of scatter/gather I/O.

### -field dwBufferCount

Type: <b>DWORD</b>

The number of buffers pointed to in the <b>lpBuffers</b> member.

### -field Control

Type: <b>WSABUF</b>

A structure of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> type used to specify optional control data. See Remarks.

### -field dwFlags

Type: <b>DWORD</b>

One or more control flags, specified as the logical <b>OR</b> of values. The possible values for <b>dwFlags</b> member on input are defined in the Winsock2.h header file. The possible values for <b>dwFlags</b> member on output are defined in the Ws2def.h header file which is automatically included by the Winsock2.h header file. 

<table>
<tr>
<th>Flags on input</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSG_PEEK"></a><a id="msg_peek"></a><dl>
<dt><b>MSG_PEEK</b></dt>
</dl>
</td>
<td width="60%">
Peek at the incoming data. The data is copied into the buffer, but is not removed from the input queue. This flag is valid only for non-overlapped sockets.

</td>
</tr>
</table>
 

<table>
<tr>
<th>Flag returned</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSG_BCAST"></a><a id="msg_bcast"></a><dl>
<dt><b>MSG_BCAST</b></dt>
</dl>
</td>
<td width="60%">
The datagram was received as a link-layer broadcast or with a destination IP address that is a broadcast address.

</td>
</tr>
<tr>
<td width="40%"><a id="MSG_MCAST"></a><a id="msg_mcast"></a><dl>
<dt><b>MSG_MCAST</b></dt>
</dl>
</td>
<td width="60%">
The datagram was received with a destination IP address that is a multicast address.

</td>
</tr>
<tr>
<td width="40%"><a id="MSG_TRUNC"></a><a id="msg_trunc"></a><dl>
<dt><b>MSG_TRUNC</b></dt>
</dl>
</td>
<td width="60%">
The datagram was truncated. More data was present than the process allocated room for.

</td>
</tr>
<tr>
<td width="40%"><a id="MSG_CTRUNC"></a><a id="msg_ctrunc"></a><dl>
<dt><b>MSG_CTRUNC</b></dt>
</dl>
</td>
<td width="60%">
The control (ancillary) data was truncated. More control data was present than the process allocated room for.

</td>
</tr>
</table>

## -remarks

In the Microsoft Windows Software Development Kit (SDK), the version of this structure for use on Windows Vista is defined with the data type for the <b>dwBufferCount</b> and <b>dwFlags</b> members as a <b>ULONG</b>.  When compiling an application if the target platform is Windows Vista and later (<b>NTDDI_VERSION &gt;= NTDDI_LONGHORN, _WIN32_WINNT &gt;= 0x0600</b>, or <b>WINVER &gt;= 0x0600</b>), the data type for the <b>dwBufferCount</b> and <b>dwFlags</b> members is a <b>ULONG</b>.

<b>Windows Server 2003 and Windows XP:  </b> When compiling an application, the data type for the <b>dwBufferCount</b> and <b>dwFlags</b> members is a <b>DWORD</b>.

On the Windows SDK released for Windows Vista and later, the <b>WSAMSG</b> structure is defined in the Ws2def.h header file. Note that the Ws2def.h header file is automatically included in Winsock2.h, and should never be used directly

If the datagram or control data is truncated during the transmission, the function being used in association with the 
<b>WSAMSG</b> structure returns SOCKET_ERROR and a call to the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function returns WSAEMSGSIZE. It is up to the application to determine what was truncated by checking for MSG_TRUNC and/or MSG_CTRUNC flags.

### Use of the control member

The following table summarizes the various uses of control data available for use in the *Control* member for IPv4 and IPv6.

|Protocol|cmsg_level|cmsg_type|Description|
|-|-|-|-|
|IPv4|IPPROTO_IP|IP_ORIGINAL_ARRIVAL_IF|Receives the original IPv4 arrival interface where the packet was received for datagram sockets. This control data is used by firewalls when a Teredo, 6to4, or ISATAP tunnel is used for IPv4 NAT traversal. The cmsg_data[] member in the <b>WSAMSG</b> structure is a <b>ULONG</b> that contains the IF_INDEX defined in the Ifdef.h header file.<br/><br/>For more information, see the <a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IPPROTO_IP Socket Options</a> for the IP_ORIGINAL_ARRIVAL_IF socket option.<br/><br/><b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP: </b>The IP_ORIGINAL_ARRIVAL_IF <b>cmsg_type</b> is not supported.|
|IPv4|IPPROTO_IP|[IP_PKTINFO](/windows/desktop/WinSock/ip-pktinfo)|Specifies/receives packet information for an IPv4 socket. For more information, see the <a href="/windows/desktop/WinSock/ip-pktinfo">IP_PKTINFO</a> socket option.|
|IPv4|IPPROTO_IP|IP_ECN|Specifies/receives ECN codepoint in the Type of Service (TOS) IPv4 header field. For more info, see [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn).|
|IPv6|IPPROTO_IPV6|IPV6_DSTOPTS|Specifies/receives destination options.|
|IPv6|IPPROTO_IPV6|IPV6_HOPLIMIT|Specifies/receives hop limit. For more information, see the <a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPPROTO_IPV6 Socket Options</a> for the IPV6_HOPLIMIT socket option.|
|IPv6|IPPROTO_IPV6|IPV6_HOPOPTS|Specifies/receives hop-by-hop options.|
|IPv6|IPPROTO_IPV6|IPV6_NEXTHOP|Specifies next-hop address.|
|IPv6|IPPROTO_IPV6|[IPV6_PKTINFO](/windows/desktop/WinSock/ipv6-pktinfo)|Specifies/receives packet information for an IPv6 socket. For more information, see the <a href="/windows/desktop/WinSock/ipv6-pktinfo">IPV6_PKTINFO</a> socket option.|
|IPv6|IPPROTO_IPV6|IPV6_RTHDR|Specifies/receives routing header.|
|IPv6|IPPROTO_IPV6|IPV6_ECN|Specifies/receives ECN codepoint in the Traffic Class IPv6 header field. For more information, see [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn).|

Control data is made up of one or more control data objects, each beginning with a <b>WSACMSGHDR</b> structure, defined as the following.

```cpp
struct wsacmsghdr {
  UINT        cmsg_len;
  INT         cmsg_level;
  INT         cmsg_type;
  /* followed by UCHAR cmsg_data[] */
} WSACMSGHDR;
```

<div class="alert"><b>Note</b>  The transport, not the application, fills out the header information in the <b>WSACMSGHDR</b> structure. The application simply sets the needed socket options and provides the adequate buffer size.</div>
<div> </div>

The members of the <b>WSACMSGHDR</b> structure are as follows:




<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="cmsg_len"></a><a id="CMSG_LEN"></a>cmsg_len

</td>
<td width="60%">
The number of bytes of data starting from the beginning of the <b>WSACMSGHDR</b> to the end of data (excluding padding bytes that may follow data). 

</td>
</tr>
<tr>
<td width="40%">
<a id="cmsg_level"></a><a id="CMSG_LEVEL"></a>cmsg_level

</td>
<td width="60%">
The protocol that originated the control information. 

</td>
</tr>
<tr>
<td width="40%">
<a id="cmsg_type"></a><a id="CMSG_TYPE"></a>cmsg_type

</td>
<td width="60%">
The protocol-specific type of control information.

</td>
</tr>
</table>
 



The following macros are used to navigate the data objects:


```cpp

#define LPCMSGHDR *WSA_CMSG_FIRSTHDR(LPWSAMSG msg);

```


Returns a pointer to the first control data object. Returns a <b>NULL</b> pointer if there is no control data in the 
<b>WSAMSG</b> structure, such as when the <b>Control</b> member is a <b>NULL</b> pointer.


```cpp

#define LPCMSGHDR *WSA_CMSG_NXTHDR(LPWSAMSG msg, LPWSACMSGHDR cmsg);

```


Returns a pointer to the next control data object, or <b>NULL</b> if there are no more data objects. If the  <i>pcmsg</i> parameter is <b>NULL</b>, a pointer to the first control data object is returned.


```cpp

#define UCHAR *WSA_CMSG_DATA(LPWSACMSGHDR pcmsg);

```


Returns a pointer to the first byte of data (referred to as the <b>cmsg_data</b> member, though it is not defined in the structure).


```cpp

#define UINT WSA_CMSG_SPACE(UINT length);

```


Returns the total size of a control data object, given the amount of data. Used to allocate the correct amount of buffer space. Includes alignment padding.


```cpp

#define UINT WSA_CMSG_LEN(UINT length);

```


Returns the value in <b>cmsg_len</b> given the amount of data. Includes alignment padding.

## -see-also

<a href="/windows/desktop/WinSock/ipv6-pktinfo">IPV6_PKTINFO</a>



<a href="/windows/desktop/WinSock/ip-pktinfo">IP_PKTINFO</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>



<a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a>