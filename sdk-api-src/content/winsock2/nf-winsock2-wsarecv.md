---
UID: NF:winsock2.WSARecv
title: WSARecv function
author: windows-sdk-content
description: Receives data from a connected socket or a bound connectionless socket.
old-location: winsock\wsarecv_2.htm
tech.root: winsock
ms.assetid: bfe66e11-e9a7-4321-ad55-3141113e9a03
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSARecv, WSARecv function [Winsock], _win32_wsarecv_2, winsock.wsarecv_2, winsock2/WSARecv
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
 - WSARecv
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSARecv function


## -description


The 
<b>WSARecv</b> function receives data from a connected socket or a bound connectionless socket.


## -parameters




### -param s [in]

A  descriptor identifying a connected socket.


### -param lpBuffers [in, out]

A pointer to an array of 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structures. Each 
<b>WSABUF</b> structure contains a pointer to a buffer and the length, in bytes, of the buffer.


### -param dwBufferCount [in]

The number of 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structures in the <i>lpBuffers</i> array.


### -param lpNumberOfBytesRecvd [out]

A pointer to the number, in bytes, of data received by this call if the receive operation completes immediately. 

Use <b>NULL</b> for this parameter if the <i>lpOverlapped</i> parameter is not <b>NULL</b> to avoid potentially erroneous results. This parameter can be <b>NULL</b> only  if the <i>lpOverlapped</i> parameter is not <b>NULL</b>.


### -param lpFlags [in, out]

A pointer to flags used to modify the behavior of the 
<b>WSARecv</b> function call. For more information, see the Remarks section.


### -param lpOverlapped [in]

A pointer to a 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure (ignored for nonoverlapped sockets).


### -param lpCompletionRoutine [in]

A pointer to the completion routine called when the receive operation has been completed (ignored for nonoverlapped sockets).


## -returns



If no error occurs and the receive operation has completed immediately, 
<b>WSARecv</b> returns zero. In this case, the completion routine will have already been scheduled to be called once the calling thread is in the alertable state. Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>. The error code 
<a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a> indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that the overlapped operation was not successfully initiated and no completion indication will occur.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was terminated due to a time-out or other failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a stream socket, the virtual circuit was reset by the remote side. The application should close the socket as it is no longer usable. For a UDP datagram socket, this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEDISCON</a></b></dt>
</dl>
</td>
<td width="60%">
Socket <i>s</i> is message oriented and the virtual circuit was gracefully closed by the remote side.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffers</i> parameter is not completely contained in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The (blocking) call was canceled by the <a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound (for example, with 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
The message was too large to fit into the specified buffer and (for unreliable protocols only) any trailing portion of the message that did not fit into the buffer has been discarded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a connection-oriented socket, this error indicates that the connection has been broken due to <i>keep-alive</i> activity that detected a failure while the operation was in progress. For a datagram socket, this error indicates that the time to live has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
<b>MSG_OOB</b> was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, or the socket is unidirectional and supports only send operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to call 
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> on a socket after 
<a href="https://msdn.microsoft.com/6998f0c6-adc9-481f-b9fb-75f9c9f5caaf">shutdown</a> has been invoked with <i>how</i> set to <b>SD_RECEIVE</b> or <b>SD_BOTH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been dropped because of a network failure or because the peer system failed to respond.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">

<b>Windows NT:  </b>Overlapped sockets: there are too many outstanding overlapped I/O requests. Nonoverlapped sockets: The socket is marked as nonblocking and the receive operation cannot be completed immediately.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped operation was successfully initiated and completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_OPERATION_ABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The overlapped operation has been canceled due to the closure of the socket.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSARecv</b> function provides some additional features compared with the standard 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function in three important areas:

<ul>
<li>It can be used in conjunction with overlapped sockets to perform overlapped 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> operations.</li>
<li>It allows multiple receive buffers to be specified making it applicable to the scatter/gather type of I/O.</li>
<li>The <i>lpFlags</i> parameter is used both on input and returned on output, allowing applications to sense the output state of the <b>MSG_PARTIAL</b> flag bit. However, the <b>MSG_PARTIAL</b> flag bit is not supported by all protocols.</li>
</ul>
The 
<b>WSARecv</b> function is used on connected sockets or bound connectionless sockets specified by the <i>s</i> parameter and is used to read incoming data. The socket's local address must be known. For server applications, this is usually done explicitly through 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a> or implicitly through 
<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a> or 
<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>. Explicit binding is discouraged for client applications. For client applications the socket can become bound implicitly to a local address through 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>, 
<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>, 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>, 
<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>, or 
<a href="https://msdn.microsoft.com/ef9efa03-feed-4f0d-b874-c646cce745c9">WSAJoinLeaf</a>.

For connected, connectionless sockets, this function restricts the addresses from which received messages are accepted. The function only returns messages from the remote address specified in the connection. Messages from other addresses are (silently) discarded.

For overlapped sockets, 
<b>WSARecv</b> is used to post one or more buffers into which incoming data will be placed as it becomes available, after which the application-specified completion indication (invocation of the completion routine or setting of an event object) occurs. If the operation does not complete immediately, the final completion status is retrieved through the completion routine or 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>.

<div class="alert"><b>Note</b>  All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> for more information.</div>
<div> </div>
If both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b>, the socket in this function will be treated as a nonoverlapped socket.

For nonoverlapped sockets, the blocking semantics are identical to that of the standard 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function and the <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> parameters are ignored. Any data that has already been received and buffered by the transport will be copied into the specified user buffers. In the case of a blocking socket with no data currently having been received and buffered by the transport, the call will block until data is received. Windows Sockets 2 does not define any standard blocking time-out mechanism for this function. For protocols acting as byte-stream protocols the stack tries to return as much data as possible subject to the available buffer space and amount of received data available. However, receipt of a single byte is sufficient to unblock the caller. There is no guarantee that more than a single byte will be returned. For protocols acting as message-oriented, a full message is required to unblock the caller.

<div class="alert"><b>Note</b>  The socket options <b>SO_RCVTIMEO</b> and <b>SO_SNDTIMEO</b> apply only to blocking sockets.</div>
<div> </div>
Whether or not a protocol is acting as byte stream is determined by the setting of XP1_MESSAGE_ORIENTED and XP1_PSEUDO_STREAM in its 
<a href="https://msdn.microsoft.com/758c5553-056f-4ea5-a851-30ef641ffb14">WSAPROTOCOL_INFO</a> structure and the setting of the MSG_PARTIAL flag passed in to this function (for protocols that support it). The following table lists relevant combinations, (an asterisk (*) indicates that the setting of this bit does not matter in this case).


<table>
<tr>
<th>XP1_MESSAGE_ORIENTED</th>
<th>XP1_PSEUDO_STREAM</th>
<th>MSG_PARTIAL</th>
<th>Acts as</th>
</tr>
<tr>
<td>not set</td>
<td>*</td>
<td>*</td>
<td>Byte stream</td>
</tr>
<tr>
<td>*</td>
<td>Set</td>
<td>*</td>
<td>Byte stream</td>
</tr>
<tr>
<td>set</td>
<td>Not set</td>
<td>set</td>
<td>Byte stream</td>
</tr>
<tr>
<td>set</td>
<td>Not set</td>
<td>not set</td>
<td>Message oriented</td>
</tr>
</table>
 



The buffers are filled in the order in which they appear in the array pointed to by <i>lpBuffers</i>, and the buffers are packed so that no holes are created.

If this function is completed in an overlapped manner, it is the Winsock service provider's responsibility to capture the 
<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structures before returning from this call. This enables applications to build stack-based 
<b>WSABUF</b> arrays pointed to by the <i>lpBuffers</i> parameter.

For byte stream-style sockets (for example, type <b>SOCK_STREAM</b>), incoming data is placed into the buffers until the buffers are filled, the connection is closed, or the internally buffered data is exhausted. Regardless of whether or not the incoming data fills all the buffers, the completion indication occurs for overlapped sockets.

For message-oriented sockets (for example, type <b>SOCK_DGRAM</b>), an incoming message is placed into the buffers up to the total size of the buffers, and the completion indication occurs for overlapped sockets. If the message is larger than the buffers, the buffers are filled with the first part of the message. If the <b>MSG_PARTIAL</b> feature is supported by the underlying service provider, the <b>MSG_PARTIAL</b> flag is set in <i>lpFlags</i> and subsequent receive operations will retrieve the rest of the message. If <b>MSG_PARTIAL</b> is not supported but the protocol is reliable, 
<b>WSARecv</b> generates the error 
<a href="windows_sockets_error_codes_2.htm">WSAEMSGSIZE</a> and a subsequent receive operation with a larger buffer can be used to retrieve the entire message. Otherwise, (that is, the protocol is unreliable and does not support <b>MSG_PARTIAL</b>), the excess data is lost, and 
<b>WSARecv</b> generates the error WSAEMSGSIZE.

For connection-oriented sockets, 
<b>WSARecv</b> can indicate the graceful termination of the virtual circuit in one of two ways that depend on whether the socket is byte stream or message oriented. For byte streams, zero bytes having been read (as indicated by a zero return value to indicate success, and <i>lpNumberOfBytesRecvd</i> value of zero) indicates graceful closure and that no more bytes will ever be read. For message-oriented sockets, where a zero byte message is often allowable, a failure with an error code of 
<a href="windows_sockets_error_codes_2.htm">WSAEDISCON</a> is used to indicate graceful closure. In any case a return error code of 
<a href="windows_sockets_error_codes_2.htm">WSAECONNRESET</a> indicates an abortive close has occurred.

The <i>lpFlags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. That is, the semantics of this function are determined by the socket options and the <i>lpFlags</i> parameter. The latter is constructed by using the bitwise OR operator with any of the values listed in the following table.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MSG_PEEK</td>
<td>
Peeks at the incoming data. The data is copied into the buffer, but is not removed from the input queue.

This flag is valid only for nonoverlapped sockets.

</td>
</tr>
<tr>
<td>MSG_OOB</td>
<td>Processes OOB data.</td>
</tr>
<tr>
<td>MSG_PARTIAL</td>
<td>
This flag is for message-oriented sockets only. On output, this flag indicates that the data specified is a portion of the message transmitted by the sender. Remaining portions of the message will be specified in subsequent receive operations. A subsequent receive operation with the <b>MSG_PARTIAL</b> flag cleared indicates end of sender's message.

As an input parameter, this flag indicates that the receive operation should complete even if only part of a message has been received by the transport  provider.

</td>
</tr>
<tr>
<td>MSG_PUSH_IMMEDIATE</td>
<td>
This flag is for stream-oriented sockets only. This flag allows an application that uses stream sockets to tell the  transport provider not to delay completion of partially filled pending receive requests. This is a hint to the transport provider that the application is willing to receive any incoming data as soon as possible without necessarily waiting for the remainder of the data that might still be in transit. What constitutes a partially filled pending receive request is a transport-specific matter. 

In the case of TCP, this refers to the case of incoming TCP segments being placed into the receive request data buffer where none of the TCP segments indicated a PUSH bit value of 1. In this case, TCP may hold the partially filled receive request a little longer to allow the remainder of the data to arrive with a TCP segment that has the PUSH bit set to 1. This flag tells TCP not to hold the receive request but to complete it immediately.

 Using this flag for large block transfers is not recommended since processing partial blocks is often not optimal. This flag is useful only for cases where receiving and processing the partial data immediately helps decrease processing latency.

This flag is a hint rather than an actual guarantee.

This flag is supported on Windows 8.1, Windows Server 2012 R2, and later.

</td>
</tr>
<tr>
<td>MSG_WAITALL</td>
<td>
The receive request will complete only when one of the following events occurs:<ul>
<li>The buffer supplied by the caller is completely full.</li>
<li>The connection has been closed.</li>
<li>The request has been canceled or an error occurred.</li>
</ul>


Be aware that if the underlying transport provider does not support <b>MSG_WAITALL</b>, or if the socket is in a non-blocking mode, then this call will fail with <b>WSAEOPNOTSUPP</b>. Also, if <b>MSG_WAITALL</b> is specified along with <b>MSG_OOB</b>, <b>MSG_PEEK</b>, or <b>MSG_PARTIAL</b>, then this call will fail with <b>WSAEOPNOTSUPP</b>.

This flag is not supported on datagram sockets or message-oriented sockets.

</td>
</tr>
</table>
 



For message-oriented sockets, the <b>MSG_PARTIAL</b> bit is set in the <i>lpFlags</i> parameter if a partial message is received. If a complete message is received, <b>MSG_PARTIAL</b> is cleared in <i>lpFlags</i>. In the case of delayed completion, the value pointed to by <i>lpFlags</i> is not updated. When completion has been indicated, the application should call 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a> and examine the flags indicated by the <i>lpdwFlags</i> parameter.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSARecv</b> with the <i>lpOverlapped</i> parameter set to NULL, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Overlapped_Socket_I_O"></a><a id="overlapped_socket_i_o"></a><a id="OVERLAPPED_SOCKET_I_O"></a>Overlapped Socket I/O</h3>
If an overlapped operation completes immediately, 
<b>WSARecv</b> returns a value of zero and the <i>lpNumberOfBytesRecvd</i> parameter is updated with the number of bytes received and the flag bits indicated by the <i>lpFlags</i> parameter are also updated. If the overlapped operation is successfully initiated and will complete later, 
<b>WSARecv</b> returns <b>SOCKET_ERROR</b> and indicates error code 
<a href="windows_sockets_error_codes_2.htm">WSA_IO_PENDING</a>. In this case, <i>lpNumberOfBytesRecvd</i> and <i>lpFlags</i> are not updated. When the overlapped operation completes, the amount of data transferred is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>. Flag values are obtained by examining the <i>lpdwFlags</i> parameter of 
<b>WSAGetOverlappedResult</b>.

The 
<b>WSARecv</b> function using overlapped I/O can be called from within the completion routine of a previous 
<b>WSARecv</b>, 
<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a>, 
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a> or 
<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a> function. For a given socket, I/O completion routines will not be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. If multiple I/O operations are simultaneously outstanding, each must reference a separate 
<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structure.

If the <i>lpCompletionRoutine</i> parameter is <b>NULL</b>, the <i>hEvent</i> parameter of <i>lpOverlapped</i> is signaled when the overlapped operation completes if it contains a valid event object handle. An application can use 
<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a> or 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a> to wait or poll on the event object.

If <i>lpCompletionRoutine</i> is not <b>NULL</b>, the <i>hEvent</i> parameter is ignored and can be used by the application to pass context information to the completion routine. A caller that passes a non-<b>NULL</b> <i>lpCompletionRoutine</i> and later calls 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of 
<b>WSAGetOverlappedResult</b> to <b>TRUE</b>. In this case the usage of the <i>hEvent</i> parameter is undefined, and attempting to wait on the <i>hEvent</i> parameter would produce unpredictable results.

The completion routine follows the same rules as stipulated for Windows file I/O completion routines. The completion routine will not be invoked until the thread is in an alertable wait state such as can occur when the function 
<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a> with the <i>fAlertable</i> parameter set to <b>TRUE</b> is invoked.

The prototype of the completion routine is as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
void CALLBACK CompletionROUTINE(
  IN DWORD dwError, 
  IN DWORD cbTransferred, 
  IN LPWSAOVERLAPPED lpOverlapped, 
  IN DWORD dwFlags
);
</pre>
</td>
</tr>
</table></span></div>
CompletionRoutine is a placeholder for an application-defined or library-defined function name. The <i>dwError</i> specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. The <i>cbTransferred</i> parameter specifies the number of bytes received. The <i>dwFlags</i> parameter contains information that would have appeared in <i>lpFlags</i> if the receive operation had completed immediately. This function does not return a value.

Returning from this function allows invocation of another pending completion routine for this socket. When using 
<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a>, all waiting completion routines are called before the alertable thread's wait is satisfied with a return code of <b>WSA_IO_COMPLETION</b>. The completion routines can be called in any order, not necessarily in the same order the overlapped operations are completed. However, the posted buffers are guaranteed to be filled in the same order in which they are specified.

If you are using I/O completion ports, be aware that the order of calls made to <b>WSARecv</b> is also the order in which the buffers are populated. <b>WSARecv</b> should not be called on the same socket simultaneously from different threads, because it can result in an unpredictable buffer order.

<h3><a id="Example_Code"></a><a id="example_code"></a><a id="EXAMPLE_CODE"></a>Example Code</h3>
The following example shows how to use  the <b>WSARecv</b> function in overlapped I/O mode.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;Windows.h&gt;

#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

// Need to link with Ws2_32.lib
#pragma comment(lib, "ws2_32.lib")

#pragma warning(disable: 4127)  // Conditional expression is a constant

#define DATA_BUFSIZE 4096

int __cdecl main(int argc, char **argv)
{
    WSADATA wsd;
    struct addrinfo *result = NULL, *ptr = NULL, hints;
    WSAOVERLAPPED RecvOverlapped;
    SOCKET ConnSocket = INVALID_SOCKET;
    WSABUF DataBuf;
    DWORD RecvBytes, Flags;
    char buffer[DATA_BUFSIZE];

    int err = 0;
    int rc;

    if (argc != 2) {
        wprintf(L"usage: %s server-name\n", argv[0]);
        return 1;
    }
    // Load Winsock
    rc = WSAStartup(MAKEWORD(2, 2), &amp;wsd);
    if (rc != 0) {
        wprintf(L"Unable to load Winsock: %d\n", rc);
        return 1;
    }
    // Make sure the hints struct is zeroed out
    SecureZeroMemory((PVOID) &amp; hints, sizeof (struct addrinfo));

    // Initialize the hints to retrieve the server address for IPv4
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;

    rc = getaddrinfo(argv[1], "27015", &amp;hints, &amp;result);
    if (rc != 0) {
        wprintf(L"getaddrinfo failed with error: %d\n", rc);
        return 1;
    }

    for (ptr = result; ptr != NULL; ptr = ptr-&gt;ai_next) {

        ConnSocket = socket(ptr-&gt;ai_family, ptr-&gt;ai_socktype, ptr-&gt;ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            wprintf(L"socket failed with error: %d\n", WSAGetLastError());
            freeaddrinfo(result);
            return 1;
        }

        rc = connect(ConnSocket, ptr-&gt;ai_addr, (int) ptr-&gt;ai_addrlen);
        if (rc == SOCKET_ERROR) {

            if (WSAECONNREFUSED == (err = WSAGetLastError())) {
                closesocket(ConnSocket);
                ConnSocket = INVALID_SOCKET;
                continue;
            }
            wprintf(L"connect failed with error: %d\n", err);
            freeaddrinfo(result);
            closesocket(ConnSocket);
            return 1;
        }
        break;
    }
    if (ConnSocket == INVALID_SOCKET) {
        wprintf(L"Unable to establish connection with the server!\n");
        freeaddrinfo(result);
        return 1;
    }

    wprintf(L"Client connected...\n");

    // Make sure the RecvOverlapped struct is zeroed out
    SecureZeroMemory((PVOID) &amp; RecvOverlapped, sizeof (WSAOVERLAPPED));

    // Create an event handle and setup an overlapped structure.
    RecvOverlapped.hEvent = WSACreateEvent();
    if (RecvOverlapped.hEvent == NULL) {
        wprintf(L"WSACreateEvent failed: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ConnSocket);
        return 1;
    }

    DataBuf.len = DATA_BUFSIZE;
    DataBuf.buf = buffer;

    // Call WSARecv until the peer closes the connection
    // or until an error occurs
    while (1) {

        Flags = 0;
        rc = WSARecv(ConnSocket, &amp;DataBuf, 1, &amp;RecvBytes, &amp;Flags, &amp;RecvOverlapped, NULL);
        if ((rc == SOCKET_ERROR) &amp;&amp; (WSA_IO_PENDING != (err = WSAGetLastError()))) {
            wprintf(L"WSARecv failed with error: %d\n", err);
            break;
        }

        rc = WSAWaitForMultipleEvents(1, &amp;RecvOverlapped.hEvent, TRUE, INFINITE, TRUE);
        if (rc == WSA_WAIT_FAILED) {
            wprintf(L"WSAWaitForMultipleEvents failed with error: %d\n", WSAGetLastError());
            break;
        }

        rc = WSAGetOverlappedResult(ConnSocket, &amp;RecvOverlapped, &amp;RecvBytes, FALSE, &amp;Flags);
        if (rc == FALSE) {
            wprintf(L"WSARecv operation failed with error: %d\n", WSAGetLastError());
            break;
        }

        wprintf(L"Read %d bytes\n", RecvBytes);

        WSAResetEvent(RecvOverlapped.hEvent);

        // If 0 bytes are received, the connection was closed
        if (RecvBytes == 0)
            break;
    }

    WSACloseEvent(RecvOverlapped.hEvent);
    closesocket(ConnSocket);
    freeaddrinfo(result);

    WSACleanup();

    return 0;
}

</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a>



<a href="https://msdn.microsoft.com/40cefe46-10a3-4b6a-8c89-3e16237fc685">WSACloseEvent</a>



<a href="https://msdn.microsoft.com/cff3bc31-f34c-4bb2-9004-5ec31d0a704a">WSACreateEvent</a>



<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a>



<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>



<a href="https://msdn.microsoft.com/7a978ade-6323-455b-b655-f372f4bcadc8">WSAWaitForMultipleEvents</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>
 

 

