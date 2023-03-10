---
UID: NF:mswsock.WSARecvEx
title: WSARecvEx function (mswsock.h)
description: The WSARecvEx function (mswsock.h) receives data from a connected socket or a bound connectionless socket.
helpviewer_keywords: ["WSARecvEx","WSARecvEx function [Winsock]","_win32_wsarecvex_2","winsock.wsarecvex_2","winsock/WSARecvEx"]
old-location: winsock\wsarecvex_2.htm
tech.root: WinSock
ms.assetid: 0ed639f7-e7bd-49a2-a7c0-177699a2cf5e
ms.date: 08/12/2022
ms.keywords: WSARecvEx, WSARecvEx function [Winsock], _win32_wsarecvex_2, winsock.wsarecvex_2, winsock/WSARecvEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSARecvEx
 - mswsock/WSARecvEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mswsock.dll
api_name:
 - WSARecvEx
---

# WSARecvEx function


## -description

The 
<b>WSARecvEx</b> function receives data from a connected socket or a bound connectionless socket. The <b>WSARecvEx</b> function is similar to the 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> function, except that the <i>flags</i> parameter is used only to return information. When a partial message is received while using datagram protocol, the MSG_PARTIAL bit is set in the <i>flags</i> parameter on return from the function.
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
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

<div class="alert"><b>Important</b>  For a stream oriented-transport protocol, MSG_PARTIAL is never set on return from 
<b>WSARecvEx</b>. This function behaves identically to the 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> function for stream-transport protocols.</div>
<div> </div>
<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was terminated due to a time-out or other failure. The application should close the socket as it is no longer usable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was reset by the remote side executing a hard or abortive close. The application should close the socket as it is no longer usable. On a UPD-datagram socket this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>buf</i> parameter is not completely contained in a valid part of the user address space.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The (blocking) call was canceled by the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound with 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, or an unknown flag was specified, or MSG_OOB was specified for a socket with SO_OOBINLINE enabled or (for byte stream sockets only) <i>len</i> was zero or negative.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a connection-oriented socket, this error indicates that the connection has been broken due to <i>keep-alive</i> activity that detected a failure while the operation was in progress. For a datagram socket, this error indicates that the time to live has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
MSG_OOB was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, or the socket is unidirectional and supports only send operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to use 
<a href="/windows/desktop/api/mswsock/nf-mswsock-wsarecvex">WSARecvEx</a> on a socket after 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> has been invoked with <i>how</i> set to SD_RECEIVE or SD_BOTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been dropped because of a network failure or because the peer system failed to respond.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking and the receive operation would block.

</td>
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
</table>

## -remarks

The 
<b>WSARecvEx</b> function that is part of the Microsoft implementation of Windows Sockets 2 is similar to the more common 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> function except that the <i>flags</i> parameter is used for a single specific purpose. The <i>flags</i> parameter is used to indicate whether a partial or complete message is received when a message-oriented protocol is being used. 

The value pointed to by the <i>flags</i> parameter is ignored on input. So no flags can be passed to the  <b>WSARecvEx</b> function to modify its behavior. The value pointed to by the <i>flags</i> parameter is set on output. This differs from the <a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> functions where the  value pointed to by the <i>flags</i> parameter on input can modify the behavior of the function.

The 
<b>WSARecvEx</b> and 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> functions behave identically for stream-oriented protocols.

The <i>flags</i> parameter accommodates two common situations in which a partial message will be received:

<ul>
<li>When the application's data buffer size is smaller than the message size and the message coincidentally arrives in two pieces.</li>
<li>When the message is rather large and must arrive in several pieces.</li>
</ul>
The MSG_PARTIAL bit is set in the value pointed to by the <i>flags</i> parameter on return from 
<b>WSARecvEx</b> when a partial message was received. If a complete message was received, MSG_PARTIAL is not set in the value pointed to by the <i>flags</i> parameter.

The 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> function is different from the  
<b>WSARecvEx</b> and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a> functions in that the 
<b>recv</b> function always receives a single message for each call for message-oriented transport protocols. The 
<b>recv</b> function also does not have a means to indicate to the application that the data received is only a partial message. An application must build its own protocol for checking whether a message is partial or complete by checking for the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a> after each call to 
<b>recv</b>. When the application buffer is smaller than the data being sent, as much of the message as will fit is copied into the user's buffer and 
<b>recv</b> returns with the error code WSAEMSGSIZE. A subsequent call to 
<b>recv</b> will get the next part of the message.

Applications written for message-oriented transport protocols should be coded for this possibility if message sizing is not guaranteed by the application's data transfer protocol. An application can use 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> and manage the protocol itself. Alternatively, an application can use 
<b>WSARecvEx</b> and check that the MSG_PARTIAL bit is set in the <i>flags</i> parameter.

The 
<b>WSARecvEx</b> function provides the developer with a more effective way of checking whether a message received is partial or complete when a very large message arrives incrementally. For example, if an application sends a one-megabyte message, the transport protocol must break up the message in order to send it over the physical network. It is theoretically possible for the transport protocol on the receiving side to buffer all the data in the message, but this would be quite expensive in terms of resources. Instead, 
<b>WSARecvEx</b> can be used, minimizing overhead and eliminating the need for an application-based protocol.

<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> function for more information.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-select">select</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
