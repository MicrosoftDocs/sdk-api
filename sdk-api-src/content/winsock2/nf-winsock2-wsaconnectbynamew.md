---
UID: NF:winsock2.WSAConnectByNameW
title: WSAConnectByNameW function (winsock2.h)
description: Establishes a connection to a specified host and port. (Unicode)
helpviewer_keywords: ["WSAConnectByName", "WSAConnectByName function [Winsock]", "WSAConnectByNameW", "winsock.wsaconnectbyname_2", "winsock2/WSAConnectByName", "winsock2/WSAConnectByNameW"]
old-location: winsock\wsaconnectbyname_2.htm
tech.root: WinSock
ms.assetid: 6d87699f-03bd-4579-9907-ae3c29b7332b
ms.date: 12/05/2018
ms.keywords: WSAConnectByName, WSAConnectByName function [Winsock], WSAConnectByNameA, WSAConnectByNameW, winsock.wsaconnectbyname_2, winsock2/WSAConnectByName, winsock2/WSAConnectByNameA, winsock2/WSAConnectByNameW
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WSAConnectByNameW (Unicode) and WSAConnectByNameA (ANSI)
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
 - WSAConnectByNameW
 - winsock2/WSAConnectByNameW
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
 - WSAConnectByName
 - WSAConnectByNameA
 - WSAConnectByNameW
---

# WSAConnectByNameW function


## -description

The <b>WSAConnectByName</b> function establishes a connection to a specified host and port. This function is provided to allow a quick connection to a network endpoint given a host name and port.

This function supports both IPv4 and IPv6 addresses.

## -parameters

### -param s [in]

A descriptor that identifies an unconnected socket.

<div class="alert"><b>Note</b>  On Windows 7,  Windows Server 2008 R2, and earlier, the <b>WSAConnectByName</b> function requires an unbound and unconnected socket. This differs from other Winsock calls to establish a connection (for example, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>). </div>
<div> </div>

### -param nodename [in]

A <b>NULL</b>-terminated string that contains the name of the host or the IP address of the host on which to connect for IPv4 or IPv6.

### -param servicename [in]

A <b>NULL</b>-terminated string that contains the service name or destination port of the host on which to connect for IPv4 or IPv6. 

A service name is a string alias for a port number. For example, “http” is an alias for port 80 defined by the Internet Engineering Task Force (IETF) as the default port used by web servers for the HTTP protocol. Possible values for the <i>servicename</i> parameter when a port number is not specified are listed in the following file: 

<code>%WINDIR%\system32\drivers\etc\services</code>

### -param LocalAddressLength [in, out]

On input, a pointer to the size, in bytes, of the <i>LocalAddress</i> buffer provided by the caller. On output, a pointer to the size, in bytes, of the <b>SOCKADDR</b> for the local address stored in the <i>LocalAddress</i> buffer filled in by the system upon successful completion of the call.

### -param LocalAddress [out]

A pointer to the <b>SOCKADDR</b> structure that receives the local address of the connection. The size of the parameter is exactly the size returned in <i>LocalAddressLength</i>. This is the same information that would be returned by the <a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a> function. This parameter can be <b>NULL</b>, in which case, the <i>LocalAddressLength</i> parameter is ignored.

### -param RemoteAddressLength [in, out]

On input, a pointer to the size, in bytes, of the <i>RemoteAddress</i> buffer provided by the caller. On output, a pointer to the size, in bytes, of the <b>SOCKADDR</b> for the remote address stored in <i>RemoteAddress</i> buffer filled-in by the system upon successful completion of the call.

### -param RemoteAddress [out]

A pointer to the <b>SOCKADDR</b> structure that receives the remote address of the connection. This is the same information that would be returned by the <b>getpeername</b> function. This parameter can be <b>NULL</b>, in which case, the <i>RemoteAddressLength</i> is ignored.

### -param timeout [in]

The time, in milliseconds, to wait for a response from the remote application before aborting the call.

### -param Reserved

Reserved for future implementation. This parameter must be set to <b>NULL</b>.

## -returns

If a connection is established, <b>WSAConnectByName</b> returns <b>TRUE</b> and <i>LocalAddress</i> and <i>RemoteAddress</i> parameters are filled in if these buffers were supplied by the caller.

If the call fails, <b>FALSE</b> is returned. <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> can then be called to get extended error information.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSAEHOSTUNREACH</b></dt>
</dl>
</td>
<td width="60%">
The host passed as the <i>nodename</i> parameter was unreachable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSAEINVAL</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.  The <i>nodename</i>  or the <i>servicename</i> parameter must not be <b>NULL</b>. The  <i>Reserved</i>  parameter must be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSAENOBUFS</b></dt>
</dl>
</td>
<td width="60%">
Sufficient memory could not be allocated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSAENOTSOCK</b></dt>
</dl>
</td>
<td width="60%">
An invalid socket was passed to the function. The <i>s</i>  parameter must not be <b>INVALID_SOCKET</b> or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSAETIMEDOUT</b></dt>
</dl>
</td>
<td width="60%">
A response from the  remote application was not received before the <i>timeout</i> parameter was exceeded.

</td>
</tr>
</table>

## -remarks

<b>WSAConnectByName</b> is provided to enable quick and transparent connections to remote hosts on specific ports. It is compatible with both IPv6 and IPv4 versions.

To enable both IPv6 and IPv4 communications, use the following method:<ul>
<li>The <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function must be called on a socket created for the AF_INET6 address family to disable the <b>IPV6_V6ONLY</b> socket option before calling <b>WSAConnectByName</b>. This is accomplished by calling the <b>setsockopt</b> function on the socket with the <i>level</i> parameter set to <b>IPPROTO_IPV6</b> (see <a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPPROTO_IPV6 Socket Options</a>), the <i>optname</i> parameter set to <b>IPV6_V6ONLY</b>, and the  <i>optvalue</i> parameter value set to  zero .</li>
</ul>


<b>WSAConnectByName</b> has limitations:
It works only for connection-oriented sockets, such as those of type SOCK_STREAM.
The function does not support overlapped I/O or non-blocking behavior. <b>WSAConnectByName</b> will block even if the socket is in non-blocking mode.
	

<b>WSAConnectByName</b> does not support user-provided data during the establishment of a connection. This call does not support FLOWSPEC structures, either. In cases where these features are required, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> must be used instead.

In versions before Windows 10, if an application needs to bind to a specific local address or port, then <b>WSAConnectByName</b> cannot be used since the socket parameter to <b>WSAConnectByName</b> must be an unbound socket.

 
This restriction was removed Windows 10.

The <i>RemoteAddress</i> and the <i>LocalAddress</i> parameters point to a <b>SOCKADDR</b>  structure, which is a generic data type. When <b>WSAConnectByName</b> is called, it is expected that a socket address type specific to the network protocol or address family being used will actually be passed in these parameters. So for IPv4 addresses, a pointer to a <b>sockaddr_in</b> structure would be cast to a pointer to <b>SOCKADDR</b> as the <i>RemoteAddress</i> and <i>LocalAddress</i> parameters. For IPv6 addresses, a pointer to a <b>sockaddr_in6</b> structure would be cast to a pointer to <b>SOCKADDR</b> as the <i>RemoteAddress</i> and <i>LocalAddress</i> parameters. 

When the 
<b>WSAConnectByName</b> function returns <b>TRUE</b>, the socket <i>s</i> is in the default state for a connected socket. The socket <i>s</i> does not enable previously set properties or options until SO_UPDATE_CONNECT_CONTEXT is set on the socket. Use the 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function to set the SO_UPDATE_CONNECT_CONTEXT option. 

For example:


```cpp
//Need to #include <mswsock.h> for SO_UPDATE_CONNECT_CONTEXT

int iResult = 0;

iResult = setsockopt( s, SOL_SOCKET, SO_UPDATE_CONNECT_CONTEXT, NULL, 0 );

```


<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSAConnectByName</b> with the <i>timeout</i> parameter set to <b>NULL</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<b>Windows Phone 8:</b> The <b>WSAConnectByNameW</b> function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: The <b>WSAConnectByNameW</b> function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

Establish a connection using <b>WSAConnectByName</b>.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <mswsock.h>   // Need for SO_UPDATE_CONNECT_CONTEXT
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET
OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket = INVALID_SOCKET;
    int ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        wprintf(L"socket failed with error: %d\n", WSAGetLastError());
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        wprintf(L"setsockopt for IPV6_V6ONLY failed with error: %d\n",
            WSAGetLastError());
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (!bSuccess){
        wprintf(L"WsaConnectByName failed with error: %d\n", WSAGetLastError());
        closesocket(ConnSocket);
        return INVALID_SOCKET;       

    
    }

    iResult = setsockopt(ConnSocket, SOL_SOCKET,
        SO_UPDATE_CONNECT_CONTEXT, NULL, 0);
    if (iResult == SOCKET_ERROR){
        wprintf(L"setsockopt for SO_UPDATE_CONNECT_CONTEXT failed with error: %d\n",
            WSAGetLastError());
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    return ConnSocket;
}

int __cdecl wmain(int argc, wchar_t **argv)
{
   //-----------------------------------------
    // Declare and initialize variables
    WSADATA wsaData;
    int iResult;

    SOCKET s = INVALID_SOCKET;

    // Validate the parameters
    if (argc != 3) {
        wprintf(L"usage: %ws <Nodename> <Portname>\n", argv[0]);
        wprintf(L"wsaconnectbyname establishes a connection to a specified host and port.\n");
        wprintf(L"%ws www.contoso.com 8080\n", argv[0]);
        return 1;
    }

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed: %d\n", iResult);
        return 1;
    }

    wprintf(L"WsaConnectByName with following parameters:\n");
    wprintf(L"\tNodename = %ws\n", argv[1]);
    wprintf(L"\tPortname (or port) = %ws\n\n", argv[2]);

    //--------------------------------
    // Call our function that uses the WsaConnectByName. 
    
    s = OpenAndConnect(argv[1], argv[2]);
    if ( s == INVALID_SOCKET ) {
        wprintf(L"WsaConnectByName failed with error: %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    else
    {
        wprintf(L"WsaConnectByName succeeded\n");
        
        closesocket(s);
        WSACleanup();
        return 0;
    }
}

```






> [!NOTE]
> The winsock2.h header defines WSAConnectByName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPPROTO_IPV6 Socket Options</a>



<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getpeername">getpeername</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>
