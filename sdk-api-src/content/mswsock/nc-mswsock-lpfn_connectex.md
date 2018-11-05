---
UID: NC:mswsock.LPFN_CONNECTEX
title: LPFN_CONNECTEX
author: windows-sdk-content
description: The ConnectEx function establishes a connection to a specified socket, and optionally sends data once the connection is established.
old-location: winsock\connectex_2.htm
tech.root: winsock
ms.assetid: a4552366-eafa-4f24-b6c2-e6a7edc4b021
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: LPFN_CONNECTEX, LPFN_CONNECTEX callback, LPFN_CONNECTEX callback function [Winsock], _win32_connectex_2, mswsock/LPFN_CONNECTEX, winsock.connectex_2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mswsock.h
api_name:
 - LPFN_CONNECTEX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


### -param *name [in]

A pointer to  
a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure that specifies the address to which to connect. For  IPv4, the <b>sockaddr</b> contains <b>AF_INET</b> for the address family, the destination IPv4 address, and the destination port. For  IPv6, the <b>sockaddr</b> structure contains <b>AF_INET6</b> for the address family, the destination IPv6 address, the destination port, and may contain additional IPv6 flow and scope-id information.


### -param namelen [in]

The length, in bytes, of the <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure pointed to by the <i>name</i> parameter.


### -param lpSendBuffer [in, optional]

A pointer to the buffer to be transferred after a connection is established. This parameter is optional. If the TCP_FASTOPEN option is enabled  on <i>s</i> before <b>ConnectEx</b> is called, then some of this data may be sent during connection establishment.


### -param dwSendDataLength [in]

The length, in bytes, of data pointed to by the <i>lpSendBuffer</i> parameter. This parameter is ignored when the <i>lpSendBuffer</i> parameter is <b>NULL</b>. 


### -param lpdwBytesSent [out]

On successful return, this parameter points to a <b>DWORD</b> value that indicates the number of bytes that were sent after the connection was established. The bytes sent are from the buffer pointed to by the <i>lpSendBuffer</i> parameter. This parameter is ignored when the <i>lpSendBuffer</i> parameter is <b>NULL</b>.


### -param lpOverlapped [in]

An 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure used to process the request. The <i>lpOverlapped</i> parameter must be specified, and cannot be <b>NULL</b>.


## -returns



On success,  the <b>ConnectEx</b> function returns <b>TRUE</b>. On failure, the function returns <b>FALSE</b>. Use the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function to get extended error information. If a call to the 
<b>WSAGetLastError</b> function returns <b>ERROR_IO_PENDING</b>, the operation initiated successfully and is in progress. Under such circumstances, the call may still fail when the overlapped operation completes.

If the error code returned is <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNREFUSED</a>, <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETUNREACH</a>, or <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a>, the application can call 
<b>ConnectEx</b>, 
<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>, or 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> again on the same socket.

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> function call must occur before using 
<a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEADDRINUSE</a></b></dt>
</dl>
</td>
<td width="60%">
The local address of the socket is already in use, and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs during a 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> operation, but the error could be delayed until a 
<a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a> function call, if the 
<b>bind</b> function was called with a wildcard address (<b>INADDR_ANY</b> or <b>in6addr_any</b>) specified for the local IP address. A specific IP address needs to be implicitly bound by the<b>ConnectEx</b> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonblocking 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>, 
<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>, or 
<a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a> function call is in progress on the specified socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address, such as ADDR_ANY (the 
<a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a> function is only supported for connection-oriented sockets).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNREFUSED</a></b></dt>
</dl>
</td>
<td width="60%">
The attempt to connect was rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i>, <i>lpSendBuffer</i>, or <i>lpOverlapped</i> parameter is not a valid part of the user address space, or <i>namelen</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>s</i> is an unbound or a listening socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is already connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEHOSTUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
A socket operation was attempted to an unreachable host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available; the socket cannot be connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a></b></dt>
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


For applications targeted to Windows Vista and later, consider using the <a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a> or <a href="https://msdn.microsoft.com/6d87699f-03bd-4579-9907-ae3c29b7332b">WSAConnectByName</a> function which greatly simplify client application design.

The 
<b>ConnectEx</b> function can only be used with connection-oriented sockets. The socket passed in the <i>s</i> parameter must be created with a socket type of <b>SOCK_STREAM</b>, <b>SOCK_RDM</b>, or <b>SOCK_SEQPACKET</b>.

The <i>lpSendBuffer</i> parameter points to a buffer of data to send after the connection is established. The <i>dwSendDataLength</i> parameter specifies the length in bytes of this data to send. An application can request to send a large buffer of data using the <b>ConnectEx</b> in the same way that the <a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> and <a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a> functions can be used. But developers are strongly advised against sending  a huge buffer in a single call using <b>ConnectEx</b>, because this operation uses a large amount of system memory resources until the whole buffer has been sent. 

If the <b>ConnectEx</b> function is successful, a connection was established and all of the data pointed to by the <i>lpSendBuffer</i> parameter was sent to the address specified in the <b>sockaddr</b> structure pointed to by the <i>name</i> parameter.


<div class="alert"><b>Note</b>  The function pointer for the 
<b>ConnectEx</b> function must be obtained at run time by making a call to the 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with the <b>SIO_GET_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_CONNECTEX</b>, a globally unique identifier (GUID) whose value identifies the <b>ConnectEx</b> extension function. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>ConnectEx</b> function. The <b>WSAID_CONNECTEX</b> GUID is defined in the <i>Mswsock.h</i> header file.</div>
<div> </div>


The 
<b>ConnectEx</b> function uses overlapped I/O. As a result, the 
<b>ConnectEx</b> function enables an application to service a large number of clients with relatively few threads. In contrast, the 
<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a> function, which does not use overlapped I/O, usually requires a separate thread to service each connection request when simultaneous  requests are received.<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> for more information.</div>
<div> </div>


Connection-oriented sockets are often unable to complete their connection immediately, and therefore the operation is initiated and the function immediately returns with the ERROR_IO_PENDING or WSA_IO_PENDING error. When the connect operation completes and success or failure is achieved, status is reported using the completion notification mechanism indicated in <i>lpOverlapped</i>. As with all overlapped function calls, you can use events or completion ports as the completion notification mechanism. The <i>lpNumberOfBytesTransferred</i> parameter of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa364986(v=VS.85).aspx">GetQueuedCompletionStatus</a> or 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a> function indicates the number of bytes sent in the request.

When the 
<b>ConnectEx</b> function successfully completes, socket handle <i>s</i> can be passed to only the following functions:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa365467(v=VS.85).aspx">ReadFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa365747(v=VS.85).aspx">WriteFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> or 
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> or 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>
</li>
<li>
<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>
</li>
</ul>


If the 
<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a> function is called on a previously connected socket with both TF_DISCONNECT and TF_REUSE_SOCKET flags, the specified socket is returned to a state in which it is not connected, but still bound. In such cases, the handle of the socket can be passed to the 
<b>ConnectEx</b> function in its <i>s</i> parameter, but the socket cannot be reused in an 
<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a> function call. Similarly, the accepted socket reused using the 
<b>TransmitFile</b> function cannot be used in a call to 
<b>ConnectEx</b>. Note that in the case of a reused socket, <b>ConnectEx</b> is subject to the behavior of the underlying transport. For example, a TCP socket may be subject to the TCP TIME_WAIT state, causing  the <b>ConnectEx</b> call to be delayed.

When the 
<b>ConnectEx</b> function returns <b>TRUE</b>, the socket <i>s</i> is in the default state for a connected socket. The socket <i>s</i> does not enable previously set properties or options until SO_UPDATE_CONNECT_CONTEXT is set on the socket. Use the 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> function to set the SO_UPDATE_CONNECT_CONTEXT option.

For example:


```cpp
//Need to #include <mswsock.h> for SO_UPDATE_CONNECT_CONTEXT

int iResult = 0;

iResult = setsockopt( s, SOL_SOCKET, SO_UPDATE_CONNECT_CONTEXT, NULL, 0 );

```


The 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> function can be used with the <b>SO_CONNECT_TIME</b> socket option to check whether a connection has been established while 
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
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> call is made, and then a 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a> call is made, Windows Sockets performs an implicit 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function call.</div>
<div> </div>


If the address parameter of the 
<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure pointed to in the <i>name</i> parameter is all zeros, 
<b>ConnectEx</b> returns the error <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEADDRNOTAVAIL</a>. Any attempt to reconnect an active connection will fail with the error code <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEISCONN</a>.

When a connected socket becomes closed for any reason, it is recommended that the socket be discarded and a new socket created. The reasoning for this is that it  is safest to assume that when things go awry on a connected socket for any reason, the application must discard teh socket and create the needed socket again in order to return to a stable point.

If the 
<a href="https://msdn.microsoft.com/220ba610-1694-470d-8b5e-e6b5fc3b4d0b">DisconnectEx</a> function is called with the <b>TF_REUSE_SOCKET</b> flag, the specified socket is returned to a state in which it is not connected, but still bound. In such cases, the handle of the socket can be passed to the 
<b>ConnectEx</b> function in its <i>s</i> parameter.

 The interval of  time that must elapse before TCP can release a closed connection and reuse its resources is known as the TIME_WAIT state or the  2MSL state. During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.

The TIME_WAIT behavior is specified in <a href="Http://go.microsoft.com/fwlink/p/?linkid=84069">RFC 793</a>, which requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (MSL) of the network. When a connection is released, its socket pair and internal resources used for the socket can be used to support another connection.

Windows TCP reverts to a TIME_WAIT state subsequent to the closing of a connection. While in the TIME_WAIT state, a socket pair cannot be reused. The TIME_WAIT period is configurable by modifying the following <b>DWORD</b> registry setting that represents the TIME_WAIT period in seconds. 


<b>HKEY_LOCAL_MACHINE</b>\<b>System</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>TCPIP</b>\<b>Parameters</b>\<b>TcpTimedWaitDelay</b>



By default, the MSL is defined to be 120 seconds. The TcpTimedWaitDelay registry setting defaults to a value 240 seconds, which represents 2 times the maximum segment lifetime of 120 seconds or 4 minutes. However, you can use this entry to customize the interval.

Reducing the value of this entry allows TCP to release closed connections faster, providing more resources for new connections. However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to re-establish the connection.

This registry setting can be set from 0 to 300 seconds.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>



<a href="https://msdn.microsoft.com/220ba610-1694-470d-8b5e-e6b5fc3b4d0b">DisconnectEx</a>



<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa364986(v=VS.85).aspx">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa365467(v=VS.85).aspx">ReadFile</a>



<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>



<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>



<a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a>



<a href="https://msdn.microsoft.com/6d87699f-03bd-4579-9907-ae3c29b7332b">WSAConnectByName</a>



<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>



<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>



<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>



<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>



<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa365747(v=VS.85).aspx">WriteFile</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>



<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>



<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>



<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>



<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a>



<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a>
 

 

