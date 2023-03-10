---
UID: NS:ws2def._CSADDR_INFO
title: CSADDR_INFO (ws2def.h)
description: The CSADDR_INFO (ws2def.h) structure contains Windows Sockets address information for a socket, network service, or namespace provider.
helpviewer_keywords: ["*LPCSADDR_INFO","*PCSADDR_INFO","CSADDR_INFO","CSADDR_INFO structure [Winsock]","IPPROTO_RM","IPPROTO_TCP","IPPROTO_UDP","SOCK_DGRAM","SOCK_RDM","SOCK_SEQPACKET","SOCK_STREAM","_CSADDR_INFO","_win32_csaddr_info_2","winsock.csaddr_info_2","ws2def/CSADDR_INFO"]
old-location: winsock\csaddr_info_2.htm
tech.root: WinSock
ms.assetid: 9cad3586-e315-4f6f-9045-7c95502bb768
ms.date: 08/16/2022
ms.keywords: '*LPCSADDR_INFO, *PCSADDR_INFO, CSADDR_INFO, CSADDR_INFO structure [Winsock], IPPROTO_RM, IPPROTO_TCP, IPPROTO_UDP, SOCK_DGRAM, SOCK_RDM, SOCK_SEQPACKET, SOCK_STREAM, _CSADDR_INFO, _win32_csaddr_info_2, winsock.csaddr_info_2, ws2def/CSADDR_INFO'
req.header: ws2def.h
req.include-header: Nspapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: CSADDR_INFO, *PCSADDR_INFO, *LPCSADDR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CSADDR_INFO
 - ws2def/_CSADDR_INFO
 - PCSADDR_INFO
 - ws2def/PCSADDR_INFO
 - CSADDR_INFO
 - ws2def/CSADDR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - CSADDR_INFO
---

# CSADDR_INFO structure


## -description

The 
<b>CSADDR_INFO</b> structure contains Windows Sockets address information for a socket, network service, or namespace provider.

## -struct-fields

### -field LocalAddr

Type: <b>SOCKET_ADDRESS</b>

The Windows Sockets local address.

In a client application, pass this address to the 
<b>bind</b> function to obtain access to a network service.

In a network service, pass this address to the 
<b>bind</b> function so that the service is bound to the appropriate local address.

### -field RemoteAddr

Type: <b>SOCKET_ADDRESS</b>

Windows Sockets remote address. 

There are several uses for this remote address:<ul>
<li>You can use this remote address to connect to the service through the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> function. This is useful if an application performs 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>/<a href="/windows/desktop/api/winsock/nf-winsock-recv">receive</a> operations that involve connection-oriented protocols.</li>
<li>You can use this remote address with the 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> function when you are communicating over a connectionless (datagram) protocol. If you are using a connectionless protocol, such as UDP, 
<b>sendto</b> is typically the way you pass data to the remote system.</li>
</ul>

### -field iSocketType

Type: <b>INT</b>

The type of Windows socket. Possible values for the socket type are defined in the <i>Winsock2.h</i> header file.

The following table lists the possible values supported for Windows Sockets 2:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SOCK_STREAM"></a><a id="sock_stream"></a><dl>
<dt><b>SOCK_STREAM</b></dt>
</dl>
</td>
<td width="60%">
A stream socket. This is a protocol that sends data as a stream of bytes, with no message boundaries. This socket type provides sequenced, reliable, two-way, connection-based byte streams with an OOB data transmission mechanism. This socket type uses the Transmission Control Protocol (TCP) for the Internet address family (AF_INET or AF_INET6).


</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_DGRAM"></a><a id="sock_dgram"></a><dl>
<dt><b>SOCK_DGRAM</b></dt>
</dl>
</td>
<td width="60%">
A datagram socket. This socket type supports datagrams, which are connectionless, unreliable buffers of a fixed (typically small) maximum length. This socket type uses the User Datagram Protocol (UDP) for the Internet address family (AF_INET or AF_INET6).


Services use 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a> function to obtain datagrams. The 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> functions do not work with datagrams.

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_RDM"></a><a id="sock_rdm"></a><dl>
<dt><b>SOCK_RDM</b></dt>
</dl>
</td>
<td width="60%">
A reliable message datagram socket. This socket type preserves message boundaries in data. An example of this type is the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as <a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">reliable multicast programming</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_SEQPACKET"></a><a id="sock_seqpacket"></a><dl>
<dt><b>SOCK_SEQPACKET</b></dt>
</dl>
</td>
<td width="60%">
A sequenced packet stream socket. This socket type provides a pseudo-stream packet based on datagrams. 


</td>
</tr>
</table>

### -field iProtocol

Type: <b>INT</b>

The protocol used. The possible options for the <i>protocol</i> parameter are specific to the address family and socket type specified. Possible values are defined in the  <i>Winsock2.h</i> and <i>Wsrm.h</i> header files.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and this parameter can be one of the values from the <b>IPPROTO</b> enumeration type defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The table below lists common values for the <i>protocol</i> although many other values are possible. 

<table>
<tr>
<th>protocol</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_TCP"></a><a id="ipproto_tcp"></a><dl>
<dt><b>IPPROTO_TCP</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The Transmission Control Protocol (TCP). This is a possible value when the address family is  <b>AF_INET</b> or <b>AF_INET6</b> and the <b>iSocketType</b> member is <b>SOCK_STREAM</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_UDP"></a><a id="ipproto_udp"></a><dl>
<dt><b>IPPROTO_UDP</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The User Datagram Protocol (UDP). This is a possible value when the address family is  <b>AF_INET</b> or <b>AF_INET6</b> and the <b>iSocketType</b> member is <b>SOCK_DGRAM</b>. 

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_RM"></a><a id="ipproto_rm"></a><dl>
<dt><b>IPPROTO_RM</b></dt>
<dt>113</dt>
</dl>
</td>
<td width="60%">
The PGM protocol for reliable multicast. This is a possible value when the address family is <b>AF_INET</b> and the <b>iSocketType</b> member is <b>SOCK_RDM</b>. On the Windows SDK released for Windows Vista and later,  this value is also called <b>IPPROTO_PGM</b>.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/nspapi/nf-nspapi-getaddressbynamea">GetAddressByName</a> function obtains Windows Sockets address information using 
<b>CSADDR_INFO</b> structures. 

The <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function called with the <a href="/windows/desktop/WinSock/so-bsp-state">SO_BSP_STATE</a> socket option retrieves a <b>CSADDR_INFO</b> structure for the specified socket.

## -see-also

<a href="/windows/desktop/api/nspapi/nf-nspapi-getaddressbynamea">GetAddressByName</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>



<a href="/windows/desktop/WinSock/so-bsp-state">SO_BSP_STATE</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>
