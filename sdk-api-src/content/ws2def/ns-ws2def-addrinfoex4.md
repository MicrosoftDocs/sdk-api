---
UID: NS:ws2def.addrinfoex4
title: ADDRINFOEX4 (ws2def.h)
description: Used by the GetAddrInfoEx function to hold host address information when a specific network interface has been requested. (addrinfoex4W)
helpviewer_keywords: ["*LPADDRINFOEX4","*PADDRINFOEX4","ADDRINFOEX4","AF_BTH","AF_INET","AF_INET6","AF_IRDA","AF_NETBIOS","AF_UNSPEC","AI_ADDRCONFIG","AI_ALL","AI_CANONNAME","AI_DISABLE_IDN_ENCODING","AI_EXTENDED","AI_FILESERVER","AI_FQDN","AI_NON_AUTHORITATIVE","AI_NUMERICHOST","AI_PASSIVE","AI_RESOLUTION_HANDLE","AI_RETURN_PREFERRED_NAMES","AI_SECURE","AI_V4MAPPED","IPPROTO_RM","IPPROTO_TCP","IPPROTO_UDP","LPaddrinfoex4","LPaddrinfoex4 structure pointer [Winsock]","Paddrinfoex4","Paddrinfoex4 structure pointer [Winsock]","SOCK_DGRAM","SOCK_RAW","SOCK_RDM","SOCK_SEQPACKET","SOCK_STREAM","addrinfoex4","addrinfoex4 structure [Winsock]","addrinfoex4A","addrinfoex4W","winsock.addrinfoex4","ws2def/LPaddrinfoex4","ws2def/Paddrinfoex4","ws2def/addrinfoex4","ws2def/addrinfoex4A","ws2def/addrinfoex4W"]
old-location: winsock\addrinfoex4.htm
tech.root: WinSock
ms.assetid: 96B19008-9F20-4F47-A0F1-AA695227725B
ms.date: 12/05/2018
ms.keywords: '*LPADDRINFOEX4, *PADDRINFOEX4, ADDRINFOEX4, AF_BTH, AF_INET, AF_INET6, AF_IRDA, AF_NETBIOS, AF_UNSPEC, AI_ADDRCONFIG, AI_ALL, AI_CANONNAME, AI_DISABLE_IDN_ENCODING, AI_EXTENDED, AI_FILESERVER, AI_FQDN, AI_NON_AUTHORITATIVE, AI_NUMERICHOST, AI_PASSIVE, AI_RESOLUTION_HANDLE, AI_RETURN_PREFERRED_NAMES, AI_SECURE, AI_V4MAPPED, IPPROTO_RM, IPPROTO_TCP, IPPROTO_UDP, LPaddrinfoex4, LPaddrinfoex4 structure pointer [Winsock], Paddrinfoex4, Paddrinfoex4 structure pointer [Winsock], SOCK_DGRAM, SOCK_RAW, SOCK_RDM, SOCK_SEQPACKET, SOCK_STREAM, addrinfoex4, addrinfoex4 structure [Winsock], addrinfoex4A, addrinfoex4W, winsock.addrinfoex4, ws2def/LPaddrinfoex4, ws2def/Paddrinfoex4, ws2def/addrinfoex4, ws2def/addrinfoex4A, ws2def/addrinfoex4W'
req.header: ws2def.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: addrinfoex4W (Unicode) and addrinfoex4A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADDRINFOEX4, *PADDRINFOEX4, *LPADDRINFOEX4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - addrinfoex4
 - ws2def/addrinfoex4
 - PADDRINFOEX4
 - ws2def/PADDRINFOEX4
 - ADDRINFOEX4
 - ws2def/ADDRINFOEX4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
api_name:
 - addrinfoex4
 - addrinfoex4A
 - addrinfoex4W
---

# ADDRINFOEX4 structure


## -description

The 
<b>addrinfoex4</b> structure is used by the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function to hold host address information when a specific network interface has been requested.

## -struct-fields

### -field ai_flags

Flags that indicate options used in the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function. 


Supported values for the <b>ai_flags</b> member are defined in the <i>Winsock2.h</i> include file and can be a combination of the following options.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AI_PASSIVE"></a><a id="ai_passive"></a><dl>
<dt><b>AI_PASSIVE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The socket address will be used in a call to the <a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_CANONNAME"></a><a id="ai_canonname"></a><dl>
<dt><b>AI_CANONNAME</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The canonical name is returned in the first <b>ai_canonname</b> member.


</td>
</tr>
<tr>
<td width="40%"><a id="AI_NUMERICHOST"></a><a id="ai_numerichost"></a><dl>
<dt><b>AI_NUMERICHOST</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
The <i>nodename</i> parameter passed to the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function must be a numeric string.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_ALL"></a><a id="ai_all"></a><dl>
<dt><b>AI_ALL</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
If this bit is set, a request is made for IPv6 addresses and IPv4 addresses with <b>AI_V4MAPPED</b>.

 This option is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_ADDRCONFIG"></a><a id="ai_addrconfig"></a><dl>
<dt><b>AI_ADDRCONFIG</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> will resolve only if a global address is configured. The IPv6 and IPv4 loopback address is not considered a valid global address. 

This option is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_V4MAPPED"></a><a id="ai_v4mapped"></a><dl>
<dt><b>AI_V4MAPPED</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
If the  <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> request for an IPv6 addresses fails, a name service request is made for IPv4 addresses and these addresses are converted to IPv4-mapped IPv6 address format.

This option is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_NON_AUTHORITATIVE"></a><a id="ai_non_authoritative"></a><dl>
<dt><b>AI_NON_AUTHORITATIVE</b></dt>
<dt>0x04000</dt>
</dl>
</td>
<td width="60%">
The address information is from non-authoritative results. 

When this option is set in the <i>pHints</i> parameter of <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>, the <b>NS_EMAIL</b> namespace provider returns both authoritative and non-authoritative results. If this option is not set, then only authoritative results are returned. 

This option is only supported on Windows Vista and later for the <b>NS_EMAIL</b> namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_SECURE"></a><a id="ai_secure"></a><dl>
<dt><b>AI_SECURE</b></dt>
<dt>0x08000</dt>
</dl>
</td>
<td width="60%">
The address information is from a secure channel. 

If the  <b>AI_SECURE</b> bit is set, the <b>NS_EMAIL</b> namespace provider will return results that were obtained with enhanced security to minimize possible spoofing. 

When this option is set in the <i>pHints</i> parameter of <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>, the <b>NS_EMAIL</b> namespace provider returns only results that were obtained with enhanced security to minimize possible spoofing. 

This option is only supported on Windows Vista and later for the <b>NS_EMAIL</b> namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_RETURN_PREFERRED_NAMES"></a><a id="ai_return_preferred_names"></a><dl>
<dt><b>AI_RETURN_PREFERRED_NAMES</b></dt>
<dt>0x010000</dt>
</dl>
</td>
<td width="60%">
The address information is for a preferred names for publication with a specific namespace. 

When this option is set in the <i>pHints</i> parameter of <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>, no name should be provided in the <i>pName</i> parameter and the <b>NS_EMAIL</b> namespace provider will return preferred names for publication.

This option is only supported on Windows Vista and later for the <b>NS_EMAIL</b> namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_FQDN"></a><a id="ai_fqdn"></a><dl>
<dt><b>AI_FQDN</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The fully qualified domain name is returned in the first <b>ai_fqdn</b> member.


When this option is set in the <i>pHints</i> parameter of <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> and a flat name (single label) is specified in the <i>pName</i> parameter,  the fully qualified domain name that the name eventually resolved to will be returned.

This option is supported on Windows 7,  Windows Server 2008 R2,   and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_FILESERVER"></a><a id="ai_fileserver"></a><dl>
<dt><b>AI_FILESERVER</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
A  hint to the namespace provider that the hostname being queried is being used in a file share scenario. The namespace provider may ignore this hint.


This option is supported on Windows 7,  Windows Server 2008 R2,   and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_DISABLE_IDN_ENCODING"></a><a id="ai_disable_idn_encoding"></a><dl>
<dt><b>AI_DISABLE_IDN_ENCODING</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Disable the automatic International Domain Name encoding using Punycode in the name resolution functions called by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function. 

This option is supported on Windows 8, Windows Server 2012,   and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_EXTENDED"></a><a id="ai_extended"></a><dl>
<dt><b>AI_EXTENDED</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Indicates that the current object is extended: that is, an <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoex2w">addrinfoex2</a> or greater.

This option is supported on Windows 8.1, Windows Server 2012 R2,   and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_RESOLUTION_HANDLE"></a><a id="ai_resolution_handle"></a><dl>
<dt><b>AI_RESOLUTION_HANDLE</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
A resolution handle is returned in the <b>ai_resolutionhandle</b> member.

This option is supported on Windows 10, Windows Server 2016,   and later.

</td>
</tr>
</table>

### -field ai_family

The address family. 

The possible values for the address family are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b> or <b>AF_INET6</b>, which are the Internet
                     address family formats for IPv4 and IPv6. Other options for address family (<b>AF_NETBIOS</b> for use with NetBIOS, for example) are supported if a Windows Sockets service provider for the address family is installed. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

The table below lists common values for the address family although many other values are possible. 

<table>
<tr>
<th>Value</th>
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
<td width="40%"><a id="AF_NETBIOS"></a><a id="af_netbios"></a><dl>
<dt><b>AF_NETBIOS</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The NetBIOS address family. This address family is only supported if a Windows Sockets provider for NetBIOS is installed.

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
The Infrared Data Association (IrDA) address family. This address family is only supported if the computer has an infrared port and driver installed. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_BTH"></a><a id="af_bth"></a><dl>
<dt><b>AF_BTH</b></dt>
<dt>32</dt>
</dl>
</td>
<td width="60%">
The Bluetooth address family. This address family is only supported if a Bluetooth adapter is installed.

</td>
</tr>
</table>

### -field ai_socktype

The socket type. Possible values for the socket type are defined in the <i>Winsock2.h</i> include file.

The following table lists the possible values for the socket type supported for Windows Sockets 2:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SOCK_STREAM"></a><a id="sock_stream"></a><dl>
<dt><b>SOCK_STREAM</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Provides sequenced, reliable, two-way, connection-based byte streams with an OOB data transmission mechanism. Uses the Transmission Control Protocol (TCP) for the Internet address family (<b>AF_INET</b> or <b>AF_INET6</b>). If the <b>ai_family</b> member is <b>AF_IRDA</b>, then <b>SOCK_STREAM</b> is the only supported socket type.

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_DGRAM"></a><a id="sock_dgram"></a><dl>
<dt><b>SOCK_DGRAM</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Supports datagrams, which are connectionless, unreliable buffers of a fixed (typically small) maximum length. Uses the User Datagram Protocol (UDP) for the Internet address family (<b>AF_INET</b> or <b>AF_INET6</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_RAW"></a><a id="sock_raw"></a><dl>
<dt><b>SOCK_RAW</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Provides a raw socket that allows an application to manipulate the next upper-layer protocol header. To manipulate the IPv4 header, the <a href="/windows/desktop/WinSock/ipproto-ip-socket-options">IP_HDRINCL</a> socket option must be set on the socket.  To manipulate the IPv6 header, the <a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPV6_HDRINCL</a> socket option must be set on the socket.  

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_RDM"></a><a id="sock_rdm"></a><dl>
<dt><b>SOCK_RDM</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Provides a reliable message datagram. An example of this type is the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as <a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">reliable multicast programming</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_SEQPACKET"></a><a id="sock_seqpacket"></a><dl>
<dt><b>SOCK_SEQPACKET</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Provides a pseudo-stream packet based on datagrams. 

</td>
</tr>
</table>
 

In Windows Sockets 2, new socket types were introduced. An application can dynamically discover the attributes of each available transport protocol through the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> function. So an application can determine the possible socket type and protocol options for an address family  and use this information when specifying this parameter. Socket type definitions in the <i>Winsock2.h</i> and <i>Ws2def.h</i> header files will be periodically updated as new socket types, address families, and protocols are defined.

In Windows Sockets 1.1, the only possible socket types are <b>SOCK_DATAGRAM</b> and <b>SOCK_STREAM</b>.

### -field ai_protocol

The protocol type. The possible options are specific to the address family and socket type specified. Possible values for the <b>ai_protocol</b> are defined in <i>Winsock2.h</i> and the <i>Wsrm.h</i> header files. 

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and this member can be one of the values from the <b>IPPROTO</b> enumeration type defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

If a value of  0 is specified for <b>ai_protocol</b>, the caller does not
              wish to specify a protocol and the service provider will choose the <b>ai_protocol</b> to use. For protocols other than IPv4 and IPv6, set <b>ai_protocol</b> to zero.

The following table lists common values for the <b>ai_protocol</b> member although many other values are possible.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_TCP"></a><a id="ipproto_tcp"></a><dl>
<dt><b>IPPROTO_TCP</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The Transmission Control Protocol (TCP). This is a possible value when the <b>ai_family</b> member is <b>AF_INET</b> or <b>AF_INET6</b> and the <b>ai_socktype</b> member is <b>SOCK_STREAM</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_UDP"></a><a id="ipproto_udp"></a><dl>
<dt><b>IPPROTO_UDP</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The User Datagram Protocol (UDP). This is a possible value when the <b>ai_family</b> member is <b>AF_INET</b> or <b>AF_INET6</b> and the <i>type</i> parameter is <b>SOCK_DGRAM</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="IPPROTO_RM"></a><a id="ipproto_rm"></a><dl>
<dt><b>IPPROTO_RM</b></dt>
<dt>113</dt>
</dl>
</td>
<td width="60%">
The PGM protocol for reliable multicast. This is a possible value when the <b>ai_family</b> member is <b>AF_INET</b> and the <b>ai_socktype</b> member is <b>SOCK_RDM</b>. On the Windows SDK released for Windows Vista and later,  this value is also called <b>IPPROTO_PGM</b>.

</td>
</tr>
</table>
 

If the <b>ai_family</b> member is <b>AF_IRDA</b>, then the <b>ai_protocol</b> must be 0.

### -field ai_addrlen

The length, in bytes, of the  buffer pointed to by the <b>ai_addr</b> member.

### -field ai_canonname

The canonical name for the host.

### -field ai_addr

A pointer to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure. The <b>ai_addr</b> member in each returned <b>addrinfoex4</b> structure points to a filled-in socket address structure. The length, in bytes, of each returned <b>addrinfoex4</b> structure is specified in the <b>ai_addrlen</b> member.

### -field ai_blob

A pointer to data that is used to return provider-specific namespace information that is associated with the name beyond a list of addresses. The length, in bytes, of the buffer pointed to by <b>ai_blob</b> must be specified in the <b>ai_bloblen</b> member.

### -field ai_bloblen

The length, in bytes, of the <b>ai_blob</b> member.

### -field ai_provider

A pointer to the GUID of a specific namespace provider.

### -field ai_next

A pointer to the next structure in a linked list. This parameter is set to <b>NULL</b> in the last 
<b>addrinfoex4</b> structure of a linked list.

### -field ai_version

The version number of this structure. The value currently used for this version of the structure is 4.

### -field ai_fqdn

The fully qualified domain name for the host.

### -field ai_interfaceindex

The interface index, as defined by the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>.<i>IfIndex</i> property returned in <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>.

### -field ai_resolutionhandle

Handle pointing to the fully qualified domain name for the host.

## -remarks

The 
<b>addrinfoex4</b> structure is supported on Windows 10 and Windows Server 2016

The <b>addrinfoex4</b> structure is used by the GetAddrInfoEx function to hold host address information when the <b>AI_EXTENDED</b> | <b>AI_FQDN</b> | <b>AI_CANONNAME</b> | <b>AI_RESOLUTION_HANDLE</b> bits are set in the <b>addrinfoex4</b><b>.ai_flags</b> member passed in through the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>.<i>hints</i> parameter.  

The <b>addrinfoex4</b>  structure is an enhanced version of the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a> structure that can return the canonical name, the fully qualified domain name for the host, and a handle to the fully qualified domain name. In turn, <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> is an enhanced version of the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>  and <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a> structures used with the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> and <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> functions. The <b>GetAddrInfoEx</b>  function allows specifying the namespace provider to resolve the query. For use with the IPv6 and IPv4 protocol, name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, an email provider (the <b>NS_EMAIL</b> namespace), or by other naming mechanisms.

The blob data in tha <b>ai_blob</b> member is used to return additional provider-specific namespace information associated with a name. The format of data in the <b>ai_blob</b> member is specific to a particular namespace provider. Currently, blob data is used by the <b>NS_EMAIL</b> namespace provider to supply additional information.  

When UNICODE or _UNICODE is defined, <b>addrinfoex4</b> is defined to <b>addrinfoex4W</b>, the Unicode version of this structure. The string parameters are defined to the <b>PWSTR</b> data type and the <b>addrinfoex4W</b> structure is used.

When UNICODE or _UNICODE is not defined, <b>addrinfoex4</b> is defined to <b>addrinfoex4A</b>, the ANSI version of this structure. The string parameters are of the <b>char *</b> data type and the <b>addrinfoex4A</b> structure is used.

Upon a successful call to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>, a linked list of 
<b>addrinfoex4</b> structures is returned in the <i>ppResult</i> parameter passed to the <b>GetAddrInfoEx</b> function. The list can be processed by following the pointer provided in the <b>ai_next</b> member of each returned 
<b>addrinfoex4</b> structure until a <b>NULL</b> pointer is encountered. In each returned 
<b>addrinfoex4</b> structure, the <b>ai_family</b>, <b>ai_socktype</b>, and <b>ai_protocol</b> members correspond to respective arguments in a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> function call. Also, the <b>ai_addr</b> member in each returned 
<b>addrinfoex4</b> structure points to a filled-in socket address structure, the length of which is specified in its <b>ai_addrlen</b> member.


#### Examples

The following code describes making a call to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> with an <b>addrinfoex4</b> structure to retrieve the handle to a FQDN. the sample then call <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> with the <a href="/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input">ASSOCIATE_NAMERES_CONTEXT_INPUT</a> structure.


```cpp
// 
// Connect to a server using its IPv4 addresses 
// 

VOID 
ConnectServer( 
    PCWSTR server) 
{ 
    int iResult; 
    PADDRINFOEX4 pResult = NULL; 
    ADDRINFOEX3 hints = { 0 }; 
    PADDRINFOEX4 pCur = NULL; 
    WSADATA wsaData; 
    SOCKET connectSocket = INVALID_SOCKET; 
    ULONG bytesReturned = 0; 
    ASSOCIATE_NAMERES_CONTEXT_INPUT input = { 0 }; 
    SOCKADDR_IN clientService; 
    wchar_t ipstringbuffer[46]; 
    String string; 
    DWORD dwRetval; 
    //  
    //  Initialize Winsock 
    // 
    iResult = WSAStartup( 
        MAKEWORD(2, 2),  
        &wsaData); 
    if (iResult != 0) { 
        printf("WSAStartup failed: %d\n", iResult); 
        goto Exit; 
    } 

    //  
    // Create a SOCKET for connection 
    // 
    connectSocket = socket( 
        AF_UNSPEC,  
        SOCK_STREAM,  
        IPPROTO_TCP); 
    if (connectSocket == INVALID_SOCKET)  
    { 
        printf("socket failed: %d\n", WSAGetLastError()); 
        goto Exit; 
    } 

    // 
    // Do name resolution 
    // 

    hints.ai_family = AF_INET; 
    hints.ai_socktype = SOCK_STREAM; 
    hints.ai_flags = AI_EXTENDED | AI_FQDN | AI_CANONNAME | AI_RESOLUTION_HANDLE; 
    hints.ai_version = ADDRINFOEX_VERSION_4; 

    dwRetval = GetAddrInfoExW( 
        server, 
        NULL, 
        NS_DNS, 
        NULL, 
        (const ADDRINFOEXW*)&hints, 
        (PADDRINFOEXW*)&pResult, 
        NULL, 
        NULL, 
        NULL, NULL); 
    if (dwRetval != 0) { 
        printf("GetAddrInfoEx failed with error: %d\n", dwRetval); 
        goto Exit; 
    } 
    input.TransportSettingId.Guid = ASSOCIATE_NAMERES_CONTEXT; 
    input.Handle = pResult->ai_resolutionhandle; 

    // 
    // Associate socket with the handle 
    // 

    if (WSAIoctl( 
            connectSocket, 
            SIO_APPLY_TRANSPORT_SETTING, 
            (VOID *)&input, 
            sizeof(input), 
            NULL, 
            0, 
            &bytesReturned, 
            NULL, 
            NULL) == SOCKET_ERROR) 
    if (iResult != 0){ 
        printf("WSAIoctl failed: %d\n", WSAGetLastError()); 
        goto Exit; 
    }     

    // 
    // Connect to server 
    // 

    pCur = pResult; 
    while (pCur != NULL) 
    { 
        if (pCur->ai_addr->sa_family == AF_INET) 
        { 
            clientService = *(const sockaddr_in*)pCur->ai_addr; 
            clientService.sin_port = htons(80); 
            if (connect( 
                connectSocket, 
                (const SOCKADDR *)&clientService, 
                sizeof(clientService)) == SOCKET_ERROR) 
            { 
                printf("connect failed: %d\n", WSAGetLastError()); 
                goto Exit; 
            } 
        } 
        pCur = pCur->ai_next; 
    } 

Exit: 

    if (connectSocket != INVALID_SOCKET) 
    { 
        closesocket(connectSocket); 
    } 
    if (pResult) 
    { 
        FreeAddrInfoExW((ADDRINFOEXW*)pResult); 
    } 
    WSACleanup(); 
    return; 
} 

```

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfow">addrinfoW</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoex3">addrinfoex3</a>
