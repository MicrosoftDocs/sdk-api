---
UID: NS:ws2def.addrinfoex2W
title: addrinfoex2W
author: windows-sdk-content
description: Used by the GetAddrInfoEx function to hold host address information when both a canonical name and a fully qualified domain name have been requested.
old-location: winsock\addrinfoex2.htm
old-project: WinSock
ms.assetid: 9CB33347-A838-473D-B5CD-1149D6632CF2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPADDRINFOEX2W, *PADDRINFOEX2W, ADDRINFOEX2, ADDRINFOEX2 structure [Winsock], ADDRINFOEX2W, AF_BTH, AF_INET, AF_INET6, AF_IRDA, AF_NETBIOS, AF_UNSPEC, AI_ADDRCONFIG, AI_ALL, AI_CANONNAME, AI_DISABLE_IDN_ENCODING, AI_FILESERVER, AI_FQDN, AI_NON_AUTHORITATIVE, AI_NUMERICHOST, AI_PASSIVE, AI_RETURN_PREFERRED_NAMES, AI_SECURE, AI_V4MAPPED, IPPROTO_RM, IPPROTO_TCP, IPPROTO_UDP, LPADDRINFOEX2, LPADDRINFOEX2 structure pointer [Winsock], PADDRINFOEX2, PADDRINFOEX2 structure pointer [Winsock], SOCK_DGRAM, SOCK_RAW, SOCK_RDM, SOCK_SEQPACKET, SOCK_STREAM, addrinfoex2, addrinfoex2 structure [Winsock], addrinfoex2A, addrinfoex2W, winsock.addrinfoex2, ws2def/LPADDRINFOEX2, ws2def/PADDRINFOEX2, ws2def/addrinfoex2, ws2def/addrinfoex2A, ws2def/addrinfoex2W"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2def.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: addrinfoex2W (Unicode) and addrinfoex2A (ANSI)
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADDRINFOEX2W, *PADDRINFOEX2W, *LPADDRINFOEX2W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
api_name:
 - ADDRINFOEX2
 - addrinfoex2A
 - addrinfoex2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# addrinfoex2W structure


## -description


The 
<b>addrinfoex2</b> structure is used by the 
<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function to hold host address information when both a canonical name and a fully qualified domain name have been requested.


## -struct-fields




### -field ai_flags

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

When this option is set in the <i>pHints</i> parameter of <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, the <b>NS_EMAIL</b> namespace provider returns only results that were obtained with enhanced security to minimize possible spoofing. 

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


When this option is set in the <i>pHints</i> parameter of <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> and a flat name (single label) is specified in the <i>pName</i> parameter,  the fully qualified domain name that the name eventually resolved to will be returned.

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
Disable the automatic International Domain Name encoding using Punycode in the name resolution functions called by the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function. 

This option is supported on Windows 8, Windows Server 2012,   and later.

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

The length, in bytes, of the  buffer pointed to by the <b>ai_addr</b> member.


### -field ai_canonname

The canonical name for the host.


### -field ai_addr

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure. The <b>ai_addr</b> member in each returned <b>addrinfoex2</b> structure points to a filled-in socket address structure. The length, in bytes, of each returned <b>addrinfoex2</b> structure is specified in the <b>ai_addrlen</b> member.


### -field ai_blob

A pointer to data that is used to return provider-specific namespace information that is associated with the name beyond a list of addresses. The length, in bytes, of the buffer pointed to by <b>ai_blob</b> must be specified in the <b>ai_bloblen</b> member.


### -field ai_bloblen

The length, in bytes, of the <b>ai_blob</b> member.


### -field ai_provider

A pointer to the GUID of a specific namespace provider.


### -field ai_next

A pointer to the next structure in a linked list. This parameter is set to <b>NULL</b> in the last 
<b>addrinfoex2</b> structure of a linked list.


### -field ai_version

The version number of this structure. The value currently used for this version of the structure is 2.


### -field ai_fqdn

The fully qualified domain name for the host.


## -remarks



The 
<b>addrinfoex2</b> structure is supported on Windows 8 and Windows Server 2012

The 
<b>addrinfoex2</b> structure is used by the 
<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function to hold host address information when both the <b>AI_FQDN</b> and <b>AI_CANONNAME</b> bits are set in the <b>ai_flags</b> member of the optional 
<a href="https://msdn.microsoft.com/1077e03d-a1a4-45ab-a5d2-29a67e03f5df">addrinfoex</a> structure provided in the <i>hints</i> parameter to the <b>GetAddrInfoEx</b> function. The <b>addrinfoex2</b>  structure is an enhanced version of the <b>addrinfoex</b> structure that can return both the canonical name and the fully qualified domain name for the host. The extra structure members are for a version number of the structure and the fully qualified domain name for the host. 

The <b>addrinfoex2</b>  structure used with <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>  function is an enhanced version of the <a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a> and <a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a> structures used with the <a href="https://msdn.microsoft.com/7034b866-346e-4a3b-b81b-72816d95b1d6">getaddrinfo</a> and <a href="https://msdn.microsoft.com/82436a88-5b37-4758-a5c9-b60dd1cbc36c">GetAddrInfoW</a> functions. The <b>GetAddrInfoEx</b>  function allows specifying the namespace provider to resolve the query. For use with the IPv6 and IPv4 protocol, name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, an email provider (the <b>NS_EMAIL</b> namespace), or by other naming mechanisms. 

The blob data in tha <b>ai_blob</b> member is used to return additional provider-specific namespace information associated with a name. The format of data in the <b>ai_blob</b> member is specific to a particular namespace provider. Currently, blob data is used by the <b>NS_EMAIL</b> namespace provider to supply additional information.  

When UNICODE or _UNICODE is defined, <b>addrinfoex2</b> is defined to <b>addrinfoex2W</b>, the Unicode version of this structure. The string parameters are defined to the <b>PWSTR</b> data type and the <b>addrinfoex2W</b> structure is used.

When UNICODE or _UNICODE is not defined, <b>addrinfoex2</b> is defined to <b>addrinfoex2A</b>, the ANSI version of this structure. The string parameters are of the <b>char *</b> data type and the <b>addrinfoex2A</b> structure is used.

Upon a successful call to <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>, a linked list of 
<b>addrinfoex2</b> structures is returned in the <i>ppResult</i> parameter passed to the <b>GetAddrInfoEx</b> function. The list can be processed by following the pointer provided in the <b>ai_next</b> member of each returned 
<b>addrinfoex2</b> structure until a <b>NULL</b> pointer is encountered. In each returned 
<b>addrinfoex2</b> structure, the <b>ai_family</b>, <b>ai_socktype</b>, and <b>ai_protocol</b> members correspond to respective arguments in a 
<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> or <a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> function call. Also, the <b>ai_addr</b> member in each returned 
<b>addrinfoex2</b> structure points to a filled-in socket address structure, the length of which is specified in its <b>ai_addrlen</b> member.




## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>



<a href="https://msdn.microsoft.com/4df914ab-59b0-4110-bc81-59e5f6722b8d">addrinfo</a>



<a href="https://msdn.microsoft.com/a4896eac-68ae-4a08-8647-36be65fe4478">addrinfoW</a>



<a href="https://msdn.microsoft.com/1077e03d-a1a4-45ab-a5d2-29a67e03f5df">addrinfoex</a>
 

 

