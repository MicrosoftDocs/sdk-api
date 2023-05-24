---
UID: NF:winsock2.WSAConnectByList
title: WSAConnectByList function (winsock2.h)
description: Establishes a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).
helpviewer_keywords: ["WSAConnectByList","WSAConnectByList function [Winsock]","winsock.wsaconnectbylist","winsock2/WSAConnectByList"]
old-location: winsock\wsaconnectbylist.htm
tech.root: WinSock
ms.assetid: 7323d814-e96e-44b9-8ade-a9317e4fbf17
ms.date: 12/05/2018
ms.keywords: WSAConnectByList, WSAConnectByList function [Winsock], winsock.wsaconnectbylist, winsock2/WSAConnectByList
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
 - WSAConnectByList
 - winsock2/WSAConnectByList
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
 - WSAConnectByList
---

# WSAConnectByList function


## -description

The <b>WSAConnectByList</b> function 
   establishes a connection to one out of a collection of possible endpoints represented by a set of 
   destination addresses (host names and ports). This function takes all the destination addresses passed 
   to it and all of the local computer's source addresses, and tries connecting using all possible address 
   combinations before giving up.
   

This function supports both IPv4 and IPv6 addresses.

## -parameters

### -param s [in]

A descriptor that identifies an unbound and unconnected socket. Note that unlike other Winsock calls to 
      establish a connection (for example, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>), 
      the <b>WSAConnectByList</b> function requires an 
      unbound socket.

### -param SocketAddress [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)">SOCKET_ADDRESS_LIST</a> 
      structure that represents the possible destination address and port pairs to connect to a peer. It is the 
      application's responsibility to fill in the port number in the each 
      <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structure in the 
      <b>SOCKET_ADDRESS_LIST</b>.

### -param LocalAddressLength [in, out]

On input, a pointer to the size, in bytes, of the <i>LocalAddress</i> buffer provided by 
      the caller. On output, a pointer to the size, in bytes, of the <b>SOCKADDR</b> for the 
      local address stored in the <i>LocalAddress</i> buffer filled in by the system upon 
      successful completion of the call.

### -param LocalAddress [out]

A pointer to the <b>SOCKADDR</b> structure that receives the local address of the 
      connection. The size of the parameter is exactly the size returned in 
      <i>LocalAddressLength</i>. This is the same information that would be returned by the 
      <a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a> function. This parameter can be 
      <b>NULL</b>, in which case, the <i>LocalAddressLength</i> parameter is 
      ignored.

### -param RemoteAddressLength [in, out]

On input, a pointer to the size, in bytes, of the <i>RemoteAddress</i> buffer provided 
      by the caller. On output, a pointer to the size, in bytes, of the <b>SOCKADDR</b> for the 
      remote address stored in <i>RemoteAddress</i> buffer filled-in by the system upon successful 
      completion of the call.

### -param RemoteAddress [out]

A pointer to the <b>SOCKADDR</b> structure that receives the remote address of the 
      connection. This is the same information that would be returned by the 
      <b>getpeername</b> function. This parameter can be <b>NULL</b>, in 
      which case, the <i>RemoteAddressLength</i> is ignored.

### -param timeout [in]

The time, in milliseconds, to wait for a response from the remote application before aborting the call. 
      This parameter can be <b>NULL</b> in which case 
      <b>WSAConnectByList</b> will complete after either the 
      connection is successfully established or after a connection was attempted and failed on all possible 
      local-remote address pairs.

### -param Reserved [in]

Reserved for future implementation. This parameter must be set to <b>NULL</b>.

## -returns

If a connection is established, 
       <b>WSAConnectByList</b> returns <b>TRUE</b> and 
       <i>LocalAddress</i> and <i>RemoteAddress</i> parameters are filled in if 
       these buffers were supplied by the caller.

If the call fails, <b>FALSE</b> is returned. 
       <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> can then be called to get 
       extended error information.

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
An invalid parameter was passed to the function. The <i>Reserved</i> parameter must be 
        <b>NULL</b>.

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
An invalid socket was passed to the function. The <i>s</i> parameter must not be 
        <b>INVALID_SOCKET</b> or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WSAETIMEDOUT</b></dt>
</dl>
</td>
<td width="60%">
A response from the  remote application was not received before the <i>timeout</i> 
        parameter was exceeded.

</td>
</tr>
</table>

## -remarks

<b>WSAConnectByList</b> is similar to the 
     <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a> function.  Instead of taking a 
     single host name and service name (port), 
     <b>WSAConnectByList</b> takes a list of addresses (host 
     addresses and ports) and connects to one of the addresses. The 
     <b>WSAConnectByList</b> function is designed to support 
     peer-to-peer collaboration scenarios where an application needs to connect to any available node out of a list of 
     potential nodes. <b>WSAConnectByList</b> is compatible 
     with both IPv6 and IPv4 versions.

The set of possible destinations, represented by a list of addresses, is 
     provided by the caller. <b>WSAConnectByList</b> does 
     more than simply attempt to connect to one of possibly many destination addresses.  Specifically, the function 
     takes all remote addresses passed in by the caller, all local addresses, and then attempts a connection first 
     using address pairs with the highest chance of success. As such, 
     <b>WSAConnectByList</b> not only ensures that connection 
     will be established if a connection is at all possible, but also minimizes the time to establish the 
     connection.

The caller can specify the <i>LocalAddress</i> and <i>RemoteAddress</i> 
     buffers and lengths to determine the local and remote addresses for which the connection was successfully 
     established.

The <i>timeout</i> parameter allows the caller to limit the time spent by the function in 
     establishing a connection. Internally, 
     <b>WSAConnectByList</b> performs multiple operations 
     (connection attempts).  In between each operation, the <i>timeout</i> parameter is checked to 
     see if the <i>timeout</i> has been exceeded and, if so, the call is aborted. Note that an 
     individual operation (connect) will not be interrupted once the <i>timeout</i> is exceeded, 
     so the <b>WSAConnectByList</b> call can take longer to 
     time out than the value specified in the <i>timeout</i> parameter.

<b>WSAConnectByList</b> has limitations: It works only 
     for connection-oriented sockets, such as those of type SOCK_STREAM. The function does not support overlapped I/O 
     or non-blocking behavior. <b>WSAConnectByList</b> will 
     block even if the socket is in non-blocking mode. 
     <b>WSAConnectByList</b> will try connecting (one-by-one) 
     to the various addresses provided by the caller. Potentially, each of these connection attempts may fail with a 
     different error code. Since only a single error code can be returned, the value returned is the error code from 
     the last connection attempt.

To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the 
     following steps must be performed prior to calling the function:
     <ul>
<li>The <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function must be called on a 
       socket created for the AF_INET6 address family to disable the <b>IPV6_V6ONLY</b> socket 
       option before calling <b>WSAConnectByList</b>. This is 
       accomplished by calling the <b>setsockopt</b> function on 
       the socket with the <i>level</i> parameter set to <b>IPPROTO_IPV6</b> 
       (see <a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPPROTO_IPV6 Socket Options</a>), the 
       <i>optname</i> parameter set to <b>IPV6_V6ONLY</b>, and the  
       <i>optvalue</i> parameter value set to  zero .</li>
<li>Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.  The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6
   address.  The IPv4 address is encoded into the low-order 32 bits of
   the IPv6 address, and the high-order 96 bits hold the fixed prefix
   0:0:0:0:0:FFFF. The IPv4-mapped IPv6 address format is specified in RFC 4291. For more information, see <a href="https://www.rfc-editor.org/rfc/rfc4291.html">www.ietf.org/rfc/rfc4291.txt</a>. The IN6ADDR_SETV4MAPPED macro in <i>Mstcpip.h</i> can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</li>
</ul>


The arrays of pointers passed in the <i>SocketAddressList</i> parameter point to an array of 
     <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>  structures, which are a generic 
     data type. The <i>RemoteAddress</i> and the <i>LocalAddress</i> 
     parameters also point to <b>SOCKADDR</b>  structures. When 
     <b>WSAConnectByList</b> is called, it is expected that 
     a socket address type specific to the network protocol or address family being used will actually be passed in 
     these parameters. So for IPv4 addresses, a pointer to a <b>sockaddr_in</b> structure 
     would be cast to a pointer to <b>SOCKADDR</b> when passed as a parameter. For IPv6 
     addresses, a pointer to a <b>sockaddr_in6</b> structure would be cast to a pointer to 
     <b>SOCKADDR</b> when passed as a parameter. The 
     <i>SocketAddressList</i> parameter can contain pointers to a mixture of IPv4 and IPv6 
     addresses. So some <b>SOCKET_ADDRESS</b> pointers can be 
     to <b>sockaddr_in</b> structures and others can be to 
     <b>sockaddr_in6</b> structures. If it is expected that IPv6 addresses can be used, then 
     the <i>RemoteAddress</i> and <i>LocalAddress</i> parameters should point 
     to <b>sockaddr_in6</b> structures and be cast to <b>SOCKADDR</b> 
     structures. The <i>RemoteAddressLength</i> and the 
     <i>LocalAddressLength</i> parameters must represent the length of these larger 
     structures.

When the 
<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">WSAConnectByList</a> function returns <b>TRUE</b>, the socket <i>s</i> is in the default state for a connected socket. The socket <i>s</i> does not enable previously set properties or options until SO_UPDATE_CONNECT_CONTEXT is set on the socket. Use the 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function to set the SO_UPDATE_CONNECT_CONTEXT option. 

For example:


```cpp
//Need to #include <mswsock.h> for SO_UPDATE_CONNECT_CONTEXT

int iResult = 0;

iResult = setsockopt( s, SOL_SOCKET, SO_UPDATE_CONNECT_CONTEXT, NULL, 0 );

```


<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">WSAConnectByList</a> with the <i>timeout</i> parameter set to <b>NULL</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.


#### Examples

Establish a connection using <b>WSAConnectByList</b>.


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


SOCKET
OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
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
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}

```

## -see-also

<a href="/windows/desktop/WinSock/ipproto-ipv6-socket-options">IPPROTO_IPV6 Socket Options</a>



<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>



<a href="/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)">SOCKET_ADDRESS_LIST</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getpeername">getpeername</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>