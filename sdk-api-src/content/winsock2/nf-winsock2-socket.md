---
UID: NF:winsock2.socket
title: socket function (winsock2.h)
description: The socket function creates a socket that is bound to a specific transport service provider.
helpviewer_keywords: ["AF_APPLETALK","AF_BTH","AF_INET","AF_INET6","AF_IPX","AF_IRDA","AF_NETBIOS","AF_UNSPEC","BTHPROTO_RFCOMM","IPPROTO_ICMP","IPPROTO_ICMPV6","IPPROTO_IGMP","IPPROTO_RM","IPPROTO_TCP","IPPROTO_UDP","SOCK_DGRAM","SOCK_RAW","SOCK_RDM","SOCK_SEQPACKET","SOCK_STREAM","_win32_socket_2","socket","socket function [Winsock]","winsock.socket_2","winsock2/socket"]
old-location: winsock\socket_2.htm
tech.root: WinSock
ms.assetid: 6bf6e6c4-6268-479c-86a6-52e90cf317db
ms.date: 12/05/2018
ms.keywords: AF_APPLETALK, AF_BTH, AF_INET, AF_INET6, AF_IPX, AF_IRDA, AF_NETBIOS, AF_UNSPEC, BTHPROTO_RFCOMM, IPPROTO_ICMP, IPPROTO_ICMPV6, IPPROTO_IGMP, IPPROTO_RM, IPPROTO_TCP, IPPROTO_UDP, SOCK_DGRAM, SOCK_RAW, SOCK_RDM, SOCK_SEQPACKET, SOCK_STREAM, _win32_socket_2, socket, socket function [Winsock], winsock.socket_2, winsock2/socket
req.header: winsock2.h
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
 - socket
 - winsock2/socket
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
 - socket
---

# socket function


## -description

The 
<b>socket</b> function creates a socket that is bound to a specific transport service provider.

## -parameters

### -param af [in]

The address family specification. Possible values for the address family are defined in the <i>Winsock2.h</i> header file. 

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the possible values for the address family are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are AF_INET or AF_INET6, which are the Internet
                     address family formats for IPv4 and IPv6. Other options for address family (AF_NETBIOS for use with NetBIOS, for example) are supported if a Windows Sockets service provider for the address family is installed. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

The table below lists common values for address family although many other values are possible. 

<table>
<tr>
<th>Af</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_IPX"></a><a id="af_ipx"></a><dl>
<dt><b>AF_IPX</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The IPX/SPX address family. This address family is only supported if the NWLink IPX/SPX NetBIOS Compatible Transport protocol is installed. 

This address family is not supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_APPLETALK"></a><a id="af_appletalk"></a><dl>
<dt><b>AF_APPLETALK</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The AppleTalk address family. This address family is only supported if the AppleTalk protocol is installed. 

This address family is not supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_NETBIOS"></a><a id="af_netbios"></a><dl>
<dt><b>AF_NETBIOS</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The NetBIOS address family. This address family is only supported if the Windows Sockets provider for NetBIOS is installed. 

The Windows Sockets provider for NetBIOS  is supported on 32-bit versions of Windows. This provider is installed by default on 32-bit versions of Windows. 

The Windows Sockets provider for NetBIOS is not supported on 64-bit versions of windows including Windows 7,  Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.  

The Windows Sockets provider for NetBIOS  only supports sockets where the <i>type</i> parameter is set to <b>SOCK_DGRAM</b>.

The Windows Sockets provider for NetBIOS  is not directly related to the <a href="/previous-versions/windows/desktop/netbios/portal">NetBIOS</a> programming interface. The NetBIOS programming interface is not supported on Windows Vista, Windows Server 2008, and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_IRDA"></a><a id="af_irda"></a><dl>
<dt><b>AF_IRDA</b></dt>
<dt>26</dt>
</dl>
</td>
<td width="60%">
The Infrared Data Association (IrDA) address family. 

This address family is only supported if the computer has an infrared port and driver installed.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_BTH"></a><a id="af_bth"></a><dl>
<dt><b>AF_BTH</b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
The Bluetooth address family. 

This address family is supported on Windows XP with SP2 or later if the computer has a Bluetooth adapter and driver installed.

</td>
</tr>
</table>

### -param type [in]

The type specification for the new socket. 


Possible values for the socket type are defined in the <i>Winsock2.h</i> header file.

The following table lists the possible values for the <i>type</i> parameter supported for Windows Sockets 2:

<table>
<tr>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SOCK_STREAM"></a><a id="sock_stream"></a><dl>
<dt><b>SOCK_STREAM</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A socket type that provides sequenced, reliable, two-way, connection-based byte streams with an OOB data transmission mechanism. This socket type uses the Transmission Control Protocol (TCP) for the Internet address family (AF_INET or AF_INET6).

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_DGRAM"></a><a id="sock_dgram"></a><dl>
<dt><b>SOCK_DGRAM</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A socket type that supports datagrams, which are connectionless, unreliable buffers of a fixed (typically small) maximum length. This socket type uses the User Datagram Protocol (UDP) for the Internet address family (AF_INET or AF_INET6).

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_RAW"></a><a id="sock_raw"></a><dl>
<dt><b>SOCK_RAW</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A socket type that provides a raw socket that allows an application to manipulate the next upper-layer protocol header. To manipulate the IPv4 header, the <a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IP_HDRINCL</a> socket option must be set on the socket.  To manipulate the IPv6 header, the <a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPV6_HDRINCL</a> socket option must be set on the socket.  

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_RDM"></a><a id="sock_rdm"></a><dl>
<dt><b>SOCK_RDM</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
A socket type that provides a reliable message datagram. An example of this type is the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as <a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">reliable multicast programming</a>. 

This <i>type</i> value is only supported if the Reliable Multicast Protocol is installed.

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_SEQPACKET"></a><a id="sock_seqpacket"></a><dl>
<dt><b>SOCK_SEQPACKET</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
A socket type that provides a pseudo-stream packet based on datagrams. 

</td>
</tr>
</table>
 

In Windows Sockets 2, new socket types were introduced. An application can dynamically discover the attributes of each available transport protocol through the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> function. So an application can determine the possible socket type and protocol options for an address family  and use this information when specifying this parameter. Socket type definitions in the <i>Winsock2.h</i> and <i>Ws2def.h</i> header files will be periodically updated as new socket types, address families, and protocols are defined.

In Windows Sockets 1.1, the only possible socket types are <b>SOCK_DGRAM</b> and <b>SOCK_STREAM</b>.

### -param protocol [in]

The protocol to be used. The possible options for the <i>protocol</i> parameter are specific to the address family and socket type specified. Possible values for the <i>protocol</i> are defined in the  <i>Winsock2.h</i> and <i>Wsrm.h</i> header files.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and this parameter can be one of the values from the <b>IPPROTO</b> enumeration type defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

If a value of  0 is specified, the caller does not
              wish to specify a protocol and the service provider will choose the <i>protocol</i> to use.


When the <i>af</i> parameter is AF_INET or AF_INET6 and the <i>type</i> is <b>SOCK_RAW</b>, the value specified for the <i>protocol</i> is set in the protocol field of the IPv6 or IPv4 packet header. 

The table below lists common values for the <i>protocol</i> although many other values are possible. 

<table>
<tr>
<th>protocol</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_ICMP"></a><a id="ipproto_icmp"></a><dl>
<dt><b>IPPROTO_ICMP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The Internet Control Message Protocol (ICMP). This is a possible value when the <i>af</i> parameter is <b>AF_UNSPEC</b>, <b>AF_INET</b>, or <b>AF_INET6</b> and the <i>type</i> parameter is <b>SOCK_RAW</b> or unspecified.

This <i>protocol</i> value is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_IGMP"></a><a id="ipproto_igmp"></a><dl>
<dt><b>IPPROTO_IGMP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Group Management Protocol (IGMP). This is a possible value when the <i>af</i> parameter is <b>AF_UNSPEC</b>, <b>AF_INET</b>, or <b>AF_INET6</b> and the <i>type</i> parameter is <b>SOCK_RAW</b> or unspecified.

This <i>protocol</i> value is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="BTHPROTO_RFCOMM"></a><a id="bthproto_rfcomm"></a><dl>
<dt><b>BTHPROTO_RFCOMM</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The Bluetooth Radio Frequency Communications (Bluetooth RFCOMM) protocol. This is a possible value when the <i>af</i> parameter is <b>AF_BTH</b> and the <i>type</i> parameter is <b>SOCK_STREAM</b>. 

This <i>protocol</i> value is supported on Windows XP with SP2 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_TCP"></a><a id="ipproto_tcp"></a><dl>
<dt><b>IPPROTO_TCP</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The Transmission Control Protocol (TCP). This is a possible value when the <i>af</i> parameter is <b>AF_INET</b> or <b>AF_INET6</b> and the <i>type</i> parameter is <b>SOCK_STREAM</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_UDP"></a><a id="ipproto_udp"></a><dl>
<dt><b>IPPROTO_UDP</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The User Datagram Protocol (UDP). This is a possible value when the <i>af</i> parameter is <b>AF_INET</b> or <b>AF_INET6</b> and the <i>type</i> parameter is <b>SOCK_DGRAM</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_ICMPV6"></a><a id="ipproto_icmpv6"></a><dl>
<dt><b>IPPROTO_ICMPV6</b></dt>
<dt>58</dt>
</dl>
</td>
<td width="60%">
The Internet Control Message Protocol  Version 6 (ICMPv6). This is a possible value when the <i>af</i> parameter is <b>AF_UNSPEC</b>, <b>AF_INET</b>, or <b>AF_INET6</b>  and the <i>type</i> parameter is <b>SOCK_RAW</b> or unspecified.

This <i>protocol</i> value is supported on Windows XP and later.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_RM"></a><a id="ipproto_rm"></a><dl>
<dt><b>IPPROTO_RM</b></dt>
<dt>113</dt>
</dl>
</td>
<td width="60%">
The PGM protocol for reliable multicast. This is a possible value when the <i>af</i> parameter is <b>AF_INET</b> and the <i>type</i> parameter is <b>SOCK_RDM</b>. On the Windows SDK released for Windows Vista and later,  this protocol is also called <b>IPPROTO_PGM</b>. 

This <i>protocol</i> value is only supported if the Reliable Multicast Protocol is installed.

</td>
</tr>
</table>

## -returns

If no error occurs, 
<b>socket</b> returns a descriptor referencing the new socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem or the associated service provider has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported. For example, an application tried to create a socket for the <b>AF_IRDA</b> address family but an infrared adapter and device driver is not installed on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was supplied.  This error is returned if the <i>af</i> parameter is set to <b>AF_UNSPEC</b> and the <i>type</i> and <i>protocol</i> parameter are unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVALIDPROVIDER</a></b></dt>
</dl>
</td>
<td width="60%">
The service provider returned a version other than 2.2.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVALIDPROCTABLE</a></b></dt>
</dl>
</td>
<td width="60%">
The service provider returned an invalid or incomplete procedure table to the 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTONOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified protocol is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTOTYPE</a></b></dt>
</dl>
</td>
<td width="60%">
The specified protocol is the wrong type for this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROVIDERFAILEDINIT</a></b></dt>
</dl>
</td>
<td width="60%">
The service provider failed to initialize. This error is returned if a layered service provider (LSP) or namespace provider was improperly installed or the provider fails to operate correctly. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESOCKTNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified socket type is not supported in this address family.

</td>
</tr>
</table>

## -remarks

The 
<b>socket</b> function causes a socket descriptor and any related resources to be allocated and bound to a specific transport-service provider. Winsock will utilize the first available service provider that supports the requested combination of address family, socket type and protocol parameters. The socket that is created will have the overlapped attribute as a default. For Windows, the Microsoft-specific socket option, SO_OPENTYPE, defined in Mswsock.h can affect this default. See Microsoft-specific documentation for a detailed description of SO_OPENTYPE.

Sockets without the overlapped attribute can be created by using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>. All functions that allow overlapped operation (<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>,
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>) also support nonoverlapped usage on an overlapped socket if the values for parameters related to overlapped operation are <b>NULL</b>.

When selecting a protocol and its supporting service provider this procedure will only choose a base protocol or a protocol chain, not a protocol layer by itself. Unchained protocol layers are not considered to have partial matches on <i>type</i> or <i>af</i> either. That is, they do not lead to an error code of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a> or 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTONOSUPPORT</a> if no suitable protocol is found.

<div class="alert"><b>Note</b>    The manifest constant <b>AF_UNSPEC</b> continues to be defined in the header file but its use is strongly discouraged, as this can cause ambiguity in interpreting the value of the <i>protocol</i> parameter.</div>
<div> </div>
Applications are encouraged to use <b>AF_INET6</b> for the <i>af</i> parameter and create a dual-mode socket that can be used with both IPv4 and IPv6.

Connection-oriented sockets such as <b>SOCK_STREAM</b> provide full-duplex connections, and must be in a connected state before any data can be sent or received on it. A connection to another socket is created with a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> call. Once connected, data can be transferred using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> calls. When a session has been completed, a 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> must be performed.

The communications protocols used to implement a reliable, connection-oriented socket ensure that data is not lost or duplicated. If data for which the peer protocol has buffer space cannot be successfully transmitted within a reasonable length of time, the connection is considered broken and subsequent calls will fail with the error code set to 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>.

Connectionless, message-oriented sockets allow sending and receiving of datagrams to and from arbitrary peers using 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>. If such a socket is connected to a specific peer, datagrams can be sent to that peer using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> and can be received only from this peer using 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>.

IPv6 and IPv4 operate differently when receiving a socket with a <i>type</i> of <b>SOCK_RAW</b>. The IPv4 receive packet includes the packet payload, the next upper-level header (for example, the IP header for a TCP or UDP packet), and the IPv4 packet header. The IPv6 receive packet includes the packet payload and the next upper-level header. The IPv6 receive packet never includes the IPv6 packet header.

<div class="alert"><b>Note</b>  On Windows NT, raw socket support requires administrative privileges.</div>
<div> </div>
A socket with a <i>type</i> parameter of <b>SOCK_SEQPACKET</b> is based on datagrams, but functions as a pseudo-stream protocol. For both send and receive packets, separate datagrams are used. However, Windows Sockets can coalesce multiple receive packets into a single packet. So an application  can issue a receive call (for example, <a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> or <a href="/windows/desktop/api/mswsock/nf-mswsock-wsarecvex">WSARecvEx</a>) and retrieve the data from several coalesced multiple packets in single call. The AF_NETBIOS address family supports a <i>type</i> parameter of <b>SOCK_SEQPACKET</b>.

When the <i>af</i> parameter is <b>AF_NETBIOS</b> for NetBIOS over TCP/IP, the <i>type</i> parameter can be  <b>SOCK_DGRAM</b> or <b>SOCK_SEQPACKET</b>. For the <b>AF_NETBIOS</b> address family, the <i>protocol</i> parameter is the LAN adapter number represented as a negative number.

On Windows XP and later, the following command can be used to list the Windows Sockets catalog to determine the service providers installed and the address family, socket type, and protocols that are supported.

<b>netsh winsock show catalog </b>

Support for sockets with type <b>SOCK_RAW</b> is not required, but service providers are encouraged to support raw sockets as practicable.

<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>
Keep the following in mind:

<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
<li>Only <b>SOCK_STREAM</b> is supported; the <b>SOCK_DGRAM</b> type is not supported by IrDA.</li>
<li>The <i>protocol</i> parameter is always set to 0 for IrDA.</li>
</ul>
A socket for use with the AF_IRDA address family can only be created if the local computer has an infrared port and driver installed. Otherwise, a call to the <b>socket</b> function with <i>af</i> parameter set to AF_IRDA will fail and <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> returns <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTONOSUPPORT</a>. 

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>socket</b> function to create a socket that is bound to a specific transport service provider..


```cpp
#ifndef UNICODE
#define UNICODE 1
#endif

// link with Ws2_32.lib
#pragma comment(lib,"Ws2_32.lib")

#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>   // Needed for _wtoi


int __cdecl wmain(int argc, wchar_t **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData = {0};
    int iResult = 0;

//    int i = 1;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    // Validate the parameters
    if (argc != 4) {
        wprintf(L"usage: %s <addressfamily> <type> <protocol>\n", argv[0]);
        wprintf(L"socket opens a socket for the specified family, type, & protocol\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17\n", argv[0]);
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);
    
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }

    wprintf(L"Calling socket with following parameters:\n");
    wprintf(L"  Address Family = ");
    switch (iFamily) {
    case AF_UNSPEC:
        wprintf(L"Unspecified");
        break;
    case AF_INET:
        wprintf(L"AF_INET (IPv4)");
        break;
    case AF_INET6:
        wprintf(L"AF_INET6 (IPv6)");
        break;
    case AF_NETBIOS:
        wprintf(L"AF_NETBIOS (NetBIOS)");
        break;
    case AF_BTH:
        wprintf(L"AF_BTH (Bluetooth)");
        break;
    default:
        wprintf(L"Other");
        break;
    }
    wprintf(L" (%d)\n", iFamily);
    
    wprintf(L"  Socket type = ");
    switch (iType) {
    case 0:
        wprintf(L"Unspecified");
        break;
    case SOCK_STREAM:
        wprintf(L"SOCK_STREAM (stream)");
        break;
    case SOCK_DGRAM:
        wprintf(L"SOCK_DGRAM (datagram)");
        break;
    case SOCK_RAW:
        wprintf(L"SOCK_RAW (raw)");
        break;
    case SOCK_RDM:
        wprintf(L"SOCK_RDM (reliable message datagram)");
        break;
    case SOCK_SEQPACKET:
        wprintf(L"SOCK_SEQPACKET (pseudo-stream packet)");
        break;
    default:
        wprintf(L"Other");
        break;
    }
    wprintf(L" (%d)\n", iType);

    wprintf(L"  Protocol = %d = ", iProtocol);
    switch (iProtocol) {
    case 0:
        wprintf(L"Unspecified");
        break;
    case IPPROTO_ICMP:
        wprintf(L"IPPROTO_ICMP (ICMP)");
        break;
    case IPPROTO_IGMP:
        wprintf(L"IPPROTO_IGMP (IGMP)");
        break;
    case IPPROTO_TCP:
        wprintf(L"IPPROTO_TCP (TCP)");
        break;
    case IPPROTO_UDP:
        wprintf(L"IPPROTO_UDP (UDP)");
        break;
    case IPPROTO_ICMPV6:
        wprintf(L"IPPROTO_ICMPV6 (ICMP Version 6)");
        break;
    default:
        wprintf(L"Other");
        break;
    }
    wprintf(L" (%d)\n", iProtocol);

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) 
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError() );
    else {
        wprintf(L"socket function succeeded\n");

        // Close the socket to release the resources associated
        // Normally an application calls shutdown() before closesocket 
        //   to  disables sends or receives on a socket first
        // This isn't needed in this simple sample
        iResult = closesocket(sock);
        if (iResult == SOCKET_ERROR) {
            wprintf(L"closesocket failed with error = %d\n", WSAGetLastError() );
            WSACleanup();
            return 1;
        }    
    }

    WSACleanup();

    return 0;
}


```


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IPPROTO_IP Socket Options</a>



<a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPPROTO_IPV6 Socket Options</a>



<a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">Reliable Multicast Programming</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-ioctlsocket">ioctlsocket</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a>