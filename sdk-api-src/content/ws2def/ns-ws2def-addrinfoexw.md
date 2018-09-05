---
UID: NS:ws2def.addrinfoexW
title: addrinfoexW
author: windows-sdk-content
description: Used by the GetAddrInfoEx function to hold host address information.
old-location: winsock\addrinfoex.htm
old-project: WinSock
ms.assetid: 1077e03d-a1a4-45ab-a5d2-29a67e03f5df
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPADDRINFOEXW, *PADDRINFOEXW, ADDRINFOEX, ADDRINFOEX structure [Winsock], ADDRINFOEXW, AF_BTH, AF_INET, AF_INET6, AF_IRDA, AF_NETBIOS, AF_UNSPEC, AI_ADDRCONFIG, AI_ALL, AI_CANONNAME, AI_DISABLE_IDN_ENCODING, AI_FILESERVER, AI_FQDN, AI_NON_AUTHORITATIVE, AI_NUMERICHOST, AI_PASSIVE, AI_RETURN_PREFERRED_NAMES, AI_SECURE, AI_V4MAPPED, IPPROTO_RM, IPPROTO_TCP, IPPROTO_UDP, PADDRINFOEX, PADDRINFOEX structure pointer [Winsock], SOCK_DGRAM, SOCK_RAW, SOCK_RDM, SOCK_SEQPACKET, SOCK_STREAM, addrinfoex, addrinfoex structure [Winsock], addrinfoexA, addrinfoexW, winsock.addrinfoex, ws2def/ADDRINFOEX, ws2def/PADDRINFOEX, ws2def/addrinfoexA, ws2def/addrinfoexW, ws2tcpip/ADDRINFOEX, ws2tcpip/PADDRINFOEX, ws2tcpip/addrinfoexA, ws2tcpip/addrinfoexW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: Windows Server 2012, Windows 7  Windows Server 2008 R2
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: addrinfoexW (Unicode) and addrinfoexA (ANSI)
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADDRINFOEXW, *PADDRINFOEXW, *LPADDRINFOEXW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
 - Ws2tcpip.h
api_name:
 - ADDRINFOEX
 - addrinfoexA
 - addrinfoexW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# addrinfoexW structure


## -description


The 
<b>addrinfoex</b> structure is used by the 
<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function to hold host address information.


## -struct-fields




### -field ai_flags

Type: <b>int</b>

Flags that indicate options used in the 
<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function. 


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
The socket address will be used in a call to the <a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>function.

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


When both the <b>AI_CANONNAME</b> and <b>AI_FQDN</b> bits are set, an <a href="https://msdn.microsoft.com/9CB33347-A838-473D-B5CD-1149D6632CF2">addrinfoex2</a> structure is returned not the <b>addrinfoex</b> structure. 

</td>
</tr>
<tr>
<td width="40%"><a id="AI_NUMERICHOST"></a><a id="ai_numerichost"></a><dl>
<dt><b>AI_NUMERICHOST</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
The <i>nodename</i> parameter passed to the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function must be a numeric string.

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
The <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> will resolve only if a global address is configured. The IPv6 and IPv4 loopback address is not considered a valid global address. 

This option is only supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_V4MAPPED"></a><a id="ai_v4mapped"></a><dl>
<dt><b>AI_V4MAPPED</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
If the  <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> request for an IPv6 addresses fails, a name service request is made for IPv4 addresses and these addresses are converted to IPv4-mapped IPv6 address format.

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

When this option is set in the <i>pHints</i> parameter of <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, the <b>NS_EMAIL</b> namespace provider returns both authoritative and non-authoritative results. If this option is not set, then only authoritative results are returned. 

In the  <i>ppResults</i> parameter returned by <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, this flag is set in the <b>ai_flags</b> member of the <b>addrinfoex</b> structure for non-authoritative results.  

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
The address information is from a secure channel. If the  <b>AI_SECURE</b> bit is set, the <b>NS_EMAIL</b> namespace provider will return results that were obtained with enhanced security to minimize possible spoofing. 

When this option is set in the <i>pHints</i> parameter of <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, the <b>NS_EMAIL</b> namespace provider returns only results that were obtained with enhanced security to minimize possible spoofing. 

In the  <i>ppResults</i> parameter returned by <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, this flag is set in the <b>ai_flags</b> member of the <b>addrinfoex</b> structure for results returned with enhanced security to minimize possible spoofing.  

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

When this option is set in the <i>pHints</i> parameter of <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, no name should be provided in the <i>pName</i> parameter and the <b>NS_EMAIL</b> namespace provider will return preferred names for publication.

In the  <i>ppResults</i> parameter returned by <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, this flag is set in the <b>ai_flags</b> member of the <b>addrinfoex</b> structure for results returned for preferred names for publication.  

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
The fully qualified domain name is returned in the first <b>ai_canonicalname</b> member.


When this option is set in the <i>pHints</i> parameter of <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> and a flat name (single label) is specified in the <i>pName</i> parameter,  the fully qualified domain name that the name eventually resolved to will be returned.

When both the <b>AI_CANONNAME</b> and <b>AI_FQDN</b> bits are set, an <a href="https://msdn.microsoft.com/9CB33347-A838-473D-B5CD-1149D6632CF2">addrinfoex2</a> structure is returned not the <b>addrinfoex</b> structure. 

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


This option is supported on Windows 7, Windows Server 2008 R2,  and later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_DISABLE_IDN_ENCODING"></a><a id="ai_disable_idn_encoding"></a><dl>
<dt><b>AI_DISABLE_IDN_ENCODING</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Disable the automatic International Domain Name encoding using Punycode in the name resolution functions called by the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function. 

This option is supported on Windows 8, Windows Server 2012,   and later.

</td>
</tr>
</table>
 


### -field ai_family

Type: <b>int</b>

The address family. Possible values for the address family are defined in the <i>Winsock2.h</i> include file. 

On the Windows SDK released for Windows Vista and later,, the organization of header files has changed and the possible values for the address family are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b> or <b>AF_INET6</b>, which are the Internet
                     address family formats for IPv4 and IPv6. Other options for address family (<b>AF_NETBIOS</b> for use with NetBIOS, for example) are supported if a Windows Sockets service provider for the address family is installed. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_UNSPEC</b> and <b>PF_UNSPEC</b>), so either constant can be used.

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
The Bluetooth address family. This address family is only supported if a Bluetooth adapter is installed on Windows Server 2003 or later.

</td>
</tr>
</table>
 


### -field ai_socktype

Type: <b>int</b>

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
Provides a raw socket that allows an application to manipulate the next upper-layer protocol header. To manipulate the IPv4 header, the <a href="https://msdn.microsoft.com/6b06a29e-59cd-4446-bd2f-131dc25bf571">IP_HDRINCL</a> socket option must be set on the socket.  To manipulate the IPv6 header, the <a href="https://msdn.microsoft.com/65f8f7a4-757b-43a3-9d47-b115754c89d6">IPV6_HDRINCL</a> socket option must be set on the socket.  

</td>
</tr>
<tr>
<td width="40%"><a id="SOCK_RDM"></a><a id="sock_rdm"></a><dl>
<dt><b>SOCK_RDM</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Provides a reliable message datagram. An example of this type is the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as <a href="https://msdn.microsoft.com/81c203ed-739f-4a06-99a1-9a99c6164edc">reliable multicast programming</a>. 

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
<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a> function. So an application can determine the possible socket type and protocol options for an address family  and use this information when specifying this parameter. Socket type definitions in the <i>Winsock2.h</i> and <i>Ws2def.h</i> header files will be periodically updated as new socket types, address families, and protocols are defined.

In Windows Sockets 1.1, the only possible socket types are <b>SOCK_DATAGRAM</b> and <b>SOCK_STREAM</b>. 


### -field ai_protocol

Type: <b>int</b>

The protocol type. The possible options are specific to the address family and socket type specified. Possible values for the <b>ai_protocol</b> are defined in <i>Winsock2.h</i> and the <i>Wsrm.h</i> header files. 

On the Windows SDK released for Windows Vista and later,, the organization of header files has changed and this member can be one of the values from the <b>IPPROTO</b> enumeration type defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

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

Type: <b>size_t</b>

The length, in bytes, of the  buffer pointed to by the <b>ai_addr</b> member.


### -field ai_canonname

Type: <b>PCTSTR</b>

The canonical name for the host.


### -field ai_addr

Type: <b>struct sockaddr*</b>

A pointer to a 
<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure. The <b>ai_addr</b> member in each returned <b>addrinfoex</b> structure points to a filled-in socket address structure. The length, in bytes, of each returned <b>addrinfoex</b> structure is specified in the <b>ai_addrlen</b> member.


### -field ai_blob

Type: <b>void*</b>

A pointer to data that is used to return provider-specific namespace information that is associated with the name beyond a list of addresses. The length, in bytes, of the buffer pointed to by <b>ai_blob</b> must be specified in the <b>ai_bloblen</b> member.


### -field ai_bloblen

Type: <b>size_t</b>

The length, in bytes, of the <b>ai_blob</b> member.


### -field ai_provider

Type: <b>LPGUID</b>

A pointer to the GUID of a specific namespace provider.


### -field ai_next

Type: <b>struct addrinfoex*</b>

A pointer to the next structure in a linked list. This parameter is set to <b>NULL</b> in the last 
<b>addrinfoex</b> structure of a linked list.


## -remarks



The 
<b>addrinfoex</b> structure is used by the 
<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function to hold host address information. The <b>addrinfoex</b>  structure is an enhanced version of the <a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a> and <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structures. The extra structure members are for blob data and the GUID for the namespace provider. The blob data is used to return additional provider-specific namespace information associated with a name. The format of data in the <b>ai_blob</b> member is specific to a particular namespace provider. Currently, blob data is used by the <b>NS_EMAIL</b> namespace provider to supply additional information.  

The <b>addrinfoex</b>  structure is an enhanced version of the <a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a> and <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structure used with <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>  function. The <b>GetAddrInfoEx</b>  function allows specifying the namespace provider to resolve the query. For use with the IPv6 and IPv4 protocol, name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, an email provider (the <b>NS_EMAIL</b> namespace), or by other naming mechanisms. 

When UNICODE or _UNICODE is defined, <b>addrinfoex</b> is defined to <b>addrinfoexW</b>, the Unicode version of this structure. The string parameters are defined to the <b>PWSTR</b> data type and the <b>addrinfoexW</b> structure is used.

When UNICODE or _UNICODE is not defined, <b>addrinfoex</b> is defined to <b>addrinfoexA</b>, the ANSI version of this structure. The string parameters are of the <b>PCSTR</b> data type and the <b>addrinfoexA</b> structure is used.

Upon a successful call to <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, a linked list of 
<b>addrinfoex</b> structures is returned in the <i>ppResult</i> parameter passed to the <b>GetAddrInfoEx</b> function. The list can be processed by following the pointer provided in the <b>ai_next</b> member of each returned 
<b>addrinfoex</b> structure until a <b>NULL</b> pointer is encountered. In each returned 
<b>addrinfoex</b> structure, the <b>ai_family</b>, <b>ai_socktype</b>, and <b>ai_protocol</b> members correspond to respective arguments in a 
<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> or <a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> function call. Also, the <b>ai_addr</b> member in each returned 
<b>addrinfoex</b> structure points to a filled-in socket address structure, the length of which is specified in its <b>ai_addrlen</b> member.


#### Examples

The following example demonstrates the use of the <b>addrinfoex</b> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;windows.h&gt;
#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;stdio.h&gt;

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
//--------------------------------
// Declare and initialize variables.
    WSADATA wsaData;
    int iResult;

    ADDRINFOEX *result = NULL;
    ADDRINFOEX *ptr = NULL;
    ADDRINFOEX hints;

    DWORD dwRetval = 0;
    int i = 1;

    DWORD dwNamespace = NS_DNS;
    LPGUID lpNspid = NULL;

    struct sockaddr_in *sockaddr_ipv4;
    struct sockaddr_in6 *sockaddr_ipv6;
//    LPSOCKADDR sockaddr_ip;

    wchar_t ipstringbuffer[46];

    // Validate the parameters
    if (argc != 3) {
        wprintf(L"usage: %ws &lt;hostname&gt; &lt;servicename&gt;\n", argv[0]);
        wprintf(L"       provides protocol-independent translation\n");
        wprintf(L"       from a host name to an IP address\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws www.contoso.com 0\n", argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &amp;wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }
//--------------------------------
// Setup the hints address info structure
// which is passed to the GetAddrInfoW() function
    memset(&amp;hints, 0, sizeof (hints));
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    wprintf(L"Calling GetAddrInfoEx with following parameters:\n");
    wprintf(L"\tName = %ws\n", argv[1]);
    wprintf(L"\tServiceName (or port) = %ws\n\n", argv[2]);

//--------------------------------
// Call GetAddrInfoEx(). If the call succeeds,
// the aiList variable will hold a linked list
// of ADDRINFOEX structures containing response
// information about the host
    dwRetval = GetAddrInfoEx(argv[1], argv[2],
                             dwNamespace, lpNspid, &amp;hints, &amp;result,
                             NULL, NULL, NULL, NULL);

    if (dwRetval != 0) {
        wprintf(L"GetAddrInfoEx failed with error: %d\n", dwRetval);
        WSACleanup();
        return 1;
    }
    wprintf(L"GetAddrInfoEx returned success\n");

    // Retrieve each address and print out the hex bytes
    for (ptr = result; ptr != NULL; ptr = ptr-&gt;ai_next) {

        wprintf(L"GetAddrInfoEx response %d\n", i++);
        wprintf(L"\tFlags: 0x%x\n", ptr-&gt;ai_flags);
        wprintf(L"\tFamily: ");
        switch (ptr-&gt;ai_family) {
        case AF_UNSPEC:
            wprintf(L"Unspecified\n");
            break;
        case AF_INET:
            wprintf(L"AF_INET (IPv4)\n");
            // the InetNtop function is available on Windows Vista and later
            sockaddr_ipv4 = (struct sockaddr_in *) ptr-&gt;ai_addr;
            wprintf(L"\tIPv4 address %ws\n",
                    InetNtop(AF_INET, &amp;sockaddr_ipv4-&gt;sin_addr, ipstringbuffer,
                             46));

            // We could also use the WSAAddressToString function
            // sockaddr_ip = (LPSOCKADDR) ptr-&gt;ai_addr;
            // The buffer length is changed by each call to WSAAddresstoString
            // So we need to set it for each iteration through the loop for safety
            // ipbufferlength = 46;
            // iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr-&gt;ai_addrlen, NULL, 
            //    ipstringbuffer, &amp;ipbufferlength );
            // if (iRetval)
            //    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
            // else    
            //    wprintf(L"\tIPv4 address %ws\n", ipstringbuffer);
            break;
        case AF_INET6:
            wprintf(L"AF_INET6 (IPv6)\n");
            // the InetNtop function is available on Windows Vista and later
            sockaddr_ipv6 = (struct sockaddr_in6 *) ptr-&gt;ai_addr;
            wprintf(L"\tIPv6 address %ws\n",
                    InetNtop(AF_INET6, &amp;sockaddr_ipv6-&gt;sin6_addr,
                             ipstringbuffer, 46));

            // We could also use WSAAddressToString which also returns the scope ID
            // sockaddr_ip = (LPSOCKADDR) ptr-&gt;ai_addr;
            // The buffer length is changed by each call to WSAAddresstoString
            // So we need to set it for each iteration through the loop for safety
            // ipbufferlength = 46;
            //iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr-&gt;ai_addrlen, NULL, 
            //    ipstringbuffer, &amp;ipbufferlength );
            //if (iRetval)
            //    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
            //else    
            //    wprintf(L"\tIPv6 address %ws\n", ipstringbuffer);
            break;
        default:
            wprintf(L"Other %ld\n", ptr-&gt;ai_family);
            break;
        }
        wprintf(L"\tSocket type: ");
        switch (ptr-&gt;ai_socktype) {
        case 0:
            wprintf(L"Unspecified\n");
            break;
        case SOCK_STREAM:
            wprintf(L"SOCK_STREAM (stream)\n");
            break;
        case SOCK_DGRAM:
            wprintf(L"SOCK_DGRAM (datagram) \n");
            break;
        case SOCK_RAW:
            wprintf(L"SOCK_RAW (raw) \n");
            break;
        case SOCK_RDM:
            wprintf(L"SOCK_RDM (reliable message datagram)\n");
            break;
        case SOCK_SEQPACKET:
            wprintf(L"SOCK_SEQPACKET (pseudo-stream packet)\n");
            break;
        default:
            wprintf(L"Other %ld\n", ptr-&gt;ai_socktype);
            break;
        }
        wprintf(L"\tProtocol: ");
        switch (ptr-&gt;ai_protocol) {
        case 0:
            wprintf(L"Unspecified\n");
            break;
        case IPPROTO_TCP:
            wprintf(L"IPPROTO_TCP (TCP)\n");
            break;
        case IPPROTO_UDP:
            wprintf(L"IPPROTO_UDP (UDP) \n");
            break;
        default:
            wprintf(L"Other %ld\n", ptr-&gt;ai_protocol);
            break;
        }
        wprintf(L"\tLength of this sockaddr: %d\n", ptr-&gt;ai_addrlen);
        wprintf(L"\tCanonical name: %s\n", ptr-&gt;ai_canonname);
    }

    FreeAddrInfoEx(result);
    WSACleanup();

    return 0;
}

</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  Ensure that the development environment targets the newest version of <i>Ws2tcpip.h</i> which includes structure and function definitions for <b>ADDRINFOEX</b> and <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, respectively.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a>



<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>
 

 

