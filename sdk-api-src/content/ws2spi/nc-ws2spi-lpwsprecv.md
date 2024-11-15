---
UID: NC:ws2spi.LPWSPRECV
title: LPWSPRECV
description: The LPWSPRecv function receives data on a socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPRECV"]
ms.date: 9/12/2019
ms.keywords: LPWSPRECV
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - ws2spi.h
api_name:
 - LPWSPRECV
f1_keywords:
 - LPWSPRECV
 - ws2spi/LPWSPRECV
---

## -description

The **LPWSPRecv** function receives data on a socket.

## -parameters

### -param s [in]

A descriptor identifying a connected socket.

### -param lpBuffers \[in\, out\]

A pointer to an array of <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures. Each **WSABUF** structure contains a pointer to a buffer and the length of the buffer, in bytes.

### -param dwBufferCount [in]

The number of <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures in the <i>lpBuffers</i> array.

### -param lpNumberOfBytesRecvd [out]

A pointer to the number of bytes received by this call.

### -param lpFlags \[in\, out\]

A pointer to flags that specify the way in which the call is made.

### -param lpOverlapped [in]

A pointer to a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure (ignored for nonoverlapped structures).

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](../winsock2/nc-winsock2-lpwsaoverlapped_completion_routine.md)

A pointer to the completion routine called when the receive operation has been completed (ignored for nonoverlapped structures).

### -param lpThreadId [in]

A pointer to a <b><a href="/windows/win32/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a></b> structure to be used by the provider in a subsequent call to <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>. The provider should store the referenced **WSATHREADID** structure (not the pointer to same) until after the **WPUQueueApc** function returns.

### -param lpErrno [out]

A pointer to the error code.

## -returns

If no error occurs and the receive operation has completed immediately, **LPWSPRecv** returns zero. Note that in this case the completion routine, if specified, will have already been queued. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>. The error code WSA_IO_PENDING indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that no overlapped operations was initiated and no completion indication will occur.

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a></dt>
</dl>
</td>
<td width="60%">
Socket is not connected.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINTR">WSAEINTR</a></dt>
</dl>
</td>
<td width="60%">
(Blocking) call was canceled through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">LPWSPCancelBlockingCall</a></b>.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></dt>
</dl>
</td>
<td width="60%">
Blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETRESET">WSAENETRESET</a></dt>
</dl>
</td>
<td width="60%">
The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffers</i> parameter is not totally contained in a valid part of the user address space.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></dt>
</dl>
</td>
<td width="60%">
MSG_OOB was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, or the socket is unidirectional and supports only send operations.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAESHUTDOWN">WSAESHUTDOWN</a></dt>
</dl>
</td>
<td width="60%">
Socket has been shut down; it is not possible to receive through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b> on a socket after <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a></b> has been invoked with <i>how</i> set to SD_RECEIVE or SD_BOTH.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a></dt>
</dl>
</td>
<td width="60%">
Windows NT: 
Overlapped sockets: there are too many outstanding overlapped I/O requests. Nonoverlapped sockets: The socket is marked as nonblocking and the receive operation cannot be completed immediately.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMSGSIZE">WSAEMSGSIZE</a></dt>
</dl>
</td>
<td width="60%">
Message was too large to fit into the specified buffer and (for unreliable protocols only) any trailing portion of the message that did not fit into the buffer has been discarded.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
Socket has not been bound (for example, with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>) or the socket is not created with the overlapped flag.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNABORTED">WSAECONNABORTED</a></dt>
</dl>
</td>
<td width="60%">
Virtual circuit was terminated due to a time-out or other failure.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNRESET">WSAECONNRESET</a></dt>
</dl>
</td>
<td width="60%">
Virtual circuit was reset by the remote side.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEDISCON">WSAEDISCON</a></dt>
</dl>
</td>
<td width="60%">
Socket <i>s</i> is message oriented and the virtual circuit was gracefully closed by the remote side.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSA_IO_PENDING">WSA_IO_PENDING</a></dt>
</dl>
</td>
<td width="60%">
An overlapped operation was successfully initiated and completion will be indicated at a later time.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSA_OPERATION_ABORTED">WSA_OPERATION_ABORTED</a></dt>
</dl>
</td>
<td width="60%">
Overlapped operation has been canceled due to the closure of the socket.
</td>
</tr>
</table>

## -remarks

**LPWSPRecv** is used on connected sockets or bound connectionless sockets specified by the <i>s</i> parameter and is used to read incoming data. The socket's local address must be known. This may be done explicitly through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b> or implicitly through **[LPWSPAccept](nc-ws2spi-lpwspaccept.md)**, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b>, or <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspjoinleaf">LPWSPJoinLeaf</a></b>.

For connected, connectionless sockets, this function restricts the addresses from which received messages are accepted. The function only returns messages from the remote address specified in the connection. Messages from other addresses are (silently) discarded.

For overlapped sockets **LPWSPRecv** is used to post one or more buffers into which incoming data will be placed as it becomes available, after which the Windows Sockets SPI client-specified completion indication (invocation of the completion routine or setting of an event object) occurs. If the operation does not complete immediately, the final completion status is retrieved through the completion routine or <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a>.

If both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are null, the socket in this function will be treated as a nonoverlapped socket.

For nonoverlapped sockets, the <i>lpOverlapped</i>, <i>lpCompletionRoutine</i>, and <i>lpThreadId</i> parameters are ignored. Any data that has already been received and buffered by the transport will be copied into the supplied user buffers. For the case of a blocking socket with no data currently having been received and buffered by the transport, the call will block until data is received. Windows Sockets 2 does not define any standard blocking timeout mechanism for this function. For protocols acting as byte-stream protocols the stack tries to return as much data as possible subject to the supplied buffer space and amount of received data available. However, receipt of a single byte is sufficient to unblock the caller. There is no guarantee that more than a single byte will be returned. For protocols acting as message-oriented, a full message is required to unblock the caller.

Whether or not a protocol is acting as byte-stream is determined by the setting of XP1_MESSAGE_ORIENTED and XP1_PSEUDO_STREAM in its <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure and the setting of the MSG_PARTIAL flag passed in to this function (for protocols that support it). The relevant combinations are summarized in the following table (an asterisk (\*) indicates that the setting of this bit does not matter in this case).

| XP1_MESSAGE_ORIENTED | XP1_PSEUDO_STREAM | MSG_PARTIAL | Acts as          |
|------------------------|---------------------|--------------|------------------|
| not set                | \*                  | \*           | byte stream      |
| \*                     | set                 | \*           | byte stream      |
| set                    | not set             | set          | byte stream      |
| set                    | not set             | not set      | message oriented |

The supplied buffers are filled in the order in which they appear in the array pointed to by <i>lpBuffers</i>, and the buffers are packed so that no holes are created.

The array of <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures pointed to by the <i>lpBuffers</i> parameter is transient. If this operation completes in an overlapped manner, it is the service provider's responsibility to capture this array of pointers to **WSABUF** structures before returning from this call. This enables Windows Sockets SPI clients to build stack-based **WSABUF** arrays.

For byte stream-style sockets (for example, type SOCK_STREAM), incoming data is placed into the buffers until the buffers are filled, the connection is closed, or internally buffered data is exhausted. Regardless of whether or not the incoming data fills all the buffers, the completion indication occurs for overlapped sockets. For message-oriented sockets (for example, type SOCK_DGRAM), an incoming message is placed into the supplied buffers, up to the total size of the buffers supplied, and the completion indication occurs for overlapped sockets. If the message is larger than the buffers supplied, the buffers are filled with the first part of the message. If the MSG_PARTIAL feature is supported by the service provider, the MSG_PARTIAL flag is set in <i>lpFlags</i> and subsequent receive operation(s) can be used to retrieve the rest of the message. If MSG_PARTIAL is not supported but the protocol is reliable, **LPWSPRecv** generates the error <b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMSGSIZE">WSAEMSGSIZE</a></b> and a subsequent receive operation with a larger buffer can be used to retrieve the entire message. Otherwise, (that is, the protocol is unreliable and does not support MSG_PARTIAL), the excess data is lost, and **LPWSPRecv** generates the error WSAEMSGSIZE.

For connection-oriented sockets, **LPWSPRecv** can indicate the graceful termination of the virtual circuit in one of two ways, depending on whether the socket is a byte stream or message oriented. For byte streams, zero bytes having been read indicates graceful closure and that no more bytes will ever be read. For message-oriented sockets, where a zero byte message is often allowable, a return error code of <b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEDISCON">WSAEDISCON</a></b> is used to indicate graceful closure. In any case a return error code of <b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNRESET">WSAECONNRESET</a></b> indicates an abortive close has occurred.

The <i>lpFlags</i> parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. That is, the semantics of this function are determined by the socket options and the <i>lpFlags</i> parameter. The latter is constructed by using the bitwise OR operator with any of the following values.

| Value        | Meaning                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MSG_PEEK    | Peeks at the incoming data. The data is copied into the buffer but is not removed from the input queue. This flag is valid only for nonoverlapped sockets.                                                                                                                                                                                                                                                                                                                                                             |
| MSG_OOB     | Processes Out Of Band (OOB) data.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| MSG_PARTIAL | This flag is for message-oriented sockets only. On output, indicates that the data supplied is a portion of the message transmitted by the sender. Remaining portions of the message will be supplied in subsequent receive operations. A subsequent receive operation with MSG_PARTIAL flag cleared indicates end of sender's message. As an input parameter, MSG_PARTIAL indicates that the receive operation should complete even if only part of a message has been received by the service provider.<br/> |

If an overlapped operation completes immediately, **LPWSPRecv** returns a value of zero and the <i>lpNumberOfBytesRecvd</i> parameter is updated with the number of bytes received and the flag bits pointed by the <i>lpFlags</i> parameter are also updated. If the overlapped operation is successfully initiated and will complete later, **LPWSPRecv** returns SOCKET_ERROR and indicates error code [WSA_IO_PENDING](/windows/win32/winsock/windows-sockets-error-codes-2#wsa-io-pending). In this case, <i>lpNumberOfBytesRecvd</i> and <i>lpFlags</i> are not updated. When the overlapped operation completes the amount of data transferred is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a>. Flag values are obtained either through the <i>dwFlags</i> parameter of the completion routine, or by examining the <i>lpdwFlags</i> parameter of <b><a href="/windows/win32/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a></b>.

Providers must allow this function to be called from within the completion routine of a previous **LPWSPRecv**, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b> or <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b> function. However, for a given socket, I/O completion routines cannot be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. If multiple I/O operations are simultaneously outstanding, each must reference a separate overlapped structure. The <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure is defined in its own reference page.

If the <i>lpCompletionRoutine</i> parameter is null, the service provider signals the **hEvent** member of <i>lpOverlapped</i> when the overlapped operation completes if it contains a valid event object handle. The Windows Sockets SPI client can use <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a> to wait or poll on the event object.

If <i>lpCompletionRoutine</i> is not null, the **hEvent** member is ignored and can be used by the Windows Sockets SPI client to pass context information to the completion routine. A client that passes a null <i>lpCompletionRoutine</i> and later calls <b><a href="/windows/win32/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a></b> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of **WSAGetOverlappedResult** to **TRUE**. In this case the usage of the **hEvent** member is undefined, and attempting to wait on the **hEvent** member would produce unpredictable results.

It is the service provider's responsibility to arrange for invocation of the client specified–completion routine when the overlapped operation completes. Since the completion routine must be executed in the context of the same thread that initiated the overlapped operation, it cannot be invoked directly from the service provider. The Ws2_32.dll offers an asynchronous procedure call (APC) mechanism to facilitate invocation of completion routines.

A service provider arranges for a function to be executed in the proper thread and process context by calling <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>, which was used to initiate the overlapped operation. This function can be called from any process and thread context, even a context different from the thread and process that was used to initiate the overlapped operation.

<b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b> takes as input parameters a pointer to a <b><a href="/windows/win32/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a></b> structure (supplied to the provider through the <i>lpThreadId</i> input parameter), a pointer to an APC function to be invoked, and a context value that is subsequently passed to the APC function. Because only a single context value is available, the APC function itself cannot be the client specified–completion routine. The service provider must instead supply a pointer to its own APC function that uses the supplied context value to access the needed result information for the overlapped operation, and then invokes the client specified–completion routine.

The prototype for the client-supplied completion routine is as follows.

```cpp
void CALLBACK 
CompletionRoutine(  
  IN DWORD           dwError, 
  IN DWORD           cbTransferred, 
  IN LPWSAOVERLAPPED lpOverlapped, 
  IN DWORD           dwFlags 
);
```

The <i>CompletionRoutine</i> parameter is a placeholder for a client-supplied function name. <i>dwError</i> specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. The <i>cbTransferred</i> parameter specifies the number of bytes received. <i>dwFlags</i> contains information that would have appeared in <i>lpFlags</i> if the receive operation had completed immediately. This function does not return a value.

The completion routines can be called in any order, but not necessarily the same order in which the overlapped operations are completed. However, the posted buffers are guaranteed to be filled in the same order in which they are supplied.

> [!Note]  
> All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the operations complete. See <b><a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a></b> for more information.

## -see-also

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucloseevent">WPUCloseEvent</a>

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreateevent">WPUCreateEvent</a>

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>
