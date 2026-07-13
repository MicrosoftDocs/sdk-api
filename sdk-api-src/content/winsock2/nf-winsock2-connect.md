---
UID: NF:winsock2.connect
title: connect function (winsock2.h)
description: The connect function establishes a connection to a specified socket.
helpviewer_keywords: ["_win32_connect_2","connect","connect function [Winsock]","winsock.connect_2","winsock2/connect"]
old-location: winsock\connect_2.htm
tech.root: WinSock
ms.assetid: 13468139-dc03-45bd-850c-7ac2dbcb6e60
ms.date: 12/05/2018
ms.keywords: _win32_connect_2, connect, connect function [Winsock], winsock.connect_2, winsock2/connect
req.header: winsock2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
 - connect
 - winsock2/connect
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
 - connect
---

# connect function


## -description

The 
<b>connect</b> function establishes a connection to a specified socket.

## -parameters

### -param s [in]

A descriptor identifying an unconnected socket.

### -param name [in]

A pointer to the 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure to which the connection should be established.

### -param namelen [in]

The length, in bytes, of the <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure pointed to by the <i>name</i> parameter.

## -returns

If no error occurs, 
<b>connect</b> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

On a blocking socket, the return value indicates success or failure of the connection attempt.


With a nonblocking socket, the connection attempt cannot be completed immediately. In this case, 
<b>connect</b> will return SOCKET_ERROR, and 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> will return 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>. In this case, there are three possible scenarios:

<ul>
<li>Use the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> function to determine the completion of the connection request by checking to see if the socket is writable.</li>
<li>If the application is using 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> to indicate interest in connection events, then the application will receive an FD_CONNECT notification indicating that the 
<b>connect</b> operation is complete (successfully or not).</li>
<li>If the application is using 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a> to indicate interest in connection events, then the associated event object will be signaled indicating that the 
<b>connect</b> operation is complete (successfully or not).</li>
</ul>


Until the connection attempt completes on a nonblocking socket, all subsequent calls to 
<b>connect</b> on the same socket will fail with the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a>, and 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a> when the connection completes successfully. Due to ambiguities in version 1.1 of the Windows Sockets specification, error codes returned from 
<b>connect</b> while a connection is already pending may vary among implementations. As a result, it is not recommended that applications use multiple calls to connect to detect connection completion. If they do, they must be prepared to handle 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a> and 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a> error values the same way that they handle 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a>, to assure robust operation.

If the error code returned indicates the connection attempt failed (that is, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a>, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a>, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>) the application can call 
<b>connect</b> again for the same socket.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRINUSE</a></b></dt>
</dl>
</td>
<td width="60%">
The socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs when executing 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, but could be delayed until the <a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> function if the 
<b>bind</b> was to a wildcard address (<b>INADDR_ANY</b> or <b>in6addr_any</b>) for the local IP address. A specific address needs to be implicitly bound by the <b>connect</b>  function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The blocking Windows Socket 1.1 call was canceled through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonblocking 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> call is in progress on the specified socket.


<div class="alert"><b>Note</b>  In order to preserve backward compatibility, this error is reported as 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a> to Windows Sockets 1.1 applications that link to either Winsock.dll or Wsock32.dll.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address (such as <b>INADDR_ANY</b> or <b>in6addr_any</b>) .

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a></b></dt>
</dl>
</td>
<td width="60%">
The attempt to connect was forcefully rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure pointed to by the <i>name</i> contains incorrect address format for the associated address family  or the <i>namelen</i> parameter is too small. This error is also returned if the <b>sockaddr</b> structure pointed to by the <i>name</i> parameter with a length  specified in the <i>namelen</i> parameter is not in a valid part of the user address space. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>s</i> is a listening socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is already connected (connection-oriented sockets only).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEHOSTUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
A socket operation was attempted to an unreachable host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  No buffer space is available. The socket cannot be connected.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor specified in the <i>s</i> parameter is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
An attempt to connect timed out without establishing a connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the connection cannot be completed immediately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
An attempt to connect a datagram socket to broadcast address failed because 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> option SO_BROADCAST is not enabled.

</td>
</tr>
</table>

## -remarks

The 
<b>connect</b> function is used to create a connection to the specified destination. If socket <i>s</i>, is unbound, unique values are assigned to the local association by the system, and the socket is marked as bound.

For connection-oriented sockets (for example, type SOCK_STREAM), an active connection is initiated to the foreign host using <i>name</i> (an address in the namespace of the socket; for a detailed description, see 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> and 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>).<div class="alert"><b>Note</b>  If a socket is opened, a 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> call is made, and then a 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> call is made, Windows Sockets performs an implicit 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function call.</div>
<div> </div>


When the socket call completes successfully, the socket is ready to send and receive data. If the address member of the structure specified by the <i>name</i> parameter is filled with zeros, 
<b>connect</b> will return the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a>. Any attempt to reconnect an active connection will fail with the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a>.

For connection-oriented, nonblocking sockets, it is often not possible to complete the connection immediately. In such a case, this function returns the error 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>. However, the operation proceeds.


When the success or failure outcome becomes known, it may be reported in one of two ways, depending on how the client registers for notification.

<ul>
<li>If the client uses the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a> function, success is reported in the writefds set and failure is reported in the exceptfds set.</li>
<li>If the client uses the functions 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>, the notification is announced with FD_CONNECT and the error code associated with the FD_CONNECT indicates either success or a specific reason for failure.</li>
</ul>

If the connection is not completed immediately, the client should wait for connection completion before attempting to set socket options using <a href="/windows/win32/api/winsock/nf-winsock-setsockopt">setsockopt</a>. Calling setsockopt while a connection is in progress is not supported.

For a connectionless socket (for example, type SOCK_DGRAM), the operation performed by 
<b>connect</b> is merely to establish a default destination address that can be used on subsequent 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>/
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>/
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> calls. Any datagrams received from an address other than the destination address specified will be discarded. If the address member of the structure specified by <i>name</i> is filled with zeros, the socket will be disconnected. Then, the default remote address will be indeterminate, so 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>/
				<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>/
				<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> calls will return the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a>. However, 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>/
				<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>/
				<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a> can still be used. The default destination can be changed by simply calling 
<b>connect</b> again, even if the socket is already connected. Any datagrams queued for receipt are discarded if <i>name</i> is different from the previous 
<b>connect</b>.

For connectionless sockets, <i>name</i> can indicate any valid address, including a broadcast address. However, to connect to a broadcast address, a socket must use 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> to enable the SO_BROADCAST option. Otherwise, 
<b>connect</b> will fail with the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a>.

When a connection between sockets is broken, the socket that was connected should be discarded and new socket should be created. When a problem develops on a connected socket, the application must discard the socket and create the socket again in order to return to a stable point.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>connect</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example demonstrates the use of the <b>connect</b> function.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

int wmain()
{
    //----------------------
    // Initialize Winsock
    WSADATA wsaData;
    int iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != NO_ERROR) {
        wprintf(L"WSAStartup function failed with error: %d\n", iResult);
        return 1;
    }
    //----------------------
    // Create a SOCKET for connecting to server
    SOCKET ConnectSocket;
    ConnectSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);
    if (ConnectSocket == INVALID_SOCKET) {
        wprintf(L"socket function failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    //----------------------
    // The sockaddr_in structure specifies the address family,
    // IP address, and port of the server to be connected to.
    sockaddr_in clientService;
    clientService.sin_family = AF_INET;
    clientService.sin_addr.s_addr = inet_addr("127.0.0.1");
    clientService.sin_port = htons(27015);

    //----------------------
    // Connect to server.
    iResult = connect(ConnectSocket, (SOCKADDR *) & clientService, sizeof (clientService));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"connect function failed with error: %ld\n", WSAGetLastError());
        iResult = closesocket(ConnectSocket);
        if (iResult == SOCKET_ERROR)
            wprintf(L"closesocket function failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }

    wprintf(L"Connected to server.\n");

    iResult = closesocket(ConnectSocket);
    if (iResult == SOCKET_ERROR) {
        wprintf(L"closesocket function failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }

    WSACleanup();
    return 0;
}


```


For another example that uses the <b>connect</b> function, see <a href="/windows/desktop/WinSock/getting-started-with-winsock">Getting Started With Winsock</a>.

<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>

<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
<li>If an existing IrDA connection is detected at the media-access level, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a> is returned.</li>
<li>If active connections to a device with a different address exist, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRINUSE</a> is returned.</li>
<li>If the socket is already connected or an exclusive/multiplexed mode change failed, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a> is returned.</li>
<li>If the socket was previously bound to a local service name to accept incoming connections using 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a> is returned. Note that once a socket is bound, it cannot be used for establishing an outbound connection.</li>
</ul>


IrDA implements the connect function with addresses of the form sockaddr_irda. Typically, a client application will create a socket with the socket function, scan the immediate vicinity for IrDA devices with the IRLMP_ENUMDEVICES socket option, choose a device from the returned list, form an address, and then call 
<b>connect</b>. There is no difference between blocking and nonblocking semantics.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
