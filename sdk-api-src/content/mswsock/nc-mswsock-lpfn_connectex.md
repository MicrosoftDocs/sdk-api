---
UID: NC:mswsock.LPFN_CONNECTEX
title: LPFN_CONNECTEX (mswsock.h)
description: The ConnectEx function establishes a connection to a specified socket, and optionally sends data once the connection is established.
helpviewer_keywords: ["LPFN_CONNECTEX","LPFN_CONNECTEX callback","LPFN_CONNECTEX callback function [Winsock]","_win32_connectex_2","mswsock/LPFN_CONNECTEX","winsock.connectex_2"]
old-location: winsock\connectex_2.htm
tech.root: WinSock
ms.assetid: a4552366-eafa-4f24-b6c2-e6a7edc4b021
ms.date: 12/05/2018
ms.keywords: LPFN_CONNECTEX, LPFN_CONNECTEX callback, LPFN_CONNECTEX callback function [Winsock], _win32_connectex_2, mswsock/LPFN_CONNECTEX, winsock.connectex_2
req.header: mswsock.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPFN_CONNECTEX
 - mswsock/LPFN_CONNECTEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mswsock.h
api_name:
 - LPFN_CONNECTEX
---

# LPFN_CONNECTEX callback function


## -description

The 
<b>ConnectEx</b> function establishes a connection to a specified socket, and optionally sends data once the connection is established. The 
<b>ConnectEx</b> function is only supported on connection-oriented sockets. <div class="alert"><b>Note</b>  This function is a Microsoft-specific extension to the Windows Sockets specification.</div>
<div> </div>

## -parameters

### -param s [in]

A descriptor that identifies an unconnected, previously bound socket. See Remarks for more information.

### -param name [in]

A pointer to  
a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that specifies the address to which to connect. For  IPv4, the <b>sockaddr</b> contains <b>AF_INET</b> for the address family, the destination IPv4 address, and the destination port. For  IPv6, the <b>sockaddr</b> structure contains <b>AF_INET6</b> for the address family, the destination IPv6 address, the destination port, and may contain additional IPv6 flow and scope-id information.

### -param namelen [in]

The length, in bytes, of the <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure pointed to by the <i>name</i> parameter.

### -param lpSendBuffer [in, optional]

A pointer to the buffer to be transferred after a connection is established. This parameter is optional. If the TCP_FASTOPEN option is enabled  on <i>s</i> before <b>ConnectEx</b> is called, then some of this data may be sent during connection establishment.

### -param dwSendDataLength [in]

The length, in bytes, of data pointed to by the <i>lpSendBuffer</i> parameter. This parameter is ignored when the <i>lpSendBuffer</i> parameter is <b>NULL</b>.

### -param lpdwBytesSent [out]

On successful return, this parameter points to a <b>DWORD</b> value that indicates the number of bytes that were sent after the connection was established. The bytes sent are from the buffer pointed to by the <i>lpSendBuffer</i> parameter. This parameter is ignored when the <i>lpSendBuffer</i> parameter is <b>NULL</b>.

### -param lpOverlapped [in]

An 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure used to process the request. The <i>lpOverlapped</i> parameter must be specified, and cannot be <b>NULL</b>.

## -returns

On success,  the <b>ConnectEx</b> function returns <b>TRUE</b>. On failure, the function returns <b>FALSE</b>. Use the 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function to get extended error information. If a call to the 
<b>WSAGetLastError</b> function returns <b>ERROR_IO_PENDING</b>, the operation initiated successfully and is in progress. Under such circumstances, the call may still fail when the overlapped operation completes.

If the error code returned is <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a>, <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a>, or <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>, the application can call 
<b>ConnectEx</b>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> again on the same socket.

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> function call must occur before using 
<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a>.

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
The local address of the socket is already in use, and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs during a 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> operation, but the error could be delayed until a 
<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a> function call, if the 
<b>bind</b> function was called with a wildcard address (<b>INADDR_ANY</b> or <b>in6addr_any</b>) specified for the local IP address. A specific IP address needs to be implicitly bound by the <b>ConnectEx</b> function.

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
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>, or 
<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a> function call is in progress on the specified socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address, such as ADDR_ANY (the 
<a href="/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex">ConnectEx</a> function is only supported for connection-oriented sockets).

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
The attempt to connect was rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i>, <i>lpSendBuffer</i>, or <i>lpOverlapped</i> parameter is not a valid part of the user address space, or <i>namelen</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>s</i> is an unbound or a listening socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is already connected.

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
No buffer space is available; the socket cannot be connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The attempt to connect timed out without establishing a connection.

</td>
</tr>
</table>

## -remarks

The 
<b>ConnectEx</b> function combines several socket functions into a single API/kernel transition. The following operations are performed when a call to the 
<b>ConnectEx</b> function completes successfully:<ul>
<li>A new connection is established.</li>
<li>An optional block of data is sent after the connection is established.</li>
</ul>


For applications targeted to Windows Vista and later, consider using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a> or <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a> function which greatly simplify client application design.

The 
<b>ConnectEx</b> function can only be used with connection-oriented sockets. The socket passed in the <i>s</i> parameter must be created with a socket type of <b>SOCK_STREAM</b>, <b>SOCK_RDM</b>, or <b>SOCK_SEQPACKET</b>.

The <i>lpSendBuffer</i> parameter points to a buffer of data to send after the connection is established. The <i>dwSendDataLength</i> parameter specifies the length in bytes of this data to send. An application can request to send a large buffer of data using the <b>ConnectEx</b> in the same way that the <a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> functions can be used. But developers are strongly advised against sending  a huge buffer in a single call using <b>ConnectEx</b>, because this operation uses a large amount of system memory resources until the whole buffer has been sent. 

If the <b>ConnectEx</b> function is successful, a connection was established and all of the data pointed to by the <i>lpSendBuffer</i> parameter was sent to the address specified in the <b>sockaddr</b> structure pointed to by the <i>name</i> parameter.


<div class="alert"><b>Note</b>  The function pointer for the 
<b>ConnectEx</b> function must be obtained at run time by making a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with the <b>SIO_GET_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_CONNECTEX</b>, a globally unique identifier (GUID) whose value identifies the <b>ConnectEx</b> extension function. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>ConnectEx</b> function. The <b>WSAID_CONNECTEX</b> GUID is defined in the <i>Mswsock.h</i> header file.</div>
<div> </div>


The 
<b>ConnectEx</b> function uses overlapped I/O. As a result, the 
<b>ConnectEx</b> function enables an application to service a large number of clients with relatively few threads. In contrast, the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a> function, which does not use overlapped I/O, usually requires a separate thread to service each connection request when simultaneous  requests are received.<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> for more information.</div>
<div> </div>


Connection-oriented sockets are often unable to complete their connection immediately, and therefore the operation is initiated and the function immediately returns with the ERROR_IO_PENDING or WSA_IO_PENDING error. When the connect operation completes and success or failure is achieved, status is reported using the completion notification mechanism indicated in <i>lpOverlapped</i>. As with all overlapped function calls, you can use events or completion ports as the completion notification mechanism. The <i>lpNumberOfBytesTransferred</i> parameter of the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> or 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> function indicates the number of bytes sent in the request.

When the 
<b>ConnectEx</b> function successfully completes, socket handle <i>s</i> can be passed to only the following functions:<ul>
<li>
<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>
</li>
<li>
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>
</li>
<li>
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>
</li>
<li>
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>
</li>
<li>
<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>
</li>
<li>
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>
</li>
</ul>


If the 
<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a> function is called on a previously connected socket with both TF_DISCONNECT and TF_REUSE_SOCKET flags, the specified socket is returned to a state in which it is not connected, but still bound. In such cases, the handle of the socket can be passed to the 
<b>ConnectEx</b> function in its <i>s</i> parameter, but the socket cannot be reused in an 
<a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a> function call. Similarly, the accepted socket reused using the 
<b>TransmitFile</b> function cannot be used in a call to 
<b>ConnectEx</b>. Note that in the case of a reused socket, <b>ConnectEx</b> is subject to the behavior of the underlying transport. For example, a TCP socket may be subject to the TCP TIME_WAIT state, causing  the <b>ConnectEx</b> call to be delayed.

When the 
<b>ConnectEx</b> function returns <b>TRUE</b>, the socket <i>s</i> is in the default state for a connected socket. The socket <i>s</i> does not enable previously set properties or options until SO_UPDATE_CONNECT_CONTEXT is set on the socket. Use the 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> function to set the SO_UPDATE_CONNECT_CONTEXT option.

For example:


```cpp
//Need to #include <mswsock.h> for SO_UPDATE_CONNECT_CONTEXT

int iResult = 0;

iResult = setsockopt( s, SOL_SOCKET, SO_UPDATE_CONNECT_CONTEXT, NULL, 0 );

```


The 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function can be used with the <b>SO_CONNECT_TIME</b> socket option to check whether a connection has been established while 
<b>ConnectEx</b> is in progress. If a connection has been established, the 
 value returned in the <i>optval</i> parameter passed to the <b>getsockopt</b> function is the number of seconds the socket has been connected. If the socket is not connected, 
the returned <i>optval</i> parameter contains 0xFFFFFFFF. Checking a connection in this manner is necessary to determine whether connections have been established for a period of time without sending any data; in such cases, it is recommended that such connections be terminated.

For example:


```cpp

//Need to #include <mswsock.h> for SO_CONNECT_TIME

int seconds;
int bytes = sizeof(seconds);
int iResult = 0;

iResult = getsockopt( s, SOL_SOCKET, SO_CONNECT_TIME,
                      (char *)&seconds, (PINT)&bytes );
if ( iResult != NO_ERROR ) {
    printf( "getsockopt(SO_CONNECT_TIME) failed with error: %u\n", 
        WSAGetLastError() );
}
else {
    if (seconds == 0xFFFFFFFF)
        printf("Connection not established yet\n");
    else
       printf("Connection has been established %ld seconds\n",
           seconds);
}

```



<div class="alert"><b>Note</b>  If a socket is opened, a 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a> call is made, and then a 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> call is made, Windows Sockets performs an implicit 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> function call.</div>
<div> </div>


If the address parameter of the 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure pointed to in the <i>name</i> parameter is all zeros, 
<b>ConnectEx</b> returns the error <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a>. Any attempt to reconnect an active connection will fail with the error code <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a>.

When a connected socket becomes closed for any reason, it is recommended that the socket be discarded and a new socket created. The reasoning for this is that it  is safest to assume that when things go awry on a connected socket for any reason, the application must discard the socket and create the needed socket again in order to return to a stable point.

If the 
<a href="/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)">DisconnectEx</a> function is called with the <b>TF_REUSE_SOCKET</b> flag, the specified socket is returned to a state in which it is not connected, but still bound. In such cases, the handle of the socket can be passed to the 
<b>ConnectEx</b> function in its <i>s</i> parameter.

 The interval of  time that must elapse before TCP can release a closed connection and reuse its resources is known as the TIME_WAIT state or the  2MSL state. During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.

The TIME_WAIT behavior is specified in <a href="https://www.ietf.org/rfc/rfc793.txt">RFC 793</a>, which requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (MSL) of the network. When a connection is released, its socket pair and internal resources used for the socket can be used to support another connection.

Windows TCP reverts to a TIME_WAIT state subsequent to the closing of a connection. While in the TIME_WAIT state, a socket pair cannot be reused. The TIME_WAIT period is configurable by modifying the following <b>DWORD</b> registry setting that represents the TIME_WAIT period in seconds. 


<b>HKEY_LOCAL_MACHINE</b>&#92;<b>System</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>TCPIP</b>&#92;<b>Parameters</b>&#92;<b>TcpTimedWaitDelay</b>



By default, the MSL is defined to be 120 seconds. The TcpTimedWaitDelay registry setting defaults to a value 240 seconds, which represents 2 times the maximum segment lifetime of 120 seconds or 4 minutes. However, you can use this entry to customize the interval.

Reducing the value of this entry allows TCP to release closed connections faster, providing more resources for new connections. However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to re-establish the connection.

This registry setting can be set from 0 to 300 seconds.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/mswsock/nf-mswsock-acceptex">AcceptEx</a>



<a href="/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)">DisconnectEx</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnect">WSAConnect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist">WSAConnectByList</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea">WSAConnectByName</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>



<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
