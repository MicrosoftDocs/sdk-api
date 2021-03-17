---
UID: NF:ws2tcpip.getnameinfo
title: getnameinfo function (ws2tcpip.h)
description: Provides protocol-independent name resolution from an address to an ANSI host name and from a port number to the ANSI service name.
helpviewer_keywords: ["GetNameInfoA","_win32_getnameinfo_2","getnameinfo","getnameinfo function [Winsock]","winsock.getnameinfo_2","ws2tcpip/getnameinfo"]
old-location: winsock\getnameinfo_2.htm
tech.root: WinSock
ms.assetid: 7d1fb0ed-cc32-4b38-8ff5-88c2cca4f375
ms.date: 12/05/2018
ms.keywords: GetNameInfoA, _win32_getnameinfo_2, getnameinfo, getnameinfo function [Winsock], winsock.getnameinfo_2, ws2tcpip/getnameinfo
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
 - getnameinfo
 - ws2tcpip/getnameinfo
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
 - getnameinfo
---

# getnameinfo function


## -description

The 
<b>getnameinfo</b> function provides protocol-independent name resolution from an address to an ANSI host name and from a port number  to the ANSI service name.

## -parameters

### -param pSockaddr [in]

A pointer to a socket address structure that contains the address and port number of the socket. For IPv4, the <i>sa</i> parameter points to a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in</a> structure. For IPv6, the <i>sa</i> parameter points to a <b>sockaddr_in6</b> structure.

### -param SockaddrLength [in]

The length, in bytes, of the structure pointed to by the <i>sa</i> parameter.

### -param pNodeBuffer [out]

A pointer to  an ANSI string used to hold the host name. On success, the host name is returned as a Fully Qualified Domain Name (FQDN) by default. If the <i>host</i> parameter is <b>NULL</b>, this indicates the caller does not want to receive a host name string.

### -param NodeBufferSize [in]

The length, in bytes, of the buffer pointed to by the <i>host</i> parameter. The caller must provide a buffer large enough to hold the host name, including the terminating <b>NULL</b> character.

### -param pServiceBuffer [out]

A pointer to  an ANSI string to hold the service name. On success, an ANSI string that represents the service name associated with the port number is returned. If the <i>serv</i> parameter is <b>NULL</b>, this indicates the caller does not want to receive a service name string.

### -param ServiceBufferSize [in]

The length, in bytes, of the buffer pointed to by the <i>serv</i> parameter. The caller must provide a buffer large enough to hold the service name, including the terminating <b>NULL</b> character.

### -param Flags [in]

A value used to customize processing of the 
<b>getnameinfo</b> function. See the Remarks section.

## -returns

On success,  <b>getnameinfo</b> returns zero. Any nonzero return value indicates failure and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

Nonzero error codes returned by the 
<b>getnameinfo</b> function also map to the set of errors outlined by Internet Engineering Task Force (IETF) recommendations. The following table lists these error codes and their WSA equivalents. It is recommended that the WSA error codes be used, as they offer familiar and comprehensive error information for Winsock programmers.

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
<td>One or more invalid parameters was passed to the <b>getnameinfo</b> function. This error is returned if a host name was requested but the <i>hostlen</i> parameter was zero or if a service name was requested, but the <i>servlen</i> parameter was zero. </td>
</tr>
<tr>
<td>EAI_FAIL</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANO_RECOVERY</a></td>
<td>A nonrecoverable failure in name resolution occurred.</td>
</tr>
<tr>
<td>EAI_FAMILY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></td>
<td>The <b>sa_family</b> member of socket address structure pointed to by the <i>sa</i> parameter is not supported. </td>
</tr>
<tr>
<td>EAI_MEMORY</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></td>
<td>A memory allocation failure occurred.</td>
</tr>
<tr>
<td>EAI_NONAME</td>
<td><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAHOST_NOT_FOUND</a></td>
<td>A service name was requested, but no port number was found in the structure pointed to by the <i>sa</i> parameter or no service name matching the port number was found. NI_NAMEREQD is set and the host name cannot be located, or both the <i>host</i> and <i>serv</i> parameters were <b>NULL</b>. </td>
</tr>
</table>
 

Use the 
<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a> function to print error messages based on the EAI codes returned by the 
<b>getnameinfo</b> function. The 
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
This error is returned if the <i>sa</i> parameter is <b>NULL</b> or the  <i>salen</i> parameter is less than the length required for the size of <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr_in</a> structure for IPv4 or the  <b>sockaddr_in6</b> structure for IPv6.

</td>
</tr>
</table>

## -remarks

The <b>getnameinfo</b> function is the ANSI version of a function that provides protocol-independent name resolution. The <b>getnameinfo</b> function is used to translate the contents of a socket address structure to a node name and/or a service name.

For IPv6 and IPv4 protocols, Name resolution can be by the Domain Name System (DNS), a local <i>hosts</i> file, or by other naming mechanisms. This function can be used to determine the host name for an IPv4 or IPv6  address, a reverse DNS lookup, or determine the service name for a port number. The <b>getnameinfo</b> function can also be used to convert an IP address or  a port number in a <b>sockaddr</b> structure to an ANSI string. This function can also be used to determine the IP address for a host name.

Another name that can be used for the <b>getnameinfo</b> function is <b>GetNameInfoA</b>. Macros in the <i>Ws2tcpip.h</i> header file define <b>GetNameInfoA</b> to <b>getnameinfo</b>.

The Unicode version of this function available on Windows XP with Service Pack 2 (SP2) and later is <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfow">GetNameInfoW</a>.

Macros in the Winsock header file define a mixed-case function name of <b>GetNameInfo</b> that can be used when the application is targeted for  Windows XP with SP2 and later (_WIN32_WINNT &gt;= 0x0502). This <b>GetNameInfo</b> function should be called with the <i>host</i> and <i>serv</i> parameters of a pointer of type  <b>TCHAR</b>. When UNICODE or _UNICODE is not defined, <b>GetNameInfo</b> is defined to the ANSI version and <b>getnameinfo</b> is called with the <i>host</i> and <i>serv</i> parameters of a pointer of type <b>char</b>. When UNICODE or _UNICODE is defined, <b>GetNameInfo</b> is defined to the Unicode version and <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfow">GetNameInfoW</a> is called with the <i>pNodeBuffer</i> and <i>pServiceBuffer</i> parameters of a pointer of type <b>PWCHAR</b>.

To simplify determining buffer requirements for the <i>host</i> and <i>serv</i> parameters, the following values for maximum host name length and maximum service name are defined in the <i>Ws2tcpip.h</i> header file.


```cpp
#define NI_MAXSERV    32
#define NI_MAXHOST  1025

```



The <i>flags</i> parameter can be used to customize processing of the 
<b>getnameinfo</b> function. The following flags are available:

<ul>
<li>NI_NOFQDN</li>
<li>NI_NUMERICHOST</li>
<li>NI_NAMEREQD</li>
<li>NI_NUMERICSERV</li>
<li>NI_DGRAM</li>
</ul>


When the <b>NI_NAMEREQD</b> flag is set, a host name that cannot be resolved by DNS results in an error.

Setting the <b>NI_NOFQDN</b> flag results in local hosts having only their Relative Distinguished Name (RDN) returned in the <i>host</i> parameter.

Setting the <b>NI_NUMERICHOST</b> flag returns the numeric form of the host name instead of its name. The numeric form of the host name is also returned if the host name cannot be resolved by DNS.

Setting the <b>NI_NUMERICSERV</b> flag returns the port number of the service instead of its name. Also, if  a host name is not found for an IP address (127.0.0.2, for example), the hostname is returned as the  IP address.

On Windows Vista and later, if <b>NI_NUMERICSERV</b> is not specified in the <i>flags</i> parameter and the port number contained in sockaddr structure pointed to by the <i>sa</i>  parameter does not resolve to a well known service, the <b>getnameinfo</b> function returns the numeric form of the
   service address (the port number) as a numeric string. When <b>NI_NUMERICSERV</b> is specified, the port number is returned as a numeric string. This behavior is specified in section 6.2 of RFC 3493. For more information, see <a href="https://www.ietf.org/rfc/rfc3493.txt">www.ietf.org/rfc3493.txt</a>

On Windows Server 2003 and earlier, if <b>NI_NUMERICSERV</b> is not specified in the <i>flags</i> parameter, and the port number contained in the <b>sockaddr</b> structure pointed to by the <i>sa</i>  parameter does not resolve to a well known service, the <b>getnameinfo</b> function fails. When <b>NI_NUMERICSERV</b> is specified, the port number is returned as a numeric string.

Setting the <b>NI_DGRAM</b> flag indicates that the service is a datagram service. This flag is necessary for the few services that provide different port numbers for UDP and TCP service.


<div class="alert"><b>Note</b>  The ability to perform reverse DNS lookups using the <b>getnameinfo</b> function is convenient, but such lookups are considered inherently unreliable, and should be used only as a hint.</div>
<div> </div>



<div class="alert"><b>Note</b>  The <b>getnameinfo</b> function cannot be used to resolve alias names.</div>
<div> </div>


<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following code example shows how to use the <b>getnameinfo</b> function.


```cpp
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

// link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int __cdecl main(int argc, char **argv)
{

    //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData = {0};
    int iResult = 0;

    DWORD dwRetval;

    struct sockaddr_in saGNI;
    char hostname[NI_MAXHOST];
    char servInfo[NI_MAXSERV];
    u_short port = 27015;

    // Validate the parameters
    if (argc != 2) {
        printf("usage: %s IPv4 address\n", argv[0]);
        printf("  to return hostname\n");
        printf("       %s 127.0.0.1\n", argv[0]);
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    //-----------------------------------------
    // Set up sockaddr_in structure which is passed
    // to the getnameinfo function
    saGNI.sin_family = AF_INET;
    saGNI.sin_addr.s_addr = inet_addr(argv[1]);
    saGNI.sin_port = htons(port);

    //-----------------------------------------
    // Call getnameinfo
    dwRetval = getnameinfo((struct sockaddr *) &saGNI,
                           sizeof (struct sockaddr),
                           hostname,
                           NI_MAXHOST, servInfo, NI_MAXSERV, NI_NUMERICSERV);

    if (dwRetval != 0) {
        printf("getnameinfo failed with error # %ld\n", WSAGetLastError());
        return 1;
    } else {
        printf("getnameinfo returned hostname = %s\n", hostname);
        return 0;
    }
}

```


<h3><a id="Support_for_getnameinfo_on_older_versions_of_Windows_"></a><a id="support_for_getnameinfo_on_older_versions_of_windows_"></a><a id="SUPPORT_FOR_GETNAMEINFO_ON_OLDER_VERSIONS_OF_WINDOWS_"></a>Support for getnameinfo on older versions of Windows
</h3>
The <b>getnameinfo</b> function was added to the <i>Ws2_32.dll</i> on Windows XP and later. If you want to execute an application using this function on earlier versions of Windows (Windows 2000, Windows NT, and Windows Me/98/95), then you need to include the <i>Ws2tcpip.h</i> file and also include the <i>Wspiapi.h</i> file. When the <i>Wspiapi.h</i> include file is added, the <b>getnameinfo</b> function is defined to the WspiapiGetNameInfo inline function in the <i>Wspiapi.h</i> file. At runtime, the WspiapiGetNameInfo function is implemented in such a way that if the <i>Ws2_32.dll</i> or the <i>Wship6.dll</i> (the file containing <b>getnameinfo</b> in the IPv6 Technology Preview for Windows 2000) does not include <b>getnameinfo</b>, then a version of  <b>getnameinfo</b> is implemented inline based on code in the <i>Wspiapi.h</i> header file. This inline code will be used on older Windows platforms that do not natively support the <b>getnameinfo</b> function. 

The IPv6  protocol is supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed. Otherwise <b>getnameinfo</b> support on versions of Windows earlier than Windows XP is limited to handling IPv4 name resolution. 

The <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfow">GetNameInfoW</a> function is the Unicode version of  <b>getnameinfo</b>.  The <b>GetNameInfoW</b> function was added to the <i>Ws2_32.dll</i> in Windows XP with SP2. The <b>GetNameInfoW</b> function cannot be used on versions of Windows earlier than Windows XP with SP2. 



<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getnameinfow">GetNameInfoW</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-gai_strerrora">gai_strerror</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>