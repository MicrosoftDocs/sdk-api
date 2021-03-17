---
UID: NC:ws2spi.LPWSPSEND
title: LPWSPSEND
description: The LPWSPSend function sends data on a connected socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPSEND"]
ms.date: 9/12/2019
ms.keywords: LPWSPSEND
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
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - LPWSPSEND
f1_keywords:
 - LPWSPSEND
 - ws2spi/LPWSPSEND
---

## -description

The **LPWSPSend** function sends data on a connected socket.

## -parameters

### -param s [in]

A descriptor identifying a connected socket.

### -param lpBuffers [in]

A pointer to an array of <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures. Each **WSABUF** structure contains a pointer to a buffer and the length of the buffer, in bytes. For a Winsock application, once the **LPWSPSend** function is called, the system owns these buffers and the application may not access them. Data buffers referenced in each WSABUF structure are owned by the system and your application may not access them for the lifetime of the call.

### -param dwBufferCount [in]

The number of <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures in the <i>lpBuffers</i> array.

### -param lpNumberOfBytesSent [out]

A pointer to the number of bytes sent by this call.

### -param dwFlags [in]

A set of flags that specifies the way in which the call is made.

### -param lpOverlapped [in]

A pointer to a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure (ignored for nonoverlapped sockets).

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](../winsock2/nc-winsock2-lpwsaoverlapped_completion_routine.md)

A pointer to the completion routine called when the send operation has been completed (ignored for nonoverlapped sockets).

### -param lpThreadId [in]

A pointer to a <b><a href="/windows/win32/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a></b> structure to be used by the provider in a subsequent call to <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>. The provider should store the referenced **WSATHREADID** structure (not the pointer to same) until after the **WPUQueueApc** function returns.

### -param lpErrno [out]

A pointer to the error code.

## -returns

If no error occurs and the send operation has completed immediately, **LPWSPSend** returns zero. Note that in this case the completion routine, if specified, will have already been queued. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>. The error code [WSA_IO_PENDING](/windows/win32/winsock/windows-sockets-error-codes-2#wsa-io-pending) indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that no overlapped operation was initiated and no completion indication will occur.

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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEACCES">WSAEACCES</a></dt>
</dl>
</td>
<td width="60%">
Requested address is a broadcast address, but the appropriate flag was not set.  
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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETRESET">WSAENETRESET</a></dt>
</dl>
</td>
<td width="60%">
The connection has been broken due to the remote host resetting. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></dt>
</dl>
</td>
<td width="60%">
The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.
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
MSG_OOB was specified, but the socket is not stream-style such as type SOCK_STREAM, OOB data is not supported in the communication domain associated with this socket, MSG_PARTIAL is not supported, or the socket is unidirectional and supports only receive operations.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAESHUTDOWN">WSAESHUTDOWN</a></dt>
</dl>
</td>
<td width="60%">
Socket has been shut down; it is not possible to <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b> on a socket after <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a></b> has been invoked with how set to SD_SEND or SD_BOTH.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a></dt>
</dl>
</td>
<td width="60%">
**Windows NT:** Overlapped sockets: There are too many outstanding overlapped I/O requests.Nonoverlapped sockets: The socket is marked as nonblocking and the send operation cannot be completed immediately.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMSGSIZE">WSAEMSGSIZE</a></dt>
</dl>
</td>
<td width="60%">
Socket is message oriented, and the message is larger than the maximum supported by the underlying transport.
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
Socket has not been bound with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>, or the socket is not created with the overlapped flag.
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNABORTED">WSAECONNABORTED</a></dt>
</dl>
</td>
<td width="60%">
Virtual circuit was terminated due to a time-out or other failure.
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNRESET">WSAECONNRESET</a></dt>
</dl>
</td>
<td width="60%">
Virtual circuit was reset by the remote side.
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSA_OPERATION_ABORTED">WSA_OPERATION_ABORTED</a></dt>
</dl>
</td>
<td width="60%">
Overlapped operation has been canceled due to the closure of the socket, or the execution of the SIO_FLUSH command in <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b>.
</tr>
</table>

## -remarks

The **LPWSPSend** function is used to write outgoing data from one or more buffers on a connection-oriented socket specified by <i>s</i>. It can also be used, however, on connectionless sockets that have a stipulated default peer address established through the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> function.

For overlapped sockets (created using <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a> with flag WSA_FLAG_OVERLAPPED) this will occur using overlapped I/O, unless both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are null in which case the socket is treated as a nonoverlapped socket. A completion indication will occur (invocation of the completion routine or setting of an event object) when the supplied buffer(s) have been consumed by the transport. If the operation does not complete immediately, the final completion status is retrieved through the completion routine or <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a>.

For nonoverlapped sockets, the parameters <i>lpOverlapped</i>, <i>lpCompletionRoutine</i>, and <i>lpThreadId</i> are ignored and **LPWSPSend** adopts the regular synchronous semantics. Data is copied from the supplied buffer(s) into the transport's buffer. If the socket is nonblocking and stream oriented, and there is not sufficient space in the transport's buffer, **LPWSPSend** will return with only part of the supplied buffers having been consumed. Given the same buffer situation and a blocking socket, **LPWSPSend** will block until all of the supplied buffer contents have been consumed.

The array of <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structures pointed to by the <i>lpBuffers</i> parameter is transient. If this operation completes in an overlapped manner, it is the service provider's responsibility to capture these **WSABUF** structures before returning from this call. This enables applications to build stack-based **WSABUF** arrays.

For message-oriented sockets, care must be taken not to exceed the maximum message size of the underlying provider, which can be obtained by getting the value of socket option SO_MAX_MSG_SIZE. If the data is too long to pass atomically through the underlying protocol the error <b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMSGSIZE">WSAEMSGSIZE</a></b> is returned, and no data is transmitted.

Note that the successful completion of a **LPWSPSend** does not indicate that the data was successfully delivered.

<i>dwFlags</i> can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. That is, the semantics of this function are determined by the socket options and the <i>dwFlags</i> parameter. The latter is constructed by using the bitwise OR operator with any of the following values.



| Value          | Meaning                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MSG_DONTROUTE | Specifies that the data should not be subject to routing. A Windows Sockets service provider can choose to ignore this flag;.                                                                                                          |
| MSG_OOB       | Sends OOB data (stream-style socket such as SOCK_STREAM only).                                                                                                                                                                        |
| MSG_PARTIAL   | Specifies that <i>lpBuffers</i> only contains a partial message. Note that the error code [WSAEOPNOTSUPP](/windows/win32/winsock/windows-sockets-error-codes-2#wsaeopnotsupp) will be returned for messages that do not support partial message transmissions. |



 

 

If an overlapped operation completes immediately, **LPWSPSend** returns a value of zero and the <i>lpNumberOfBytesSent</i> parameter is updated with the number of bytes sent. If the overlapped operation is successfully initiated and will complete later, **LPWSPSend** returns SOCKET_ERROR and indicates error code [WSA_IO_PENDING](/windows/win32/winsock/windows-sockets-error-codes-2#wsa-io-pending). In this case, <i>lpNumberOfBytesSent</i> is not updated. When the overlapped operation completes the amount of data transferred is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified), or through the <i>lpcbTransfer</i> parameter in <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a>.

Providers must allow this function to be called from within the completion routine of a previous <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b>, **LPWSPSend** or <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b> function. However, for a given socket, I/O completion routines cannot be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. If multiple I/O operations are simultaneously outstanding, each must reference a separate overlapped structure. The <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaoverlapped">WSAOverlapped</a></b> structure is defined in its own reference page.

If the <i>lpCompletionRoutine</i> parameter is null, the service provider signals the **hEvent** member of <i>lpOverlapped</i> when the overlapped operation completes if it contains a valid event object handle. The Windows Sockets SPI client can use <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a> to wait or poll on the event object.

If <i>lpCompletionRoutine</i> is not null, the **hEvent** member is ignored and can be used by the Windows Sockets SPI client to pass context information to the completion routine. A client that passes a non-null <i>lpCompletionRoutine</i> and later calls **WSAGetOverlappedResult** for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of **WSAGetOverlappedResult** to **TRUE**. In this case the usage of the **hEvent** member is undefined, and attempting to wait on the **hEvent** member would produce unpredictable results.

A service provider arranges for a function to be executed in the proper thread and process context by calling <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>. This function can be called from any process and thread context, even a context different from the thread and process that was used to initiate the overlapped operation.

A service provider arranges for a function to be executed in the proper thread by calling <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>. Note that this function must be invoked while in the context of the same process (but not necessarily the same thread) that was used to initiate the overlapped operation. It is the service provider's responsibility to arrange for this process context to be active prior to calling **WPUQueueApc**.

The <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b> function takes as input parameters a pointer to a <b><a href="/windows/win32/api/ws2spi/ns-ws2spi-wsathreadid">WSATHREADID</a></b> structure (supplied to the provider through the <i>lpThreadId</i> input parameter), a pointer to an APC function to be invoked, and a context value that is subsequently passed to the APC function. Because only a single context value is available, the APC function itself cannot be the client specified–completion routine. The service provider must instead supply a pointer to its own APC function that uses the supplied context value to access the needed result information for the overlapped operation, and then invokes the client specified–completion routine.

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

The CompletionRoutine is a placeholder for a client supplied function name. <i>dwError</i> specifies the completion status for the overlapped operation as indicated by <i>lpOverlapped</i>. <i>cbTransferred</i> specifies the number of bytes sent. No flag values are currently defined and the <i>dwFlags</i> value will be zero. This function does not return a value.

The completion routines can be called in any order, though not necessarily in the same order that the overlapped operations are completed. However, the service provider guarantees to the client that posted buffers are sent in the same order they are supplied.

> [!Note]  
> All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the operations complete. See <b><a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a></b> for more information.

## -see-also

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetoverlappedresult">LPWSPGetOverlappedResult</a>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>