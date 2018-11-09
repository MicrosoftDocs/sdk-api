---
UID: NF:mswsock.WSARecvEx
title: WSARecvEx function
author: windows-sdk-content
description: Receives data from a connected socket or a bound connectionless socket.
old-location: winsock\wsarecvex_2.htm
tech.root: winsock
ms.assetid: 0ed639f7-e7bd-49a2-a7c0-177699a2cf5e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WSARecvEx, WSARecvEx function [Winsock], _win32_wsarecvex_2, winsock.wsarecvex_2, winsock/WSARecvEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mswsock.h
req.include-header: Mswsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mswsock.lib
req.dll: Mswsock.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - WSARecvEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSARecvEx function


## -description


The 
<b>WSARecvEx</b> function receives data from a connected socket or a bound connectionless socket. The <b>WSARecvEx</b> function is similar to the 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function, except that the <i>flags</i> parameter is used only to return information. When a partial message is received while using datagram protocol, the MSG_PARTIAL bit is set in the <i>flags</i> parameter on return from the function.
<div class="alert"><b>Note</b>  The 
<b>WSARecvEx</b> function is a Microsoft-specific extension to the Windows Sockets specification.</div><div> </div>

## -parameters




### -param s [in]

A descriptor that identifies a connected socket.


### -param buf [out]

A pointer to the buffer to receive the incoming data.


### -param len [in]

The length, in bytes, of the buffer pointed to by the <i>buf</i> parameter.


### -param flags [in, out]

An indicator specifying whether the message is fully or partially received for datagram sockets.


## -returns



If no error occurs, 
<b>WSARecvEx</b> returns the number of bytes received. If the connection has been closed, it returns zero. Additionally, if a partial message was received, the MSG_PARTIAL bit is set in the <i>flags</i> parameter. If a complete message was received, MSG_PARTIAL is not set in <i>flags</i>

Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<div class="alert"><b>Important</b>  For a stream oriented-transport protocol, MSG_PARTIAL is never set on return from 
<b>WSARecvEx</b>. This function behaves identically to the 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function for stream-transport protocols.</div>
<div> </div>
<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was terminated due to a time-out or other failure. The application should close the socket as it is no longer usable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was reset by the remote side executing a hard or abortive close. The application should close the socket as it is no longer usable. On a UPD-datagram socket this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> parameter is not completely contained in a valid part of the user address space.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The (blocking) call was canceled by the <a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound with 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, or an unknown flag was specified, or MSG_OOB was specified for a socket with SO_OOBINLINE enabled or (for byte stream sockets only) <i>len</i> was zero or negative.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a connection-oriented socket, this error indicates that the connection has been broken due to <i>keep-alive</i> activity that detected a failure while the operation was in progress. For a datagram socket, this error indicates that the time to live has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.

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
MSG_OOB was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, or the socket is unidirectional and supports only send operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to use 
<a href="https://msdn.microsoft.com/0ed639f7-e7bd-49a2-a7c0-177699a2cf5e">WSARecvEx</a> on a socket after 
<a href="https://msdn.microsoft.com/6998f0c6-adc9-481f-b9fb-75f9c9f5caaf">shutdown</a> has been invoked with <i>how</i> set to SD_RECEIVE or SD_BOTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been dropped because of a network failure or because the peer system failed to respond.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the receive operation would block.

</td>
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
</table>
 




## -remarks



The 
<b>WSARecvEx</b> function that is part of the Microsoft implementation of Windows Sockets 2 is similar to the more common 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function except that the <i>flags</i> parameter is used for a single specific purpose. The <i>flags</i> parameter is used to indicate whether a partial or complete message is received when a message-oriented protocol is being used. 

The value pointed to by the <i>flags</i> parameter is ignored on input. So no flags can be passed to the  <b>WSARecvEx</b> function to modify its behavior. The value pointed to by the <i>flags</i> parameter is set on output. This differs from the <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> and <a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> functions where the  value pointed to by the <i>flags</i> parameter on input can modify the behavior of the function.

The 
<b>WSARecvEx</b> and 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> functions behave identically for stream-oriented protocols.

The <i>flags</i> parameter accommodates two common situations in which a partial message will be received:

<ul>
<li>When the application's data buffer size is smaller than the message size and the message coincidentally arrives in two pieces.</li>
<li>When the message is rather large and must arrive in several pieces.</li>
</ul>
The MSG_PARTIAL bit is set in the value pointed to by the <i>flags</i> parameter on return from 
<b>WSARecvEx</b> when a partial message was received. If a complete message was received, MSG_PARTIAL is not set in the value pointed to by the <i>flags</i> parameter.

The 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function is different from the  
<b>WSARecvEx</b> and <a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> functions in that the 
<b>recv</b> function always receives a single message for each call for message-oriented transport protocols. The 
<b>recv</b> function also does not have a means to indicate to the application that the data received is only a partial message. An application must build its own protocol for checking whether a message is partial or complete by checking for the error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEMSGSIZE</a> after each call to 
<b>recv</b>. When the application buffer is smaller than the data being sent, as much of the message as will fit is copied into the user's buffer and 
<b>recv</b> returns with the error code WSAEMSGSIZE. A subsequent call to 
<b>recv</b> will get the next part of the message.

Applications written for message-oriented transport protocols should be coded for this possibility if message sizing is not guaranteed by the application's data transfer protocol. An application can use 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> and manage the protocol itself. Alternatively, an application can use 
<b>WSARecvEx</b> and check that the MSG_PARTIAL bit is set in the <i>flags</i> parameter.

The 
<b>WSARecvEx</b> function provides the developer with a more effective way of checking whether a message received is partial or complete when a very large message arrives incrementally. For example, if an application sends a one-megabyte message, the transport protocol must break up the message in order to send it over the physical network. It is theoretically possible for the transport protocol on the receiving side to buffer all the data in the message, but this would be quite expensive in terms of resources. Instead, 
<b>WSARecvEx</b> can be used, minimizing overhead and eliminating the need for an application-based protocol.

<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See the <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> function for more information.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>



<a href="https://msdn.microsoft.com/3e4282e0-3ed0-43e7-9b27-72ec36b9cfa1">recvfrom</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>



<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

