---
UID: NC:ws2spi.LPWSPACCEPT
title: LPWSPACCEPT (ws2spi.h)
author: windows-sdk-content
description: The WSPAccept function conditionally accepts a connection based on the return value of a condition function.
old-location: winsock\wspaccept_2.htm
tech.root: WinSock
ms.assetid: d73aa3a8-cef5-485d-b2ba-b2fe42ab6200
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPWSPACCEPT, WSPAccept, WSPAccept function [Winsock], _win32_wspaccept_2, winsock.wspaccept_2, ws2spi/WSPAccept
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WSPAccept
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPWSPACCEPT callback function


## -description


The 
<b>WSPAccept</b> function conditionally accepts a connection based on the return value of a condition function.


## -parameters




### -param s [in]

Descriptor identifying a socket that is listening for connections after a 
<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566297(v%3dvs.85)">WSPListen</a>.


### -param *addr [out]

Optional pointer to a buffer that receives the address of the connecting entity, as known to the service provider. The exact format of the <i>addr</i> parameter is determined by the address family established when the socket in the 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure was created.


### -param addrlen [in, out]

Optional pointer to an integer that contains the length of the <i>addr</i> parameter, in bytes.


### -param lpfnCondition [in]

Procedure instance address of an optional-condition function furnished by Windows Sockets. This function is used in the accept or reject decision based on the caller information passed in as parameters.


### -param dwCallbackData [in]

Callback data to be passed back to the Windows Socket 2 client as the value of the <i>dwCallbackData</i> parameter of the condition function. This parameter is not interpreted by the service provider.


### -param lpErrno [out]

Pointer to the error code.


## -returns



If no error occurs, 
<b>WSPAccept</b> returns a value of type SOCKET that is a descriptor for the accepted socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a></b></dt>
</dl>
</td>
<td width="60%">
The connection request was forcefully rejected as indicated in the return value of the condition function (CF_REJECT).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
An incoming connection was indicated, but was subsequently terminated by the remote peer prior to accepting the call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>addrlen</i> parameter is too small or the <i>lpfnCondition</i> parameter is not part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A (blocking) call was canceled through 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)">WSPCancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets call is in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566297(v%3dvs.85)">WSPListen</a> was not invoked prior to 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspaccept">WSPAccept</a>, parameter <i>g</i> specified in the condition function is not a valid value, the return value of the condition function is not a valid one, or any case where the specified socket is in an invalid state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></b></dt>
</dl>
</td>
<td width="60%">
Queue is nonempty upon entry to 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspaccept">WSPAccept</a> and there are no socket descriptors available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
Referenced socket is not a type that supports connection-oriented service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
Acceptance of the connection request was deferred as indicated in the return value of the condition function (CF_DEFER).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
Socket is marked as nonblocking and no connections are present to be accepted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The connection request that was offered has timed out or been withdrawn.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



The 
<b>WSPAccept</b> function extracts the first connection on the queue of pending connections on socket <i>s</i>, and checks it against the condition function, provided the condition function is specified (that is, not null). The condition function must be executed in the same thread as this routine. If the condition function returns CF_ACCEPT, 
<b>WSPAccept</b> creates a new socket.

Newly created sockets have the same properties as the socket <i>s</i>, including network events registered with 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)">WSPAsyncSelect</a> or with 
<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566287(v%3dvs.85)">WSPEventSelect</a>. As described in 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/descriptor-allocation-2">DescriptorAllocation</a>, when new socket descriptors are allocated, IFS providers must call 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a> and non-IFS providers must call 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>.

If the condition function returns CF_REJECT, 
<b>WSPAccept</b> rejects the connection request. If the application's accept/reject decision cannot be made immediately, the condition function will return CF_DEFER to indicate that no decision has been made. No action about this connection request is to be taken by the service provider. When the application is ready to take action on the connection request, it will invoke 
<b>WSPAccept</b> again and return either CF_ACCEPT or CF_REJECT as a return value from the condition function.

For sockets that are in the (default) blocking mode, if no pending connections are present on the queue, 
<b>WSPAccept</b> blocks the caller until a connection is present. For sockets in nonblocking mode, if this function is called when no pending connections are present on the queue, 
<b>WSPAccept</b> returns the error code 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a>. The accepted socket cannot be used to accept more connections. The original socket remains open.

The parameter <i>addr</i> is a result parameter that is filled with the address of the connecting entity, as known to the service provider. The exact format of the <i>addr</i> parameter is determined by the address family in which the communication is occurring. The <i>addrlen</i> is a value-result parameter; it will initially contain the amount of space pointed to by <i>addr</i>. On return, it must contain the actual length (in bytes) of the address returned by the service provider. This call is used with connection-oriented socket types such as SOCK_STREAM. If <i>addr</i> and/or <i>addrlen</i> are equal to null, then no information about the remote address of the accepted socket is returned. Otherwise, these two parameters shall be filled in regardless of whether the condition function is specified or what it returns.

The prototype of the condition function is as follows:


```cpp

int CALLBACK ConditionFunc(
  IN LPWSABUF     lpCallerId, 
  IN LPWSABUF     lpCallerData, 
  IN OUT LPQOS    lpSQOS, 
  IN OUT LPQOS    lpGQOS,
  IN LPWSABUF     lpCalleeId, 
  IN LPWSABUF     lpCalleeData, 
  OUT GROUP FAR   *g, 
  IN DWORD        dwCallbackData 
);

```


The <i>lpCallerId</i> and <i>lpCallerData</i> are value parameters that must contain the address of the connecting entity and any user data that was sent along with the connection request. If no caller identifier or caller data is available, the corresponding parameter will be null. Many network protocols do not support connect-time caller data. Most conventional network protocols can be expected to support caller identifier information at connection-request time. The <b>buf</b> part of the 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2def/ns-ws2def-_wsabuf">WSABUF</a> pointed to by <i>lpCallerId</i> points to a 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>. The <b>sockaddr</b> is interpreted according to its address family (typically by casting the <b>sockaddr</b> to some type specific to the address family).

The <i>lpSQOS</i> parameter references the flow specifications for socket <i>s</i> specified by the caller, one for each direction, followed by any additional provider-specific parameters. The sending or receiving flow specification values will be ignored as appropriate for any unidirectional sockets. A null value for <i>lpSQOS</i> indicates that there is no caller-supplied QoS and that no negotiation is possible. A non-<b>NULL</b> <i>lpSQOS</i> pointer indicates that a QoS negotiation is to occur or that the provider is prepared to accept the QoS request without negotiation.

The <i>lpCalleeId</i> is a value parameter that contains the local address of the connected entity. The <b>buf</b> part of the 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2def/ns-ws2def-_wsabuf">WSABUF</a> pointed to by <i>lpCalleeId</i> points to a 
<a href="https://docs.microsoft.com/windows/desktop/WinSock/sockaddr-2">sockaddr</a>. The <b>sockaddr</b> is interpreted according to its address family (typically by casting the <b>sockaddr</b> to some type specific to the address family).

The <i>lpCalleeData</i> is a result parameter used by the condition function to supply user data back to the connecting entity. The storage for this data must be provided by the service provider. The <i>lpCalleeData</i>-&gt;<b>len</b> initially contains the length of the buffer allocated by the service provider and pointed to by <i>lpCalleeData</i>-&gt;<b>buf</b>. A value of zero means passing user data back to the caller is not supported. The condition function will copy up to <i>lpCalleeData</i>-&gt;<b>len</b> bytes of data into <i>lpCalleeData</i>-&gt;<b>buf</b>, and then update <i>lpCalleeData</i>-&gt;<b>len</b> to indicate the actual number of bytes transferred. If no user data is to be passed back to the caller, the condition function will set <i>lpCalleeData</i>-&gt;<b>len</b> to zero. The format of all address and user data is specific to the address family to which the socket belongs.

The <i>dwCallbackData</i> parameter value passed to the condition function is the value passed as the <i>dwCallbackData</i> parameter in the original 
<b>WSPAccept</b> call. This value is interpreted only by the Windows Sockets 2 client. This allows a client to pass some context information from the 
<b>WSPAccept</b> call site through to the condition function, which provides the condition function with any additional information required to determine whether to accept the connection. A typical usage is to pass a (suitably cast) pointer to a data structure containing references to application-defined objects with which this socket is associated.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)">WSPAsyncSelect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566268(v%3dvs.85)">WSPBind</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566275(v%3dvs.85)">WSPConnect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566287(v%3dvs.85)">WSPEventSelect</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566292(v%3dvs.85)">WSPGetSockOpt</a>



<a href="https://docs.microsoft.com/previous-versions/windows/hardware/network/ff566297(v%3dvs.85)">WSPListen</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)">WSPSelect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpwspsocket">WSPSocket</a>
 

 

