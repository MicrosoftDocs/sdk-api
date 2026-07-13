---
UID: NS:ws2def.addrinfoW
title: ADDRINFOW (ws2def.h)
description: Used by the GetAddrInfoW function to hold host address information.
helpviewer_keywords: ["*PADDRINFOW","ADDRINFOW","ADDRINFOW structure [Winsock]","AF_BTH","AF_INET","AF_INET6","AF_IRDA","AF_NETBIOS","AF_UNSPEC","AI_ADDRCONFIG","AI_ALL","AI_CANONNAME","AI_DISABLE_IDN_ENCODING","AI_FILESERVER","AI_FQDN","AI_NON_AUTHORITATIVE","AI_NUMERICHOST","AI_PASSIVE","AI_RETURN_PREFERRED_NAMES","AI_SECURE","AI_V4MAPPED","IPPROTO_RM","IPPROTO_TCP","IPPROTO_UDP","PADDRINFOW","PADDRINFOW structure pointer [Winsock]","SOCK_DGRAM","SOCK_RAW","SOCK_RDM","SOCK_SEQPACKET","SOCK_STREAM","addrinfoW","addrinfoW structure [Winsock]","winsock.addrinfow","ws2def/PADDRINFOW","ws2def/addrinfoW","ws2tcpip/PADDRINFOW","ws2tcpip/addrinfoW"]
old-location: winsock\addrinfow.htm
tech.root: WinSock
ms.assetid: a4896eac-68ae-4a08-8647-36be65fe4478
ms.date: 12/05/2018
ms.keywords: '*PADDRINFOW, ADDRINFOW, ADDRINFOW structure [Winsock], AF_BTH, AF_INET, AF_INET6, AF_IRDA, AF_NETBIOS, AF_UNSPEC, AI_ADDRCONFIG, AI_ALL, AI_CANONNAME, AI_DISABLE_IDN_ENCODING, AI_FILESERVER, AI_FQDN, AI_NON_AUTHORITATIVE, AI_NUMERICHOST, AI_PASSIVE, AI_RETURN_PREFERRED_NAMES, AI_SECURE, AI_V4MAPPED, IPPROTO_RM, IPPROTO_TCP, IPPROTO_UDP, PADDRINFOW, PADDRINFOW structure pointer [Winsock], SOCK_DGRAM, SOCK_RAW, SOCK_RDM, SOCK_SEQPACKET, SOCK_STREAM, addrinfoW, addrinfoW structure [Winsock], winsock.addrinfow, ws2def/PADDRINFOW, ws2def/addrinfoW, ws2tcpip/PADDRINFOW, ws2tcpip/addrinfoW'
req.header: ws2def.h
req.include-header: Windows Server 2012, Windows 7  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
req.typenames: ADDRINFOW, *PADDRINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - addrinfoW
 - ws2def/addrinfoW
 - PADDRINFOW
 - ws2def/PADDRINFOW
 - ADDRINFOW
 - ws2def/ADDRINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
 - Ws2tcpip.h
api_name:
 - ADDRINFOW
---

# ADDRINFOW structure


## -description

The 
<b>addrinfoW</b> structure is used by the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function to hold host address information.

## -struct-fields

### -field ai_flags

Type: <b>int</b>

Flags that indicate options used in the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function.


Supported values for the <b>ai_flags</b> member are defined in the <i>Winsock2.h</i> header file and can be a combination of the options listed in the following table.



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
The <i>nodename</i> parameter passed to the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function must be a numeric string.

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
The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> will resolve only if a global address is configured. The IPv6 and IPv4 loopback address is not considered a valid global address. This option is only supported on Windows Vista and  later.

</td>
</tr>
<tr>
<td width="40%"><a id="AI_V4MAPPED"></a><a id="ai_v4mapped"></a><dl>
<dt><b>AI_V4MAPPED</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
If the  <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> request for an IPv6 addresses fails, a name service request is made for IPv4 addresses and these addresses are converted to IPv4-mapped IPv6 address format.

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
The address information can be from a non-authoritative namespace provider. 

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
The address information is for a preferred name for a user. 

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
If a flat name (single label) is specified,  <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> will return the fully qualified domain name that the name eventually resolved to. The fully qualified domain name is returned in the <b>ai_canonname</b> member. 

This is different than <b>AI_CANONNAME</b> bit flag that returns the canonical name registered in DNS which may be different than the fully qualified domain name  that the flat name resolved to. 

Only one of the <b>AI_FQDN</b> and <b>AI_CANONNAME</b> bits can be set. The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function will fail if both flags are present with <b>EAI_BADFLAGS</b>.

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
Disable the automatic International Domain Name encoding using Punycode in the name resolution functions called by the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function. 

This option is supported on Windows 8, Windows Server 2012,   and later.

</td>
</tr>
</table>

### -field ai_family

Type: <b>int</b>

The address family. Possible values for the address family are defined in the <i>Winsock2.h</i> header file. 

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the possible values for the address family are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b> or <b>AF_INET6</b>, which are the Internet
                     address family formats for IPv4 and IPv6. Other options for address family (<b>AF_NETBIOS</b> for use with NetBIOS, for example) are supported if a Windows Sockets service provider for the address family is installed. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_UNSPEC</b> and <b>PF_UNSPEC</b>), so either constant can be used.

The following table lists common values for the address family although many other values are possible.

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

The following table lists the possible values for the socket type supported for Windows Sockets 2.

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

Type: <b>int</b>

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

Type: <b>size_t</b>

The length, in bytes, of the buffer pointed to by the <b>ai_addr</b> member.

### -field ai_canonname

Type: <b>PWSTR</b>

The canonical name for the host.

### -field ai_addr

Type: <b>struct sockaddr*</b>

A pointer to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure. The <b>ai_addr</b> member in each returned <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">ADDRINFOW</a> structure points to a filled-in socket address structure. The length, in bytes, of each returned <b>ADDRINFOW</b> structure is specified in the <b>ai_addrlen</b> member.

### -field ai_next

Type: <b>struct addrinfoW*</b>

A pointer to the next structure in a linked list. This parameter is set to <b>NULL</b> in the last 
<b>addrinfoW</b> structure of a linked list.

## -remarks

The 
<b>addrinfoW</b> structure is used by the 
Unicode <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a> function to hold host address information.

 The <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure is ANSI version of this structure used by the ANSI <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a> function.

Macros in the <i>Ws2tcpip.h</i> header file define a <b>ADDRINFOT</b> structure and a mixed-case function name of <b>GetAddrInfo</b>. The <b>GetAddrInfo</b> function should be called with the <i>nodename</i> and <i>servname</i> parameters of a pointer of type  <b>TCHAR</b> and the <i>hints</i> and <i>res</i> parameters of a pointer of type <b>ADDRINFOT</b>. When UNICODE or _UNICODE is defined, <b>ADDRINFOT</b> is defined to the <b>addrinfoW</b> structure and <b>GetAddrInfo</b> is defined to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>, the Unicode version of this function. When UNICODE or _UNICODE is not defined, <b>ADDRINFOT</b> is defined to the <a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a> structure and <b>GetAddrInfo</b> is defined to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>, the ANSI version of this function.

Upon a successful call to <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>, a linked list of 
<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">ADDRINFOW</a> structures is returned in the <i>ppResult</i> parameter passed to the <b>GetAddrInfoW</b> function. The list can be processed by following the pointer provided in the <b>ai_next</b> member of each returned 
<b>ADDRINFOW</b> structure until a <b>NULL</b> pointer is encountered. In each returned 
<b>ADDRINFOW</b> structure, the <b>ai_family</b>, <b>ai_socktype</b>, and <b>ai_protocol</b> members correspond to respective arguments in a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>  or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> function call. Also, the <b>ai_addr</b> member in each returned 
<b>ADDRINFOW</b> structure points to a filled-in socket address structure, the length of which is specified in its <b>ai_addrlen</b> member.


#### Examples

The following code example shows how to use the <b>addrinfoW</b> structure.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
//--------------------------------
// Declare and initialize variables.
    WSADATA wsaData;
    int iResult;

    ADDRINFOW *result = NULL;
    ADDRINFOW *ptr = NULL;
    ADDRINFOW hints;

    DWORD dwRetval = 0;
    int i = 1;

    struct sockaddr_in *sockaddr_ipv4;
    struct sockaddr_in6 *sockaddr_ipv6;
//    LPSOCKADDR sockaddr_ip;

    wchar_t ipstringbuffer[46];

    // Validate the parameters
    if (argc != 3) {
        wprintf(L"usage: %ws <hostname> <servicename>\n", argv[0]);
        wprintf(L"       provides protocol-independent translation\n");
        wprintf(L"       from a host name to an IP address\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws www.contoso.com 0\n", argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }
//--------------------------------
// Setup the hints address info structure
// which is passed to the GetAddrInfoW() function
    memset(&hints, 0, sizeof (hints));
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    wprintf(L"Calling GetAddrInfoW with following parameters:\n");
    wprintf(L"\tName = %ws\n", argv[1]);
    wprintf(L"\tServiceName (or port) = %ws\n\n", argv[2]);

//--------------------------------
// Call GetAddrInfoW(). If the call succeeds,
// the aiList variable will hold a linked list
// of addrinfo structures containing response
// information about the host
    dwRetval = GetAddrInfoW(argv[1], argv[2], &hints, &result);

    if (dwRetval != 0) {
        wprintf(L"GetAddrInfoW failed with error: %d\n", dwRetval);
        WSACleanup();
        return 1;
    }
    wprintf(L"GetAddrInfoW returned success\n");

    // Retrieve each address and print out the hex bytes
    for (ptr = result; ptr != NULL; ptr = ptr->ai_next) {

        wprintf(L"GetAddrInfoW response %d\n", i++);
        wprintf(L"\tFlags: 0x%x\n", ptr->ai_flags);
        wprintf(L"\tFamily: ");
        switch (ptr->ai_family) {
        case AF_UNSPEC:
            wprintf(L"Unspecified\n");
            break;
        case AF_INET:
            wprintf(L"AF_INET (IPv4)\n");
            // the InetNtop function is available on Windows Vista and later
            sockaddr_ipv4 = (struct sockaddr_in *) ptr->ai_addr;
            wprintf(L"\tIPv4 address %ws\n",
                    InetNtop(AF_INET, &sockaddr_ipv4->sin_addr, ipstringbuffer,
                             46));

            // We could also use the WSAAddressToString function
            // sockaddr_ip = (LPSOCKADDR) ptr->ai_addr;
            // The buffer length is changed by each call to WSAAddresstoString
            // So we need to set it for each iteration through the loop for safety
            // ipbufferlength = 46;
            // iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr->ai_addrlen, NULL, 
            //    ipstringbuffer, &ipbufferlength );
            // if (iRetval)
            //    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
            // else    
            //    wprintf(L"\tIPv4 address %ws\n", ipstringbuffer);
            break;
        case AF_INET6:
            wprintf(L"AF_INET6 (IPv6)\n");
            // the InetNtop function is available on Windows Vista and later
            sockaddr_ipv6 = (struct sockaddr_in6 *) ptr->ai_addr;
            wprintf(L"\tIPv6 address %ws\n",
                    InetNtop(AF_INET6, &sockaddr_ipv6->sin6_addr,
                             ipstringbuffer, 46));

            // We could also use WSAAddressToString which also returns the scope ID
            // sockaddr_ip = (LPSOCKADDR) ptr->ai_addr;
            // The buffer length is changed by each call to WSAAddresstoString
            // So we need to set it for each iteration through the loop for safety
            // ipbufferlength = 46;
            //iRetval = WSAAddressToString(sockaddr_ip, (DWORD) ptr->ai_addrlen, NULL, 
            //    ipstringbuffer, &ipbufferlength );
            //if (iRetval)
            //    wprintf(L"WSAAddressToString failed with %u\n", WSAGetLastError() );
            //else    
            //    wprintf(L"\tIPv6 address %ws\n", ipstringbuffer);
            break;
        default:
            wprintf(L"Other %ld\n", ptr->ai_family);
            break;
        }
        wprintf(L"\tSocket type: ");
        switch (ptr->ai_socktype) {
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
            wprintf(L"Other %ld\n", ptr->ai_socktype);
            break;
        }
        wprintf(L"\tProtocol: ");
        switch (ptr->ai_protocol) {
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
            wprintf(L"Other %ld\n", ptr->ai_protocol);
            break;
        }
        wprintf(L"\tLength of this sockaddr: %d\n", ptr->ai_addrlen);
        wprintf(L"\tCanonical name: %s\n", ptr->ai_canonname);
    }

    FreeAddrInfo(result);
    WSACleanup();

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoa">addrinfo</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoexw">addrinfoex</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-addrinfoex2w">addrinfoex2</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>