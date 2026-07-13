---
UID: NF:winsock2.WSAStringToAddressA
title: WSAStringToAddressA function (winsock2.h)
description: The WSAStringToAddress function converts a network address in its standard text presentation form into its numeric binary form in a sockaddr structure, suitable for passing to Windows Sockets routines that take such a structure. (ANSI)
helpviewer_keywords: ["WSAStringToAddressA", "winsock2/WSAStringToAddressA"]
old-location: winsock\wsastringtoaddress_2.htm
tech.root: WinSock
ms.assetid: 7b9946c3-c8b3-45ae-9bde-03faaf604bba
ms.date: 12/05/2018
ms.keywords: WSAStringToAddress, WSAStringToAddress function [Winsock], WSAStringToAddressA, WSAStringToAddressW, _win32_wsastringtoaddress_2, winsock.wsastringtoaddress_2, winsock2/WSAStringToAddress, winsock2/WSAStringToAddressA, winsock2/WSAStringToAddressW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAStringToAddressW (Unicode) and WSAStringToAddressA (ANSI)
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
 - WSAStringToAddressA
 - winsock2/WSAStringToAddressA
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
 - WSAStringToAddress
 - WSAStringToAddressA
 - WSAStringToAddressW
---

# WSAStringToAddressA function


## -description

The 
<b>WSAStringToAddress</b> function converts a network address in its standard text   presentation form into its numeric binary form in a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure, suitable for passing to Windows Sockets routines that take such a structure.

## -parameters

### -param AddressString [in]

A pointer to the zero-terminated string that contains the network address in standard text form to convert.

### -param AddressFamily [in]

The address family of the network address pointed to by the <i>AddressString</i> parameter.

### -param lpProtocolInfo [in, optional]

The 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure associated with the provider to be used. If this is <b>NULL</b>, the call is routed to the provider of the first protocol supporting the indicated <i>AddressFamily</i>.

### -param lpAddress [out]

A pointer to a buffer that is filled with a  <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure for the address string if the function succeeds.

### -param lpAddressLength [in, out]

A pointer to the length, in bytes, of the buffer pointed to by the <i>lpAddress</i> parameter. If the function call is successful, this parameter returns a pointer to the size of the <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure returned in the <i>lpAddress</i> parameter. If the specified buffer is not large enough, the function fails with a specific error of 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a> and this parameter is updated with the required size in bytes.

## -returns

The return value for 
<b>WSAStringToAddress</b> is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

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
The buffer pointed to by the <i>lpAddress</i> parameter is too small. Pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The functions was unable to translate the string into a 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>. See the following Remarks section for more information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> before calling any Windows Socket functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>

## -remarks

The 
<b>WSAStringToAddress</b> function converts a network address in standard text   form into its numeric binary form in a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure.

Any missing components of the address will be defaulted to a reasonable value, if possible. For example, a missing port number will default to zero. If the caller wants the translation to be done by a particular provider, it should supply the corresponding 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure in the <i>lpProtocolInfo</i> parameter.

The 
<b>WSAStringToAddress</b> function fails (and returns WSAEINVAL) if the <b>sin_family</b> member of the <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN</a> structure, which is passed in the <i>lpAddress</i> parameter in the form of a 
<b>sockaddr</b> structure, is not set to AF_INET or AF_INET6. 

Support for IPv6 addresses using the <b>WSAStringToAddress</b> function was added on Windows XP with Service Pack 1 (SP1)and later. IPv6 must also be installed on the local computer for the <b>WSAStringToAddress</b> function to support IPv6 addresses. 

<b>Windows Phone 8:</b> This  function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.





> [!NOTE]
> The winsock2.h header defines WSAStringToAddress as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetntopw">InetNtop</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-inetptonw">InetPton</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringa">RtlIpv4AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4addresstostringexw">RtlIpv4AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressa">RtlIpv4StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv4stringtoaddressexw">RtlIpv4StringToAddressEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringa">RtlIpv6AddressToString</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6addresstostringexw">RtlIpv6AddressToStringEx</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa">RtlIpv6StringToAddress</a>



<a href="/windows/desktop/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw">RtlIpv6StringToAddressEx</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa">WSAAddressToString</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a>



<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
