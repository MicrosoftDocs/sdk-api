---
UID: NF:winsock2.WSAConnect
title: WSAConnect function
author: windows-sdk-content
description: The WSAConnect function establishes a connection to another socket application, exchanges connect data, and specifies required quality of service based on the specified FLOWSPEC structure.
old-location: winsock\wsaconnect_2.htm
tech.root: winsock
ms.assetid: 3b32cc6e-3df7-4104-a0d4-317fd445c7b2
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WSAConnect, WSAConnect function [Winsock], _win32_wsaconnect_2, winsock.wsaconnect_2, winsock2/WSAConnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAConnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WSAConnect
: 
---

# WSAConnect function


## -description


The 
<b>WSAConnect</b> function establishes a connection to another socket application, exchanges connect data, and specifies required quality of service based on the specified 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure.


## -parameters




### -param s [in]

A descriptor identifying an unconnected socket.


### -param name [in]

A pointer to a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure  that specifies the address to which to connect. For  IPv4, the <b>sockaddr</b> contains <b>AF_INET</b> for the address family, the destination IPv4 address, and the destination port. For  IPv6, the <b>sockaddr</b> structure contains <b>AF_INET6</b> for the address family, the destination IPv6 address, the destination port, and may contain additional flow and scope-id information. 


### -param namelen [in]

The length, in bytes, of the <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure pointed to by the <i>name</i> parameter.


### -param lpCallerData [in]

A pointer to the user data that is to be transferred to the other socket during connection establishment. See Remarks.


### -param lpCalleeData [out]

A pointer to the user data that is to be transferred back from the other socket during connection establishment. See Remarks.


### -param lpSQOS [in]

A pointer to the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for socket <i>s</i>, one for each direction.


### -param lpGQOS [in]

Reserved for future use with socket groups. A pointer to the 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for the socket group (if applicable). This parameter should be <b>NULL</b>.


## -returns



If no error occurs, 
<b>WSAConnect</b> returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>. On a blocking socket, the return value indicates success or failure of the connection attempt.

With a nonblocking socket, the connection attempt cannot be completed immediately. In this case, 
<b>WSAConnect</b> will return SOCKET_ERROR, and 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> will return 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a>; the application could therefore:

<ul>
<li>Use 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> to determine the completion of the connection request by checking if the socket is writeable.</li>
<li>If your application is using 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> to indicate interest in connection events, then your application will receive an FD_CONNECT notification when the connect operation is complete(successful or not).</li>
<li>If your application is using 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> to indicate interest in connection events, then the associated event object will be signaled when the connect operation is complete (successful or not).</li>
</ul>
For a nonblocking socket, until the connection attempt completes all subsequent calls to 
<b>WSAConnect</b> on the same socket will fail with the error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEALREADY</a>.

If the return error code indicates the connection attempt failed (that is, 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNREFUSED</a>, 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETUNREACH</a>, 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a>) the application can call 
<b>WSAConnect</b> again for the same socket.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

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
The local address of the socket is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs during the execution of 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, but could be delayed until this function if the 
<b>bind</b> function operates on a partially wildcard address (involving ADDR_ANY) and if a specific address needs to be "committed" at the time of this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The (blocking) Windows Socket 1.1 call was canceled through 
<a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

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
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> or <a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a> call is in progress on the specified socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address (such as ADDR_ANY).

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
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, the <i>namelen</i> parameter is too small, the buffer length for <i>lpCalleeData</i>, <i>lpSQOS</i>, and <i>lpGQOS</i> are too small, or the buffer length for <i>lpCallerData</i> is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>s</i> is a listening socket, or the destination address specified is not consistent with that of the constrained group to which the socket belongs, or the <i>lpGQOS</i> parameter is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is already connected (connection-oriented sockets only).

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
No buffer space is available. The socket cannot be connected.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures specified in <i>lpSQOS</i> and <i>lpGQOS</i> cannot be satisfied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEPROTONOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpCallerData</i> parameter is not supported by the service provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
Attempt to connect timed out without establishing a connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the connection cannot be completed immediately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
Attempt to connect datagram socket to broadcast address failed because 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> SO_BROADCAST is not enabled.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAConnect</b> function is used to create a connection to the specified destination, and to perform a number of other ancillary operations that occur at connect time. If the socket, <i>s</i>, is unbound, unique values are assigned to the local association by the system, and the socket is marked as bound.

For applications targeted to Windows Vista and later, consider using the <a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a> or <a href="https://msdn.microsoft.com/6d87699f-03bd-4579-9907-ae3c29b7332b">WSAConnectByName</a> function which greatly simplify client application design.

For connection-oriented sockets (for example, type SOCK_STREAM), an active connection is initiated to the foreign host using <i>name</i> (an address in the namespace of the socket; for a detailed description, please see 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>). When this call completes successfully, the socket is ready to send/receive data. If the address parameter of the <i>name</i> structure is all zeroes, 
<b>WSAConnect</b> will return the error 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEADDRNOTAVAIL</a>. Any attempt to reconnect an active connection will fail with the error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEISCONN</a>.

<div class="alert"><b>Note</b>  If a socket is opened, a 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> call is made, and then a 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a> call is made, Windows Sockets performs an implicit 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> function call.</div>
<div> </div>
For connection-oriented, nonblocking sockets, it is often not possible to complete the connection immediately. In such cases, this function returns the error 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a>. However, the operation proceeds. When the success or failure outcome becomes known, it may be reported in one of several ways depending on how the client registers for notification. If the client uses 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>, success is reported in the <i>writefds</i> set and failure is reported in the <i>exceptfds</i> set. If the client uses 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> or 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>, the notification is announced with FD_CONNECT and the error code associated with the FD_CONNECT indicates either success or a specific reason for failure.

For a connectionless socket (for example, type SOCK_DGRAM), the operation performed by 
<b>WSAConnect</b> is merely to establish a default destination address so that the socket can be used on subsequent connection-oriented send and receive operations (<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>, 
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>, 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>, and 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>). Any datagrams received from an address other than the destination address specified will be discarded. If the entire name structure is all zeros (not just the address parameter of the name structure), then the socket will be disconnected. Then, the default remote address will be indeterminate, so <b>send</b>, <b>WSASend</b>, <b>recv</b>, and <b>WSARecv</b> calls will return the error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTCONN</a>. However, 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>,
				<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>, <a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a>, and 
				<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a> can still be used. The default destination can be changed by simply calling 
<b>WSAConnect</b> again, even if the socket is already connected. Any datagrams queued for receipt are discarded if <i>name</i> is different from the previous 
<b>WSAConnect</b>.

For connectionless sockets, <i>name</i> can indicate any valid address, including a broadcast address. However, to connect to a broadcast address, a socket must have 
<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> SO_BROADCAST enabled. Otherwise, 
<b>WSAConnect</b> will fail with the error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEACCES</a>.

On connectionless sockets, exchange of user-to-user data is not possible and the corresponding parameters will be silently ignored.

The application is responsible for allocating any memory space pointed to directly or indirectly by any of the parameters it specifies.

The <i>lpCallerData</i> parameter contains a pointer to any user data that is to be sent along with the connection request (called connect data). This is additional data, not in the normal network data stream, that is sent with network requests to establish a connection. This option is used by legacy protocols such as DECNet, OSI TP4, and others. <div class="alert"><b>Note</b>  Connect data is not supported by the TCP/IP protocol in Windows. Connect data is supported only on ATM (RAWWAN) over a raw socket. </div>
<div> </div>


If <i>lpCallerData</i> is <b>NULL</b>, no user data will be passed to the peer. The <i>lpCalleeData</i> is a result parameter that will contain any user data passed back from the other socket as part of the connection establishment in a 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structure. The <b>len</b> member of the <b>WSABUF</b> structure pointed to by the <i>lpCalleeData</i> parameter initially contains the length of the buffer allocated by the application for the <b>buf</b> member of the <b>WSABUF</b> structure. The <b>len</b> member of the <b>WSABUF</b> structure pointed to by the <i>lpCalleeData</i> parameter will be set to zero if no user data has been passed back. The <i>lpCalleeData</i> information will be valid when the connection operation is complete. For blocking sockets, the connection operation completes when the 
<b>WSAConnect</b> function returns. For nonblocking sockets, completion will be after the FD_CONNECT notification has occurred. If <i>lpCalleeData</i> is <b>NULL</b>, no user data will be passed back. The exact format of the user data is specific to the address family to which the socket belongs.

At connect time, an application can use the <i>lpSQOS</i> and <i>lpGQOS</i> parameter to override any previous quality of service specification made for the socket through 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> with either the SIO_SET_QOS or SIO_SET_GROUP_QOS opcode.

The <i>lpSQOS</i> parameter specifies the 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for socket <i>s</i>, one for each direction, followed by any additional provider-specific parameters. If either the associated transport provider in general or the specific type of socket in particular cannot honor the quality of service request, an error will be returned as indicated in the following. The sending or receiving flow specification values will be ignored, respectively, for any unidirectional sockets. If no provider-specific parameters are specified, the <b>buf</b> and <b>len</b> members of the <a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structure pointed to by the <i>lpCalleeData</i> parameter  should be set to <b>NULL</b> and zero, respectively. A <b>NULL</b> value for <i>lpSQOS</i> parameter indicates no application-supplied quality of service.

Reserved for future use with socket groups <i>lpGQOS</i> specifies the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for the socket group (if applicable), one for each direction, followed by any additional provider-specific parameters. If no provider-specific parameters are specified, the <b>buf</b> and <b>len</b> members of the <a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structure pointed to by the <i>lpCalleeData</i> parameter   should be set to <b>NULL</b> and zero, respectively. A <b>NULL</b> value for <i>lpGQOS</i> indicates no application-supplied group quality of service. This parameter will be ignored if <i>s</i> is not the creator of the socket group.

When connected sockets become closed for whatever reason, they should be discarded and recreated. It is safest to assume that when things go awry for any reason on a connected socket, the application must discard and recreate the needed sockets in order to return to a stable point.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSAConnect</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a>



<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>



<a href="https://msdn.microsoft.com/7323d814-e96e-44b9-8ade-a9317e4fbf17">WSAConnectByList</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/be20a731-cdfc-48ae-90b2-43f2cf9ecf6d">getsockname</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

