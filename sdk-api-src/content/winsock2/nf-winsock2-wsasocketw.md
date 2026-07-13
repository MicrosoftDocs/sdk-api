---
UID: NF:winsock2.WSASocketW
title: WSASocketW function (winsock2.h)
description: The WSASocket function creates a socket that is bound to a specific transport-service provider. (Unicode)
helpviewer_keywords: ["AF_APPLETALK", "AF_BTH", "AF_INET", "AF_INET6", "AF_IPX", "AF_IRDA", "AF_NETBIOS", "AF_UNSPEC", "BTHPROTO_RFCOMM", "IPPROTO_ICMP", "IPPROTO_ICMPV6", "IPPROTO_IGMP", "IPPROTO_RM", "IPPROTO_TCP", "IPPROTO_UDP", "SG_CONSTRAINED_GROUP", "SG_UNCONSTRAINED_GROUP", "SOCK_DGRAM", "SOCK_RAW", "SOCK_RDM", "SOCK_SEQPACKET", "SOCK_STREAM", "WSASocket", "WSASocket function [Winsock]", "WSASocketW", "WSA_FLAG_ACCESS_SYSTEM_SECURITY", "WSA_FLAG_MULTIPOINT_C_LEAF", "WSA_FLAG_MULTIPOINT_C_ROOT", "WSA_FLAG_MULTIPOINT_D_LEAF", "WSA_FLAG_MULTIPOINT_D_ROOT", "WSA_FLAG_NO_HANDLE_INHERIT", "WSA_FLAG_OVERLAPPED", "_win32_wsasocket_2", "winsock.wsasocket_2", "winsock2/WSASocket", "winsock2/WSASocketW"]
old-location: winsock\wsasocket_2.htm
tech.root: WinSock
ms.assetid: dcf2e543-de54-43d9-9e45-4cb935da3548
ms.date: 12/05/2018
ms.keywords: AF_APPLETALK, AF_BTH, AF_INET, AF_INET6, AF_IPX, AF_IRDA, AF_NETBIOS, AF_UNSPEC, BTHPROTO_RFCOMM, IPPROTO_ICMP, IPPROTO_ICMPV6, IPPROTO_IGMP, IPPROTO_RM, IPPROTO_TCP, IPPROTO_UDP, SG_CONSTRAINED_GROUP, SG_UNCONSTRAINED_GROUP, SOCK_DGRAM, SOCK_RAW, SOCK_RDM, SOCK_SEQPACKET, SOCK_STREAM, WSASocket, WSASocket function [Winsock], WSASocketA, WSASocketW, WSA_FLAG_ACCESS_SYSTEM_SECURITY, WSA_FLAG_MULTIPOINT_C_LEAF, WSA_FLAG_MULTIPOINT_C_ROOT, WSA_FLAG_MULTIPOINT_D_LEAF, WSA_FLAG_MULTIPOINT_D_ROOT, WSA_FLAG_NO_HANDLE_INHERIT, WSA_FLAG_OVERLAPPED, _win32_wsasocket_2, winsock.wsasocket_2, winsock2/WSASocket, winsock2/WSASocketA, winsock2/WSASocketW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSASocketW (Unicode) and WSASocketA (ANSI)
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
 - WSASocketW
 - winsock2/WSASocketW
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
 - WSASocket
 - WSASocketA
 - WSASocketW
---

# WSASocketW function


## -description

The 
<b>WSASocket</b> function creates a socket that is bound to a specific transport-service provider.

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

The protocol to be used. The possible options for the <i>protocol</i> parameter are specific to the address family and socket type specified. Possible values for the <i>protocol</i> are defined are defined in the  <i>Winsock2.h</i> and <i>Wsrm.h</i> header files. 

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

### -param lpProtocolInfo [in]

A pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure that defines the characteristics of the socket to be created. If this parameter is not <b>NULL</b>, the socket will be bound to the provider associated with the indicated 
<b>WSAPROTOCOL_INFO</b> structure.

### -param g [in]

An existing socket group ID or an appropriate action to take when creating a new socket and a new socket group. 

If <i>g</i> is an existing socket group ID, join the new socket to this
            socket group, provided all the requirements set by this group are met. 

If <i>g</i> is not an existing socket group ID, then the following values are possible.

<table>
<tr>
<th>g</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No group operation is performed. 

</td>
</tr>
<tr>
<td width="40%"><a id="SG_UNCONSTRAINED_GROUP"></a><a id="sg_unconstrained_group"></a><dl>
<dt><b>SG_UNCONSTRAINED_GROUP</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Create an unconstrained socket group and have the new socket  be the first member. For an unconstrained group, Winsock does not constrain all sockets in the socket group to have been created with the same value for the <i>type</i> and <i>protocol</i> parameters. 

</td>
</tr>
<tr>
<td width="40%"><a id="SG_CONSTRAINED_GROUP"></a><a id="sg_constrained_group"></a><dl>
<dt><b>SG_CONSTRAINED_GROUP</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Create a constrained socket group and have the new socket  be the first member. For a constrained socket group, Winsock constrains all sockets in the socket group to have been created with the same value for the <i>type</i> and <i>protocol</i> parameters. A constrained socket group may consist only of connection-oriented sockets, and requires that connections on all grouped sockets be to the same address on the same host.  

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The SG_UNCONSTRAINED_GROUP and SG_CONSTRAINED_GROUP constants are not currently defined in a public header file.</div>
<div> </div>

### -param dwFlags [in]

A set of flags used to specify additional socket attributes. 

A combination of these flags may be set, although some combinations are not allowed. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSA_FLAG_OVERLAPPED"></a><a id="wsa_flag_overlapped"></a><dl>
<dt><b>WSA_FLAG_OVERLAPPED</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Create a socket that supports overlapped I/O operations.

Most sockets should be created with this flag set. Overlapped sockets can utilize 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, and 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> for overlapped I/O operations, which allow multiple operations to be initiated and in progress simultaneously. 

All functions that allow overlapped operation (<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>) also support nonoverlapped usage on an overlapped socket if the values for parameters related to overlapped operations are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WSA_FLAG_MULTIPOINT_C_ROOT"></a><a id="wsa_flag_multipoint_c_root"></a><dl>
<dt><b>WSA_FLAG_MULTIPOINT_C_ROOT</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Create a socket that will be a c_root in a multipoint session.

This attribute is only allowed if the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider that creates the socket supports a multipoint or multicast mechanism and the control plane for a multipoint session is rooted. This would be indicated by the <b>dwServiceFlags1</b> 
 member of the <b>WSAPROTOCOL_INFO</b> structure  with the <b>XP1_SUPPORT_MULTIPOINT</b> and <b>XP1_MULTIPOINT_CONTROL_PLANE</b>  flags set. 

When the <i>lpProtocolInfo</i> parameter is not NULL, the  <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider is pointed to by the <i>lpProtocolInfo</i> parameter.  When the <i>lpProtocolInfo</i> parameter is NULL, the  <b>WSAPROTOCOL_INFO</b> structure is based on the transport provider selected by the values specified for the  <i>af</i>, <i>type</i>, and <i>protocol</i> parameters. 

Refer to 
<a href="/windows/desktop/WinSock/multipoint-and-multicast-semantics-2">Multipoint and Multicast Semantics</a> for additional information on a multipoint session.

</td>
</tr>
<tr>
<td width="40%"><a id="WSA_FLAG_MULTIPOINT_C_LEAF"></a><a id="wsa_flag_multipoint_c_leaf"></a><dl>
<dt><b>WSA_FLAG_MULTIPOINT_C_LEAF</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Create a socket that will be a c_leaf in a multipoint session.

This attribute is only allowed if the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider that creates the socket supports a multipoint or multicast mechanism and the control plane for a multipoint session is non-rooted. This would be indicated by the <b>dwServiceFlags1</b> 
 member of the <b>WSAPROTOCOL_INFO</b> structure  with the <b>XP1_SUPPORT_MULTIPOINT</b> flag set and the <b>XP1_MULTIPOINT_CONTROL_PLANE</b>  flag not set. 

When the <i>lpProtocolInfo</i> parameter is not NULL, the  <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider is pointed to by the <i>lpProtocolInfo</i> parameter.  When the <i>lpProtocolInfo</i> parameter is NULL, the  <b>WSAPROTOCOL_INFO</b> structure is based on the transport provider selected by the values specified for the  <i>af</i>, <i>type</i>, and <i>protocol</i> parameters. 

Refer to 
<a href="/windows/desktop/WinSock/multipoint-and-multicast-semantics-2">Multipoint and Multicast Semantics</a> for additional information on a multipoint session.

</td>
</tr>
<tr>
<td width="40%"><a id="WSA_FLAG_MULTIPOINT_D_ROOT"></a><a id="wsa_flag_multipoint_d_root"></a><dl>
<dt><b>WSA_FLAG_MULTIPOINT_D_ROOT</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Create a socket that will be a d_root in a multipoint session.

This attribute is only allowed if the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider that creates the socket supports a multipoint or multicast mechanism and the data plane for a multipoint session is rooted. This would be indicated by the <b>dwServiceFlags1</b> 
 member of the <b>WSAPROTOCOL_INFO</b> structure  with the <b>XP1_SUPPORT_MULTIPOINT</b> and <b>XP1_MULTIPOINT_DATA_PLANE</b>  flags set. 

When the <i>lpProtocolInfo</i> parameter is not NULL, the  <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider is pointed to by the <i>lpProtocolInfo</i> parameter.  When the <i>lpProtocolInfo</i> parameter is NULL, the  <b>WSAPROTOCOL_INFO</b> structure is based on the transport provider selected by the values specified for the  <i>af</i>, <i>type</i>, and <i>protocol</i> parameters. 

Refer to 
<a href="/windows/desktop/WinSock/multipoint-and-multicast-semantics-2">Multipoint and Multicast Semantics</a> for additional information on a multipoint session.

</td>
</tr>
<tr>
<td width="40%"><a id="WSA_FLAG_MULTIPOINT_D_LEAF"></a><a id="wsa_flag_multipoint_d_leaf"></a><dl>
<dt><b>WSA_FLAG_MULTIPOINT_D_LEAF</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Create a socket that will be a d_leaf in a multipoint session.

This attribute is only allowed if the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider that creates the socket supports a multipoint or multicast mechanism and the data plane for a multipoint session is non-rooted. This would be indicated by the <b>dwServiceFlags1</b> 
 member of the <b>WSAPROTOCOL_INFO</b> structure  with the <b>XP1_SUPPORT_MULTIPOINT</b> flag set and the <b>XP1_MULTIPOINT_DATA_PLANE</b>  flag not set. 

When the <i>lpProtocolInfo</i> parameter is not NULL, the  <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure for the transport provider is pointed to by the <i>lpProtocolInfo</i> parameter.  When the <i>lpProtocolInfo</i> parameter is NULL, the  <b>WSAPROTOCOL_INFO</b> structure is based on the transport provider selected by the values specified for the  <i>af</i>, <i>type</i>, and <i>protocol</i> parameters. 

Refer to 
<a href="/windows/desktop/WinSock/multipoint-and-multicast-semantics-2">Multipoint and Multicast Semantics</a> for additional information on a multipoint session.

</td>
</tr>
<tr>
<td width="40%"><a id="WSA_FLAG_ACCESS_SYSTEM_SECURITY"></a><a id="wsa_flag_access_system_security"></a><dl>
<dt><b>WSA_FLAG_ACCESS_SYSTEM_SECURITY</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Create a socket that allows the ability to set a security descriptor on the socket that contains a security access control list (SACL) as opposed to just a discretionary access control list (DACL).

SACLs are used for generating audits and alarms when an access check occurs on the object. For a socket, an access check occurs to determine whether the socket should be allowed to bind to a specific address specified to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function.

The <b>ACCESS_SYSTEM_SECURITY</b> access right controls the ability to get or set the SACL in an object's security descriptor. The system grants this access right only if the <b>SE_SECURITY_NAME</b> privilege is enabled in the access token of the requesting thread.



</td>
</tr>
<tr>
<td width="40%"><a id="WSA_FLAG_NO_HANDLE_INHERIT"></a><a id="wsa_flag_no_handle_inherit"></a><dl>
<dt><b>WSA_FLAG_NO_HANDLE_INHERIT</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
Create a socket that is non-inheritable. 

A socket handle created by the <b>WSASocket</b> or the <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function is inheritable by default. When this flag is set, the socket handle is non-inheritable. 

The <a href="/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation">GetHandleInformation</a> function can be used to determine if a socket handle was created with the <b>WSA_FLAG_NO_HANDLE_INHERIT</b> flag set. The <b>GetHandleInformation</b> function will return that the <b>HANDLE_FLAG_INHERIT</b> value is set.

This flag is supported on Windows 7 with SP1,  Windows Server 2008 R2 with SP1, and later 

</td>
</tr>
</table>
 

<div class="alert"><b>Important</b>  For multipoint sockets, only one of <b>WSA_FLAG_MULTIPOINT_C_ROOT</b> or <b>WSA_FLAG_MULTIPOINT_C_LEAF</b> flags can be specified, and only  one of <b>WSA_FLAG_MULTIPOINT_D_ROOT</b> or <b>WSA_FLAG_MULTIPOINT_D_LEAF</b> flags can be specified. Refer to 
<a href="/windows/desktop/WinSock/multipoint-and-multicast-semantics-2">Multipoint and Multicast Semantics</a> for additional information.</div>
<div> </div>

## -returns

If no error occurs, 
<b>WSASocket</b> returns a descriptor referencing the new socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<div class="alert"><b>Note</b>  This error code description is Microsoft-specific.</div>
<div> </div>
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
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProtocolInfo</i> parameter is not in a valid part of the process address space.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
This value is true for any of the following conditions. 




<ul>
<li>The parameter <i>g</i> specified is not valid.</li>
<li>The 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure that <i>lpProtocolInfo</i> points to is incomplete, the contents are invalid or the 
<b>WSAPROTOCOL_INFO</b> structure has already been used in an earlier duplicate socket operation.</li>
<li>The values specified for members of the socket triple &lt;<i>af</i>, <i>type</i>, and <i>protocol</i>&gt; are individually supported, but the given combination is not.</li>
</ul>
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
<b>WSASocket</b> function causes a socket descriptor and any related resources to be allocated and associated with a transport-service provider. Most sockets should be created with the <b>WSA_FLAG_OVERLAPPED</b> attribute set in the <i>dwFlags</i> parameter. A socket created with this attribute supports the use of overlapped I/O operations which provide higher performance. By default, a socket created with the <b>WSASocket</b> function will not have this overlapped attribute set. In contrast, the <a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> function creates a socket that supports overlapped I/O operations as the default behavior.

If the <i>lpProtocolInfo</i> parameter is <b>NULL</b>, Winsock will utilize the first available transport-service provider that supports the requested combination of address family, socket type and protocol specified in the <i>af</i>, <i>type</i>, and <i>protocol</i> parameters.

If the <i>lpProtocolInfo</i> parameter is not <b>NULL</b>, the socket will be bound to the provider associated with the indicated 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure. In this instance, the application can supply the manifest constant <b>FROM_PROTOCOL_INFO</b> as the value for any of <i>af</i>, <i>type</i>, or <i>protocol</i> parameters. This indicates that the corresponding values from the indicated 
<b>WSAPROTOCOL_INFO</b> structure (<b>iAddressFamily</b>, <b>iSocketType</b>, <b>iProtocol</b>) are to be assumed. In any case, the values specified for <i>af</i>, <i>type</i>, and <i>protocol</i> are passed unmodified to the transport-service provider.

When selecting a protocol and its supporting service provider based on <i>af</i>, <i>type</i>, and <i>protocol</i>, this procedure will only choose a base protocol or a protocol chain, not a protocol layer by itself. Unchained protocol layers are not considered to have partial matches on <i>type</i> or <i>af</i>, either. That is, they do not lead to an error code of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a> or 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTONOSUPPORT</a>, if no suitable protocol is found.

<div class="alert"><b>Note</b>  The manifest constant <b>AF_UNSPEC</b> continues to be defined in the header file but its use is strongly discouraged, as this can cause ambiguity in interpreting the value of the <i>protocol</i> parameter.</div>
<div> </div>
Applications are encouraged to use <b>AF_INET6</b> for the <i>af</i> parameter and create a dual-mode socket that can be used with both IPv4 and IPv6.

If a socket is created using the <b>WSASocket</b> function, then the <i>dwFlags</i> parameter must have the <b>WSA_FLAG_OVERLAPPED</b> attribute set for the <b>SO_RCVTIMEO</b> or <b>SO_SNDTIMEO</b> socket options to function properly. Otherwise the timeout never takes effect on the socket.

Connection-oriented sockets such as <b>SOCK_STREAM</b> provide full-duplex connections, and must be in a connected state before any data can be sent or received on them. A connection to  a specified socket is established with a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> function call. Once connected, data can be transferred using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> calls. When a session has been completed, the <a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> function should be called to release the resources associated with the socket. For connection-oriented sockets, the <a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> function should be called to stop data transfer on the socket before calling the <b>closesocket</b> function.

The communications protocols used to implement a reliable, connection-oriented socket ensure that data is not lost or duplicated. If data for which the peer protocol has buffer space cannot be successfully transmitted within a reasonable length of time, the connection is considered broken and subsequent calls will fail with the error code set to 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>.

Connectionless, message-oriented sockets allow sending and receiving of datagrams to and from arbitrary peers using 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>. If such a socket is connected to a specific peer, datagrams can be sent to that peer using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> and can be received from (only) this peer using 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>/<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>.

Support for sockets with type <b>SOCK_RAW</b> is not required, but service providers are encouraged to support raw sockets whenever possible.

The <b>WSASocket</b> function can be used to create a socket to be used by a service so that if another socket tries to bind to the same port used by the service, and audit record is generated. To enable this option, an application would need to do the following:


<ul>
<li>Call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function to enable the <b>SE_SECURITY_NAME</b> privilege in the access token for the process. This privilege is required to set the  <b>ACCESS_SYSTEM_SECURITY</b> access rights on the security descriptor for an object. </li>
<li>Call the <b>WSASocket</b> function to create a socket with <i>dwFlag</i> with the <b>WSA_FLAG_ACCESS_SYSTEM_SECURITY</b> option set. The <b>WSASocket</b> function will fail if the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function is not called first to enable the <b>SE_SECURITY_NAME</b> privilege needed for this operation.</li>
<li>Call the <a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a> function to set a security descriptor with a System Access Control List (SACL) on the socket. The socket handle returned by the <b>WSASocket</b> function is passed in the <i>handle</i> parameter. If the function succeeds, this will set the <b>ACCESS_SYSTEM_SECURITY</b> access right on the security descriptor for the socket.</li>
<li>Call the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function to bind the socket to a specific port. If the <b>bind</b> function succeeds, then an audit entry is generated if another socket tries to bind to the same port. </li>
<li>Call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function to remove the <b>SE_SECURITY_NAME</b> privilege in the access token for the process, since this is no longer needed. </li>
</ul>


For more information on <b>ACCESS_SYSTEM_SECURITY</b>, see <a href="/windows/desktop/SecAuthZ/sacl-access-right">SACL Access Right</a> and <a href="/windows/desktop/SecAuthZ/audit-generation">Audit Generation</a> in the Authorization documentation.


<h3><a id="Socket_Groups"></a><a id="socket_groups"></a><a id="SOCKET_GROUPS"></a>Socket Groups</h3>
WinSock 2 introduced the notion of a socket group as a means for an application, or cooperating set of applications, to indicate to an underlying service provider that a particular set of sockets are related and that the group thus formed has certain attributes.  Group attributes include relative priorities of the individual sockets within the group and a group quality of service specification. 

Applications that need to exchange multimedia streams over the network are an example where being able to establish a specific relationship among a set of sockets could be beneficial.  It is up to the transport on how to treat socket groups. 

The <b>WSASocket</b> and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaccept">WSAAccept</a> functions can be used to explicitly create and join a socket group when creating a new socket.  The socket group ID for a socket can be retrieved by using the <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function with <i>level</i> parameter set to <a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET</a> and the <i>optname</i> parameter set to <b>SO_GROUP_ID</b>.  A socket group
    and its associated socket group ID remain valid until the last socket belonging to this
    socket group is closed. Socket group IDs are unique across all processes
    for a given service provider. A socket group of zero indicates that the socket is not member of a socket group.

The relative group priority of  a socket group can be accessed by using the <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function with the <i>level</i> parameter set to <a href="/windows/desktop/WinSock/sol-socket-socket-options">SOL_SOCKET</a> and the <i>optname</i> parameter set to <b>SO_GROUP_PRIORITY</b>. The relative group priority of  a socket group can be set by using <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> with the <i>level</i> parameter set to SOL_SOCKET and the <i>optname</i> parameter set to <b>SO_GROUP_PRIORITY</b>. 

The Winsock provider included with Windows allows the creation of socket groups and it enforces the SG_CONSTRAINED_GROUP. All sockets in a constrained socket group must be created with the same value for the <i>type</i> and <i>protocol</i> parameters. A constrained socket group may consist only of connection-oriented sockets, and requires that connections on all grouped sockets be to the same address on the same host.  This is the only restriction applied to a socket group by the Winsock provider included with Windows. The socket group priority is not currently used by the Winsock provider or the TCP/IP stack included with Windows. 

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>WSASocket</b> function.


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
    DWORD dwFlags = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %s <addressfamily> <type> <protocol> <flags>\n", argv[0]);
        wprintf(L"       opens a socket for the specified family, type, protocol, and flags\n");
        wprintf(L"       flags value must be in decimal, not hex\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 1\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17 OVERLAPPED\n", argv[0]);
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);
    dwFlags = _wtoi(argv[4]);
    
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

    wprintf(L"  Flags = ");
    if (dwFlags & WSA_FLAG_OVERLAPPED)
        wprintf(L"  WSA_FLAG_OVERLAPPED");
    if (dwFlags & WSA_FLAG_MULTIPOINT_C_ROOT)
        wprintf(L"  WSA_FLAG_MULTIPOINT_C_ROOT");
    if (dwFlags & WSA_FLAG_MULTIPOINT_C_LEAF)
        wprintf(L"  WSA_FLAG_MULTIPOINT_C_LEAF");
    if (dwFlags & WSA_FLAG_MULTIPOINT_D_ROOT)
        wprintf(L"  WSA_FLAG_MULTIPOINT_D_ROOT");
    if (dwFlags & WSA_FLAG_MULTIPOINT_D_LEAF)
        wprintf(L"  WSA_FLAG_MULTIPOINT_D_LEAF");
    if (dwFlags & WSA_FLAG_ACCESS_SYSTEM_SECURITY)
        wprintf(L"  WSA_FLAG_ACCESS_SYSTEM_SECURITY");
#ifdef WSA_FLAG_NO_HANDLE_INHERIT 
    if (dwFlags & WSA_FLAG_NO_HANDLE_INHERIT)
        wprintf(L"  WSA_FLAG_NO_HANDLE_INHERIT");
#endif
    wprintf(L" (0x%x)\n" , dwFlags);

    sock = WSASocket(iFamily, iType, iProtocol, NULL, 0, dwFlags);
    if (sock == INVALID_SOCKET) 
        wprintf(L"WSASocket function failed with error = %d\n", WSAGetLastError() );
    else {
        wprintf(L"WSASocket function succeeded\n");

        // Close the socket to release the resources associated
        // Normally an application calls shutdown() before closesocket 
        //   to  disables sends or receives on a socket first
        // This isn't needed in this simple sample
        iResult = closesocket(sock);
        if (iResult == SOCKET_ERROR) {
            wprintf(L"closesocket function zfailed with error = %d\n", WSAGetLastError() );
            WSACleanup();
            return 1;
        }    
    }
    WSACleanup();

    return 0;
}


```




<b>Windows Phone 8:</b> The <b>WSASocketW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSASocketW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSASocket as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



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



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
