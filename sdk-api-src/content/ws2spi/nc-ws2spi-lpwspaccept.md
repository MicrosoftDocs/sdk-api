---
UID: NC:ws2spi.LPWSPACCEPT
title: LPWSPACCEPT
description: The LPWSPAccept function conditionally accepts a connection based on the return value of a condition function.
tech.root: winsock
helpviewer_keywords: ["LPWSPACCEPT","WSPACCEPT"]
ms.date: 9/9/2019
ms.keywords: LPWSPACCEPT, WSPACCEPT
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
req.target-type: Windows
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
 - LPWSPACCEPT
f1_keywords:
 - LPWSPACCEPT
 - ws2spi/LPWSPACCEPT
---

## -description

The **LPWSPAccept** function conditionally accepts a connection based on the return value of a condition function.

## -parameters

### -param s [in]

Descriptor identifying a socket that is listening for connections after a <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a>.

### -param addr [out]

Optional pointer to a buffer that receives the address of the connecting entity, as known to the service provider. The exact format of the <i>addr</i> parameter is determined by the address family established when the socket in the <a href="/windows/win32/winsock/sockaddr-2">sockaddr</a> structure was created.

### -param addrlen [in, out]

Optional pointer to an integer that contains the length of the <i>addr</i> parameter, in bytes.

### -param lpfnCondition [in]

Procedure instance address of an optional-condition function furnished by Windows Sockets. This function is used in the accept or reject decision based on the caller information passed in as parameters.

### -param dwCallbackData [in]

Callback data to be passed back to the Windows Socket 2 client as the value of the <i>dwCallbackData</i> parameter of the condition function. This parameter is not interpreted by the service provider.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPAccept** returns a value of type SOCKET that is a descriptor for the accepted socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th> Error Code </th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNREFUSED">WSAECONNREFUSED</a></b></dl>
</dl>
</td>
<td width="60%">
The connection request was forcefully rejected as indicated in the return value of the condition function (CF_REJECT).  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNRESET">WSAECONNRESET</a></b></dl>
</dl>
</td>
<td width="60%">
An incoming connection was indicated, but was subsequently terminated by the remote peer prior to accepting the call. 
</td>
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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>addrlen</i> parameter is too small or the <i>lpfnCondition</i> parameter is not part of the user address space.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINTR">WSAEINTR</a></b></dl>
</dl>
</td>
<td width="60%">
A (blocking) call was canceled through <a href="/windows/win32/api/winsock2/nf-winsock2-wsacancelblockingcall">LPWSPCancelBlockingCall</a>.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets call is in progress.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a> was not invoked prior to LPWSPAccept, parameter <i>g</i> specified in the condition function is not a valid value, the return value of the condition function is not a valid one, or any case where the specified socket is in an invalid state.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMFILE">WSAEMFILE</a></b></dl>
</dl>
</td>
<td width="60%">
Queue is nonempty upon entry to LPWSPAccept and there are no socket descriptors available.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
No buffer space is available.
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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></b></dl>
</dl>
</td>
<td width="60%">
Referenced socket is not a type that supports connection-oriented service.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSATRY_AGAIN">WSATRY_AGAIN</a></b></dl>
</dl>
</td>
<td width="60%">
Acceptance of the connection request was deferred as indicated in the return value of the condition function (CF_DEFER).
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a></b></dl>
</dl>
</td>
<td width="60%">
Socket is marked as nonblocking and no connections are present to be accepted.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEACCES">WSAEACCES</a></b></dl>
</dl>
</td>
<td width="60%">
The connection request that was offered has timed out or been withdrawn.
</td>
</tr>
</table>

## -remarks

The **LPWSPAccept** function extracts the first connection on the queue of pending connections on socket <i>s</i>, and checks it against the condition function, provided the condition function is specified (that is, not null). The condition function must be executed in the same thread as this routine. If the condition function returns CF_ACCEPT, **LPWSPAccept** creates a new socket.

Newly created sockets have the same properties as the socket <i>s</i>, including network events registered with <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspasyncselect">**LPWSPAsyncSelect**</a> or with <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">**LPWSPEventSelect**</a>. As described in <a href="/windows/win32/winsock/descriptor-allocation-2">**DescriptorAllocation**</a>, when new socket descriptors are allocated, IFS providers must call <a href="/windows/win32/api/ws2spi/nf-ws2spi-wpumodifyifshandle">**WPUModifyIFSHandle**</a> and non-IFS providers must call <a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">**WPUCreateSocketHandle**</a>.

If the condition function returns CF_REJECT, **LPWSPAccept** rejects the connection request. If the application's accept/reject decision cannot be made immediately, the condition function will return CF_DEFER to indicate that no decision has been made. No action about this connection request is to be taken by the service provider. When the application is ready to take action on the connection request, it will invoke **LPWSPAccept** again and return either CF_ACCEPT or CF_REJECT as a return value from the condition function.

For sockets that are in the (default) blocking mode, if no pending connections are present on the queue, **LPWSPAccept** blocks the caller until a connection is present. For sockets in nonblocking mode, if this function is called when no pending connections are present on the queue, **LPWSPAccept** returns the error code <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a>. The accepted socket cannot be used to accept more connections. The original socket remains open.

The parameter <i>addr</i> is a result parameter that is filled with the address of the connecting entity, as known to the service provider. The exact format of the <i>addr</i> parameter is determined by the address family in which the communication is occurring. The <i>addrlen</i> is a value-result parameter; it will initially contain the amount of space pointed to by <i>addr</i>. On return, it must contain the actual length (in bytes) of the address returned by the service provider. This call is used with connection-oriented socket types such as SOCK_STREAM. If <i>addr</i> and/or <i>addrlen</i> are equal to null, then no information about the remote address of the accepted socket is returned. Otherwise, these two parameters shall be filled in regardless of whether the condition function is specified or what it returns.

The prototype of the condition function is as follows.

```cpp
int CALLBACK 
ConditionFunc( 
  IN     LPWSABUF    lpCallerId, 
  IN     LPWSABUF    lpCallerData, 
  IN OUT LPQOS       lpSQOS, 
  IN OUT LPQOS       lpGQOS,
  IN     LPWSABUF    lpCalleeId, 
  IN     LPWSABUF    lpCalleeData, 
  OUT    GROUP FAR * g, 	
  IN     DWORD_PTR   dwCallbackData
);
```

The <i>lpCallerId</i> and <i>lpCallerData</i> are value parameters that must contain the address of the connecting entity and any user data that was sent along with the connection request. If no caller identifier or caller data is available, the corresponding parameter will be null. Many network protocols do not support connect-time caller data. Most conventional network protocols can be expected to support caller identifier information at connection-request time. The **buf** part of the <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">**WSABUF**</a> pointed to by <i>lpCallerId</i> points to a <a href="/windows/win32/winsock/sockaddr-2">**sockaddr**</a>. The **sockaddr** is interpreted according to its address family (typically by casting the **sockaddr** to some type specific to the address family).

The <i>lpSQOS</i> parameter references the flow specifications for socket <i>s</i> specified by the caller, one for each direction, followed by any additional provider-specific parameters. The sending or receiving flow specification values will be ignored as appropriate for any unidirectional sockets. A null value for <i>lpSQOS</i> indicates that there is no caller-supplied QoS and that no negotiation is possible. A non-**NULL** <i>lpSQOS</i> pointer indicates that a QoS negotiation is to occur or that the provider is prepared to accept the QoS request without negotiation.

The <i>lpCalleeId</i> is a value parameter that contains the local address of the connected entity. The **buf** part of the <a href="/windows/win32/api/ws2def/ns-ws2def-wsabuf">**WSABUF**</a> pointed to by <i>lpCalleeId</i> points to a <a href="/windows/win32/winsock/sockaddr-2">**sockaddr**</a>. The **sockaddr** is interpreted according to its address family (typically by casting the **sockaddr** to some type specific to the address family).

The <i>lpCalleeData</i> is a result parameter used by the condition function to supply user data back to the connecting entity. The storage for this data must be provided by the service provider. The <i>lpCalleeData</i>-&gt;**len** initially contains the length of the buffer allocated by the service provider and pointed to by <i>lpCalleeData</i>-&gt;**buf**. A value of zero means passing user data back to the caller is not supported. The condition function will copy up to <i>lpCalleeData</i>-&gt;**len** bytes of data into <i>lpCalleeData</i>-&gt;**buf**, and then update <i>lpCalleeData</i>-&gt;**len** to indicate the actual number of bytes transferred. If no user data is to be passed back to the caller, the condition function will set <i>lpCalleeData</i>-&gt;**len** to zero. The format of all address and user data is specific to the address family to which the socket belongs.

The <i>dwCallbackData</i> parameter value passed to the condition function is the value passed as the <i>dwCallbackData</i> parameter in the original **LPWSPAccept** call. This value is interpreted only by the Windows Sockets 2 client. This allows a client to pass some context information from the **LPWSPAccept** call site through to the condition function, which provides the condition function with any additional information required to determine whether to accept the connection. A typical usage is to pass a (suitably cast) pointer to a data structure containing references to application-defined objects with which this socket is associated.

## -see-also

[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">LPWSPEventSelect</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockOpt</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspselect">LPWSPSelect</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

