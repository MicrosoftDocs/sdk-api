---
UID: NC:ws2spi.LPWSPCLOSESOCKET
title: LPWSPCLOSESOCKET
description: The LPWSPCloseSocket function closes a socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPCLOSESOCKET"]
ms.date: 9/12/2019
ms.keywords: LPWSPCLOSESOCKET
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
 - LPWSPCLOSESOCKET
f1_keywords:
 - LPWSPCLOSESOCKET
 - ws2spi/LPWSPCLOSESOCKET
---

## -description

The **LPWSPCloseSocket** function closes a socket.

## -parameters

### -param s [in]

Descriptor identifying a socket.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPCloseSocket** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th> Error Code </th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></b></dl>
</dl>
</td>
<td width="60%">
The network subsystem has failed. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
Blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></b></dl>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a></b></dl>
</dl>
</td>
<td width="60%">
Socket is marked as nonblocking and SO_LINGER is set to a nonzero time-out value.
</td>
</tr>
</table>

## -remarks

This function closes a socket. More precisely, it releases the socket descriptor <i>s</i>, so further references to <i>s</i> should fail with the error <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a>. If this is the last reference to an underlying socket, the associated naming information and queued data are discarded. Any blocking or asynchronous calls pending on the socket (issued by any thread in this process) are canceled without posting any notification messages. Any pending overlapped operations issued by any thread in this process are also canceled. Whatever completion action was specified for these overlapped operations is performed (for example, event, completion routine, or completion port). In this case, the pending overlapped operations fail with the error status <a href="/windows/win32/winsock/windows-sockets-error-codes-2#wsa_operation_aborted">WSA_OPERATION_ABORTED
</a>. FD_CLOSE will not be posted after **LPWSPCloseSocket** is called.

**LPWSPCloseSocket** behavior is summarized as follows:

-   If SO_DONTLINGER is enabled (the default setting), **LPWSPCloseSocket** returns immediately and connection is gracefully closed in the background.
-   If SO_LINGER is enabled with a zero time-out, **LPWSPCloseSocket** returns immediately and the connection is reset/terminated.

    or

-   If SO_LINGER is enabled with a nonzero time-out with a blocking socket, **LPWSPCloseSocket** blocks until all data is sent or the time-out expires.
-   If SO_LINGER is enabled with a nonzero time-out with a nonblocking socket, **LPWSPCloseSocket** returns immediately, thus indicating failure.

The semantics of **LPWSPCloseSocket** are affected by the socket options SO_LINGER and SO_DONTLINGER as follows.



| Option         | Interval    | Type of close | Wait for close? |
|----------------|-------------|---------------|-----------------|
| SO_DONTLINGER | Do not care | Graceful      | No              |
| SO_LINGER     | Zero        | Hard          | No              |
| SO_LINGER     | Nonzero     | Graceful      | Yes             |



 

 

If SO_LINGER is set (that is, the **l_onoff** member of the linger structure is nonzero) and the time-out interval, **l_linger**, is zero, **LPWSPCloseSocket** is not blocked even if queued data has not yet been sent or acknowledged. This is called a hard or abortive close, because the socket's virtual circuit is reset immediately, and any unsent data is lost. Any <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b> call on the remote side of the circuit will fail with <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNRESET">WSAECONNRESET</a>.

If SO_LINGER is set with a nonzero time-out interval on a blocking socket, the **LPWSPCloseSocket** call blocks on a blocking socket until the remaining data has been sent or until the time-out expires. This is called a graceful disconnect. If the time-out expires before all data has been sent, the service provider should terminate the connection before **LPWSPCloseSocket** returns.

Enabling SO_LINGER with a nonzero time-out interval on a nonblocking socket is not recommended. In this case, the call to **LPWSPCloseSocket** will fail with an error of <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a> if the close operation cannot be completed immediately. If **LPWSPCloseSocket** fails with WSAEWOULDBLOCK, the socket handle is still valid and a disconnect is not initiated.

The Winsock SPI client must call **LPWSPCloseSocket** again to close the socket, although **LPWSPCloseSocket** can continue to fail unless the Winsock SPI client does one of the following:

-   Disables SO_DONTLINGER.
-   Enables SO_LINGER with a zero time-out.
-   Calls <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspshutdown">LPWSPShutdown</a></b> to initiate closure.

If SO_DONTLINGER is set on a stream socket (that is, the **l_onoff** member of the linger structure is zero), the **LPWSPCloseSocket** call will return immediately and does not get WSAEWOULDBLOCK, whether the socket is blocking or nonblocking. However, any data queued for transmission will be sent if possible before the underlying socket is closed. This is called a graceful disconnect and is the default behavior.

Note that in this case the Winsock provider is allowed to retain any resources associated with the socket until such time as the graceful disconnect has completed or the provider terminates the connection due to an inability to complete the operation in a provider-determined amount of time. This can affect Winsock clients that expect to use all available sockets. This is the default behavior; SO_DONTLINGER is set by default.

## -see-also

[LPWSPAccept](nc-ws2spi-lpwspaccept.md)

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a>

<a href="/previous-versions/windows/hardware/network/ff566318(v=vs.85)">WSPSetSockOpt</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>