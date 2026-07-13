---
UID: NF:ws2tcpip.GetNameInfoW
title: GetNameInfoW function (ws2tcpip.h)
description: Provides protocol-independent name resolution from an address to a Unicode host name and from a port number to the Unicode service name.
helpviewer_keywords: ["GetNameInfoW","GetNameInfoW function [Winsock]","winsock.getnameinfow","ws2tcpip/GetNameInfoW"]
old-location: winsock\getnameinfow.htm
tech.root: WinSock
ms.assetid: 5630a49a-c182-440c-ad54-6ff3ba4274c6
ms.date: 12/05/2018
ms.keywords: GetNameInfoW, GetNameInfoW function [Winsock], winsock.getnameinfow, ws2tcpip/GetNameInfoW
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
 - GetNameInfoW
 - ws2tcpip/GetNameInfoW
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
 - GetNameInfoW
---

# GetNameInfoW function


## -description

The 
<b>GetNameInfoW</b> function provides protocol-independent name resolution from an address to a Unicode host name and from a port number  to the Unicode service name.

## -parameters

### -param pSockaddr [in]

A pointer to a socket address structure containing the IP address and port number of the socket. For IPv4, the <i>pSockaddr</i> parameter points to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in</a> structure. For IPv6, the <i>pSockaddr</i> parameter points to a <b>sockaddr_in6</b> structure.

### -param SockaddrLength [in]

The length, in bytes, of the structure pointed to by the <i>pSockaddr</i> parameter.

### -param pNodeBuffer [out]

A pointer to  a Unicode string to hold the host name. On success, a pointer to the Unicode host name is returned as a Fully Qualified Domain Name (FQDN) by default. If the <i>pNodeBuffer</i> parameter is <b>NULL</b>, this indicates the caller does not want to receive a host name string.

### -param NodeBufferSize [in]

The number of <b>WCHAR</b> characters in the buffer pointed to by the <i>pNodeBuffer</i> parameter. The caller must provide a buffer large enough to hold the Unicode host name, including the terminating <b>NULL</b> character.

### -param pServiceBuffer [out]

A pointer to  a Unicode string to hold the service name. On success, a pointer is returned to a Unicode string representing the service name associated with the port number. If the <i>pServiceBuffer</i> parameter is <b>NULL</b>, this indicates the caller does not want to receive a service name string.

### -param ServiceBufferSize [in]

The number of <b>WCHAR</b> characters in the buffer pointed to by the <i>pServiceBuffer</i> parameter. The caller must provide a buffer large enough to hold the Unicode service name, including the terminating <b>NULL</b> character.

### -param Flags [in]

A value used to customize processing of the 
<b>GetNameInfoW</b> function. See the Remarks section.

## -returns

On success,  <b>GetNameInfoW</b> returns zero. Any nonzero return value indicates failure and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

Nonzero error codes returned by the 
<b>GetNameInfoW</b> function also map to the set of errors outlined by Internet Engineering Task Force (IETF) recommendations. The following table shows these error codes and their WSA equivalents. It is recommended that the WSA error codes be used, as they offer familiar and comprehensive error information for Winsock programmers.

<table>
<tr>
<th>Error value</th>
<th>WSA equivalent</th>
<th>Description</th>
</tr>
<tr>
<td>EAI_AGAIN</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></td>
<td>A temporary failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_BADFLAGS</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></td>
<td>One or more invalid parameters was passed to the <b>GetNameInfoW</b> function. This error is returned if a host name was requested but the <i>NodeBufferSize</i> parameter was zero or if a service name was requested but the <i>ServiceBufferSize</i> parameter was zero. </td>
</tr>
<tr>
<td>EAI_FAIL</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></td>
<td>A nonrecoverable failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_FAMILY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></td>
<td>The <b>sa_family</b> member of socket address structure pointed to by the <i>pSockaddr</i> parameter is not supported. </td>
</tr>
<tr>
<td>EAI_MEMORY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></td>
<td>A memory allocation failure occurred.</td>
</tr>
<tr>
<td>EAI_NONAME</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></td>
<td>A service name was requested, but no port number was found in the structure pointed to by the <i>pSockaddr</i> parameter or no service name matching the port number was found. NI_NAMEREQD is set and the host's name cannot be located, or both the <i>pNodeBuffer</i> and <i>pServiceBuffer</i> parameters were <b>NULL</b>. </td>
</tr>
</table>
 

You can use the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a> function to print error messages based on the EAI codes returned by the 
<b>GetNameInfoW</b> function. The 
<b>gai_strerror</b> function is provided for compliance with IETF recommendations, but it is not thread safe. Therefore, use of traditional Windows Sockets functions such as 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> is recommended.

In addition, the following error codes can be returned.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
This error is returned if the <i>pSockaddr</i> parameter is <b>NULL</b> or the  <i>SockaddrLength</i> parameter is less than the length needed for the size of <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in</a> structure for IPv4 or the  <b>sockaddr_in6</b> structure for IPv6.

</td>
</tr>
</table>

## -remarks

The <b>GetNameInfoW</b> function is the Unicode version of a function that provides protocol-independent name resolution. The <b>GetNameInfoW</b> function is used to translate the contents of a socket address structure to a node name and/or a service name.

For the IPv6 and IPv4 protocols, name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, or by other naming mechanisms. This function can be used to determine the host name for an IPv4 or IPv6  address, a reverse DNS lookup, or determine the service name for a port number. The <b>GetNameInfoW</b> function can also be used to convert an IP address or  a port number in a <b>SOCKADDR</b> structure to an Unicode string. This function can also be used to determine the IP address for a host name.

The ANSI version of this function is <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a>.

Macros in the Winsock header file define a mixed-case function name of <b>GetNameInfo</b> that can be used when the application is targeted for  Windows XP with Service Pack 2 (SP2) and later (_WIN32_WINNT &gt;= 0x0502). This <b>GetNameInfo</b> function should be called with the <i>pNodeBuffer</i> and <i>pServiceBuffer</i> parameters of a pointer of type  <b>TCHAR</b>. When UNICODE or _UNICODE is defined, <b>GetNameInfo</b> is defined to the Unicode version and <b>GetNameInfoW</b> is called with the <i>host</i> and <i>serv</i> parameters of a pointer of type <b>char</b>. When UNICODE or _UNICODE is not defined, <b>GetNameInfo</b> is defined to the ANSI version and <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a> is called with the <i>pNodeBuffer</i> and <i>pServiceBuffer</i> parameters of a pointer of type <b>PWCHAR</b>.

To simplify determining buffer requirements for the <i>pNodeBuffer</i> and <i>pServiceBuffer</i> parameters, the following values for maximum host name length and maximum service name are defined in the <i>Ws2tcpip.h</i> header file:


```cpp
#include <windows.h>

#define NI_MAXSERV    32
#define NI_MAXHOST  1025

```



The <i>Flags</i> parameter can be used to customize processing of the 
<b>GetNameInfoW</b> function. The following flags are available:

<ul>
<li>NI_NOFQDN</li>
<li>NI_NUMERICHOST</li>
<li>NI_NAMEREQD</li>
<li>NI_NUMERICSERV</li>
<li>NI_DGRAM</li>
</ul>


When the <b>NI_NAMEREQD</b> flag is set, a host name that cannot be resolved by the DNS results in an error.

Setting the <b>NI_NOFQDN</b> flag results in local hosts having only their Relative Distinguished Name (RDN) returned in the <i>pNodeBuffer</i> parameter.

Setting the <b>NI_NUMERICHOST</b> flag returns the numeric form of the host name instead of its name. The numeric form of the host name is also returned if the host name cannot be resolved by DNS.

Setting the <b>NI_NUMERICSERV</b> flag returns the port number of the service instead of its name. Also, if  a host name is not found for an IP address (127.0.0.2, for example), the hostname is returned as the  IP address.

On Windows Vista and later, if <b>NI_NUMERICSERV</b> is not specified in the <i>flags</i> parameter, and the port number contained in <b>sockaddr</b> structure pointed to by the <i>sa</i>  parameter does not resolve to a well known service, the <b>GetNameInfoW</b> function returns the numeric form of the
   service address (the port number) as a numeric string. When <b>NI_NUMERICSERV</b> is specified, the port number is returned as a numeric string. This behavior is specified in section 6.2 of RFC 3493. For more information, see <a href="https://www.ietf.org/rfc/rfc3493.txt">www.ietf.org/rfc/rfc3493.txt</a>

On Windows Server 2003 and earlier, if <b>NI_NUMERICSERV</b> is not specified in the <i>flags</i> parameter and the port number contained in sockaddr structure pointed to by the <i>sa</i>  parameter does not resolve to a well known service, the <b>GetNameInfoW</b> function fails. When <b>NI_NUMERICSERV</b> is specified, the port number is returned as a numeric string.

Setting the <b>NI_DGRAM</b> flag indicates that the service is a datagram service. This flag is necessary for the few services that provide different port numbers for UDP and TCP service.


<div class="alert"><b>Note</b>  The capability to perform reverse DNS lookups using the <b>GetNameInfoW</b> function is convenient, but such lookups are considered inherently unreliable, and should be used only as a hint.</div>
<div> </div>



<div class="alert"><b>Note</b>  <b>GetNameInfoW</b> cannot be used to resolve alias names.</div>
<div> </div>


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>GetNameInfoW</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int __cdecl main(int argc, char **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    DWORD dwRetval;

    struct sockaddr_in saGNI;
    WCHAR hostname[NI_MAXHOST];
    WCHAR servInfo[NI_MAXSERV];
    u_short port = 27015;

    // Validate the parameters
    if (argc != 2) {
        wprintf(L"usage: %s IPv4 address\n", argv[0]);
        wprintf(L"  to return hostname\n");
        wprintf(L"       %s 127.0.0.1\n", argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }
    //-----------------------------------------
    // Set up sockaddr_in structure which is passed
    // to the getnameinfo function
    saGNI.sin_family = AF_INET;
    saGNI.sin_addr.s_addr = inet_addr(argv[1]);
    saGNI.sin_port = htons(port);

    //-----------------------------------------
    // Call GetNameInfoW
    dwRetval = GetNameInfoW((struct sockaddr *) &saGNI,
                           sizeof (struct sockaddr),
                           hostname,
                           NI_MAXHOST, servInfo, NI_MAXSERV, NI_NUMERICSERV);

    if (dwRetval != 0) {
        wprintf(L"GetNameInfoW failed with error # %ld\n", WSAGetLastError());
        return 1;
    } else {
        wprintf(L"GetNameInfoW returned hostname = %ws\n", hostname);
        return 0;
    }
}

```






> [!NOTE]
> The ws2tcpip.h header defines GetNameInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfo">getnameinfo</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>