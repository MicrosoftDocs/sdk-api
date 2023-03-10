---
UID: NF:winsock2.WSASendMsg
title: WSASendMsg function (winsock2.h)
description: Sends data and optional control information from connected and unconnected sockets. Note  This function is a Microsoft-specific extension to the Windows Sockets specification. .
helpviewer_keywords: ["WSASendMsg","WSASendMsg function [Winsock]","winsock.wsasendmsg","winsock2/WSASendMsg"]
old-location: winsock\wsasendmsg.htm
tech.root: WinSock
ms.assetid: 3b2ba645-6a70-4ba2-b4a2-5bde0c7f8d08
ms.date: 12/05/2018
ms.keywords: WSASendMsg, WSASendMsg function [Winsock], winsock.wsasendmsg, winsock2/WSASendMsg
req.header: winsock2.h
req.include-header: Mswsock.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - WSASendMsg
 - winsock2/WSASendMsg
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
 - WSASendMsg
---

# WSASendMsg function


## -description

The <b>WSASendMsg</b> function sends data and optional control information from connected and unconnected sockets. <div class="alert"><b>Note</b>  This function is a Microsoft-specific extension to the Windows Sockets specification.</div>
<div> </div>

## -parameters

### -param Handle [in]

A descriptor identifying the  socket.

### -param lpMsg [in]

A <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure storing the Posix.1g <b>msghdr</b> structure.

### -param dwFlags [in]

The flags used to modify the behavior of the <b>WSASendMsg</b> function call. For more information, see Using <i>dwFlags</i> in the Remarks section.

### -param lpNumberOfBytesSent [out]

A pointer to the number, in bytes, sent by this call if the I/O operation completes immediately. 

Use <b>NULL</b> for this parameter if the <i>lpOverlapped</i> parameter is not <b>NULL</b> to avoid potentially erroneous results. This parameter can be <b>NULL</b> only  if the <i>lpOverlapped</i> parameter is not <b>NULL</b>.

### -param lpOverlapped [in]

A pointer to a 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure. Ignored for non-overlapped sockets.

### -param lpCompletionRoutine [in]

Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](./nc-winsock2-lpwsaoverlapped_completion_routine.md)

A pointer to the completion routine called when the send operation completes. Ignored for non-overlapped sockets.

## -returns

Returns zero when successful and immediate completion occurs. When zero is returned, the specified completion routine is called when the calling thread is in the alertable state.

A return value of <b>SOCKET_ERROR</b>, and subsequent call to <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> that returns WSA_IO_PENDING, indicates the overlapped operation has successfully initiated; completion is then indicated through other means, such as through events or completion ports.

Upon failure, returns <b>SOCKET_ERROR</b> and a subsequent call to <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> returns a value other than <b>WSA_IO_PENDING</b>. The following table lists error codes.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The requested address is a broadcast address, but the appropriate flag was not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
For a UDP datagram socket, this error would indicate that a previous send operation resulted in an ICMP "Port Unreachable" message. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpMsg</i>, <i>lpNumberOfBytesSent</i>, <i>lpOverlapped</i>, or <i>lpCompletionRoutine</i> parameter is not totally contained in a valid part of the user address space. This error is also returned if a <b>name</b> member of the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure pointed to by the <i>lpMsg</i> parameter was a <b>NULL</b> pointer and the <b>namelen</b> member of the <b>WSAMSG</b> structure was not set to  zero.  This error is also returned if a <b>Control.buf</b> member of the <b>WSAMSG</b> structure pointed to by the <i>lpMsg</i> parameter was a <b>NULL</b> pointer and the <b>Control.len</b> member of the <b>WSAMSG</b> structure was not set to  zero.  

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
A blocking Windows Socket 1.1 call was canceled through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.

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
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, or the socket was not created with the overlapped flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMSGSIZE</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is message oriented, and the message is larger than the maximum supported by the underlying transport.

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
For a datagram socket, this error indicates that the time to live has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The network is unreachable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
The Windows Sockets provider reports a buffer deadlock.

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
The socket operation is not supported. This error is returned if the <b>dwFlags</b> member of the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure pointed to by the <i>lpMsg</i> parameter includes any control flags invalid for <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has been shut down; it is not possible to 
call the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg">WSASendMsg</a> function on a socket after 
<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a> has been invoked with <i>how</i> set to SD_SEND or SD_BOTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The socket timed out. This error is returned if the socket had a wait timeout specified using the <b>SO_SNDTIMEO</b> socket option and the timeout was exceeded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
Overlapped sockets: There are too many outstanding overlapped I/O requests. Nonoverlapped sockets: The socket is marked as nonblocking and the send operation cannot be completed immediately.

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
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped operation was successfully initiated and completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_OPERATION_ABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The overlapped operation has been canceled  due to the closure of the socket or due to the execution of the <b>SIO_FLUSH</b> command in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>.

</td>
</tr>
</table>

## -remarks

 The <b>WSASendMsg</b> function can be used in place of the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a> and <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> functions. The <b>WSASendMsg</b> function can only be used with datagrams  and raw sockets. The socket descriptor in the <i>s</i> parameter must be opened with the socket type set to <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>.

The <i>dwFlags</i> parameter can only contain a combination of the  following control flags: <b>MSG_DONTROUTE</b>, <b>MSG_PARTIAL</b>, and <b>MSG_OOB</b>. The <b>dwFlags</b> member of the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure pointed to by the <i>lpMsg</i> parameter is ignored on input and not used on output.


<div class="alert"><b>Note</b>  The function pointer for the 
<b>WSASendMsg</b> function must be obtained at run time by making a call to the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a> function with the <b>SIO_GET_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_WSASENDMSG</b>, a globally unique identifier (GUID) whose value identifies the <b>WSASendMsg</b> extension function. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>WSASendMsg</b> function. The <b>WSAID_WSASENDMSG</b> GUID is defined in the <i>Mswsock.h</i> header file.</div>
<div> </div>


Overlapped sockets are  created with a <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a> function call that has the <b>WSA_FLAG_OVERLAPPED</b> flag set. For overlapped sockets, sending information uses overlapped I/O unless both <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b>; when <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> are <b>NULL</b>, the socket is treated as a nonoverlapped socket. A completion indication occurs with overlapped sockets; once the buffer or buffers have been consumed by the transport, a completion routine is triggered or an event object is set. If the operation does not complete immediately, the final completion status is retrieved through the completion routine or by calling the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> function.

For nonoverlapped sockets, the <i>lpOverlapped</i> and <i>lpCompletionRoutine</i> parameters  are ignored and <b>WSASendMsg</b> adopts the same blocking semantics as the <a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a> function: data is copied from the buffer or buffers into the transport's buffer. If the socket is nonblocking and stream oriented, and there is insufficient space in the transport's buffer, <b>WSASendMsg</b> returns with only part of the application's buffers having been consumed. In contrast, this buffer situation on a blocking socket results in <b>WSASendMsg</b> blocking until all of the application's buffer contents have been consumed.


If this function is completed in an overlapped manner, it is the Winsock service provider's responsibility to capture this <a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a> structure before returning from this call. This enables applications to build stack-based 
<b>WSABUF</b> arrays pointed to by the <b>lpBuffers</b> member of the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure pointed to by the <i>lpMsg</i> parameter.

For message-oriented sockets, care must be taken not to exceed the maximum message size of the underlying provider, which can be obtained by getting the value of socket option <b>SO_MAX_MSG_SIZE</b>. If the data is too long to pass atomically through the underlying protocol, the error <b>WSAEMSGSIZE</b> is returned and no data is transmitted.


On an IPv4 socket of type  <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>, an application can specific  the local IP source address to use for sending with the <b>WSASendMsg</b> function. One of the control data objects passed in the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure to the <b>WSASendMsg</b> function may contain an 
<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-in_pktinfo">in_pktinfo</a> structure used to specify the local IPv4 source address to use for sending.

On an IPv6 socket of type  <b>SOCK_DGRAM</b> or <b>SOCK_RAW</b>, an application can specific  the local IP source address to use for sending with the <b>WSASendMsg</b> function. One of the control data objects passed in the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure to the <b>WSASendMsg</b> function may contain an 
<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-in6_pktinfo">in6_pktinfo</a> structure used to specify the local IPv6 source address to use for sending.

For a dual-stack socket when sending datagrams  with the <b>WSASendMsg</b> function and an application wants to specify a specific local IP source address to be used, the method to handle this depends on the destination IP address. When sending to an IPv4 destination address or an IPv4-mapped IPv6 destination address, one of the control data objects passed in the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure pointed to by the <i>lpMsg</i> parameter should contain an 
<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-in_pktinfo">in_pktinfo</a> structure containing the local IPv4 source address to use for sending. When sending to an IPv6 destination address that is not a an IPv4-mapped IPv6 address, one of the control data objects passed in the <b>WSAMSG</b> structure pointed to by the <i>lpMsg</i> parameter should contain an 
<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-in6_pktinfo">in6_pktinfo</a> structure containing the local IPv6 source address to use for sending. 

<div class="alert"><b>Note</b>  The <b>SO_SNDTIMEO</b> socket option applies only to blocking sockets.</div>
<div> </div>
<div class="alert"><b>Note</b>  The successful completion of a 
<b>WSASendMsg</b> does not indicate that the data was successfully delivered.</div>
<div> </div>
<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSASendMsg</b> with the <i>lpOverlapped</i> parameter set to NULL, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="dwFlags"></a><a id="dwflags"></a><a id="DWFLAGS"></a>dwFlags</h3>
The <i>dwFlags</i> input parameter can be used to influence the behavior of the function invocation beyond the options specified for the associated socket. That is, the semantics of this function are determined by the socket options and the <i>dwFlags</i> parameter. The latter is constructed by using the bitwise OR operator with any of the following values.<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>MSG_DONTROUTE</b></td>
<td>Specifies that the data should not be subject to routing. A Windows Sockets service provider can choose to ignore this flag.</td>
</tr>
<tr>
<td><b>MSG_PARTIAL</b></td>
<td>Specifies that <i>lpMsg-&gt;lpBuffers</i> contains only a partial message. Note that the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a> will be returned by transports that do not support partial message transmissions.</td>
</tr>
</table>
 </p>The possible values for <i>dwFlags</i> parameter are defined in the <i>Winsock2.h</i> header file.

On output, the <b>dwFlags</b> member of the <a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a> structure pointed to by the <i>lpMsg</i> parameter is not used. 

<h3><a id="Overlapped_Socket_I_O"></a><a id="overlapped_socket_i_o"></a><a id="OVERLAPPED_SOCKET_I_O"></a>Overlapped Socket I/O</h3>
If an overlapped operation completes immediately, 
<b>WSASendMsg</b> returns a value of zero and the <i>lpNumberOfBytesSent</i> parameter is updated with the number of bytes sent. If the overlapped operation is successfully initiated and will complete later, 
<b>WSASendMsg</b> returns SOCKET_ERROR and indicates error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_IO_PENDING</a>. In this case, <i>lpNumberOfBytesSent</i> is not updated. When the overlapped operation completes, the amount of data transferred is indicated either through the <i>cbTransferred</i> parameter in the completion routine (if specified) or through the <i>lpcbTransfer</i> parameter in 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>.


<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> for more information.</div>
<div> </div>


The 
<b>WSASendMsg</b> function using overlapped I/O can be called from within the completion routine of a previous 
, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, <a href="/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg">LPFN_WSARECVMSG (WSARecvMsg)</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>, <b>WSASendMsg</b>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a> function. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The <i>lpOverlapped</i> parameter must be valid for the duration of the overlapped operation. If multiple I/O operations are simultaneously outstanding, each must reference a separate 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.

If the <i>lpCompletionRoutine</i> parameter is <b>NULL</b>, the <i>hEvent</i> parameter of <i>lpOverlapped</i> is signaled when the overlapped operation completes if it contains a valid event object handle. An application can use 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> to wait or poll on the event object.

If <i>lpCompletionRoutine</i> is not <b>NULL</b>, the <i>hEvent</i> parameter is ignored and can be used by the application to pass context information to the completion routine. A caller that passes a non-<b>NULL</b> <i>lpCompletionRoutine</i> and later calls 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a> for the same overlapped I/O request may not set the <i>fWait</i> parameter for that invocation of 
<b>WSAGetOverlappedResult</b> to <b>TRUE</b>. In this case, the usage of the <i>hEvent</i> parameter is undefined, and attempting to wait on the <i>hEvent</i> parameter would produce unpredictable results.

The completion routine follows the same rules as stipulated for Windows file I/O completion routines. The completion routine will not be invoked until the thread is in an alertable wait state, for example, with <a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a> called with the <i>fAlertable</i> parameter set to <b>TRUE</b>.

The transport providers allow an application to invoke send and receive operations from within the context of the socket I/O completion routine, and guarantee that, for a given socket, I/O completion routines will not be nested. This permits time-sensitive data transmissions to occur entirely within a preemptive context.

The prototype of the completion routine is as follows.


```cpp

void CALLBACK CompletionRoutine(
  IN DWORD dwError,
  IN DWORD cbTransferred,
  IN LPWSAOVERLAPPED lpOverlapped,
  IN DWORD dwFlags
);

```


The <b>CompletionRoutine</b> function is a placeholder for an application-defined or library-defined function name. The <i>dwError</i> parameter specifies the completion status for the overlapped operation as indicated by the <i>lpOverlapped</i> parameter. The <i>cbTransferred</i> parameter indicates the number of bytes sent. Currently there are no flag values defined and the <i>dwFlags</i> parameter will be zero. The <b>CompletionRoutine</b> function does not return a value.

Returning from this function allows invocation of another pending completion routine for the socket. All waiting completion routines are called before the alertable thread's wait is satisfied with a return code of WSA_IO_COMPLETION. The completion routines can be called in any order, not necessarily in the same order the overlapped operations are completed. However, the posted buffers are guaranteed to be sent in the same order they are specified.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/WinSock/ipv6-pktinfo">IPV6_PKTINFO</a>



<a href="/windows/desktop/WinSock/ip-pktinfo">IP_PKTINFO</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-wsabuf">WSABUF</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult">WSAGetOverlappedResult</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-wsamsg">WSAMSG</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasend">WSASend</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendTo</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsawaitformultipleevents">WSAWaitForMultipleEvents</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-in6_pktinfo">in6_pktinfo</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-in_pktinfo">in_pktinfo</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>



<a href="/windows/desktop/api/winsock/nf-winsock-shutdown">shutdown</a>