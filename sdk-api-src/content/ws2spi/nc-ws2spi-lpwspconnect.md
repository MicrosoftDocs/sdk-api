---
UID: NC:ws2spi.LPWSPCONNECT
title: LPWSPCONNECT
description: The LPWSPConnect function establishes a connection to a peer, exchanges connect data, and specifies needed quality of service based on the supplied flow specification.
tech.root: winsock
helpviewer_keywords: ["LPWSPCONNECT"]
ms.date: 9/12/2019
ms.keywords: LPWSPCONNECT
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
 - LPWSPCONNECT
f1_keywords:
 - LPWSPCONNECT
 - ws2spi/LPWSPCONNECT
---

## -description

The **LPWSPConnect** function establishes a connection to a peer, exchanges connect data, and specifies needed quality of service based on the supplied flow specification.

## -parameters

### -param s [in]

Descriptor identifying an unconnected socket.

### -param name [in]

Name of the peer to which the socket in the <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> is to be connected.

### -param namelen [in]

Length of the <i>name</i>, in bytes.

### -param lpCallerData [in]

Pointer to the user data that is to be transferred to the peer during connection establishment.

### -param lpCalleeData [out]

Pointer to a buffer into which any user data received from the peer during connection establishment can be copied.

### -param lpSQOS [in]

Pointer to the flow specifications for socket <i>s</i>, one for each direction.

### -param lpGQOS [in]

Reserved.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPConnect** returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.

On a blocking socket, the return value indicates success or failure of the connection attempt. If the return error code indicates the connection attempt failed (that is, <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNREFUSED">WSAECONNREFUSED</a>, <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETUNREACH">WSAENETUNREACH</a>, <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAETIMEDOUT">WSAETIMEDOUT</a>) the Winsock SPI client can call **LPWSPConnect** again for the same socket.

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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEADDRINUSE">WSAEADDRINUSE</a></b></dl>
</dl>
</td>
<td width="60%">
Local address of the socket is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs at the time of bind, but could be delayed until this function if the bind was to a partially wildcard address (involving ADDR_ANY) and if a specific address needs to be committed at the time of this function. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINTR">WSAEINTR</a></b></dl>
</dl>
</td>
<td width="60%">
(Blocking) call was canceled through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">LPWSPCancelBlockingCall</a></b>. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
Blocking Winsock call is in progress or the service provider is still processing a callback function. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEALREADY">WSAEALREADY</a></b></dl>
</dl>
</td>
<td width="60%">
Nonblocking <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> call is in progress on the specified socket. <br/> In order to preserve backward compatibility, this error is reported as WSAEINVAL to Windows Sockets 1.1 applications that link to either Winsock.dll or Wsock32.dll. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEADDRNOTAVAIL">WSAEADDRNOTAVAIL</a></b></dl>
</dl>
</td>
<td width="60%">
Remote address is not a valid address (for example, ADDR_ANY). 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEAFNOSUPPORT">WSAEAFNOSUPPORT</a></b></dl>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNREFUSED">WSAECONNREFUSED</a></b></dl>
</dl>
</td>
<td width="60%">
An attempt to connect was rejected.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, the <i>namelen</i> parameter is too small, the buffer length for <i>lpCalleeData</i>, <i>lpSQOS</i>, and <i>lpGQOS</i> is too small, or the buffer length for <i>lpCallerData</i> is too large.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
Parameter <i>s</i> is a listening socket.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEISCONN">WSAEISCONN</a></b></dl>
</dl>
</td>
<td width="60%">
Socket is already connected (connection-oriented sockets only).
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETUNREACH">WSAENETUNREACH</a></b></dl>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be connected.
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
Flow specifications specified in <i>lpSQOS</i> cannot be satisfied.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEPROTONOSUPPORT">WSAEPROTONOSUPPORT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpCallerData</i> augment is not supported by the service provider.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAETIMEDOUT">WSAETIMEDOUT</a></b></dl>
</dl>
</td>
<td width="60%">
An attempt to connect timed out without establishing a connection.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a></b></dl>
</dl>
</td>
<td width="60%">
Socket is marked as nonblocking and the connection cannot be completed immediately. It is possible to select the socket using the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspselect">LPWSPSelect</a></b> function while it is connecting by using the **WSPSelect** function to select it for writing.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEACCES">WSAEACCES</a></b></dl>
</dl>
</td>
<td width="60%">
An attempt to connect datagram socket to broadcast address failed because <b><a href="/previous-versions/windows/hardware/network/ff566318(v=vs.85)">WSPSetSockOpt</a></b> SO_BROADCAST is not enabled.
</td>
</tr>
</table>

## -remarks

This function is used to create a connection to the specified destination and to perform a number of other ancillary operations that occur at connect time as well. If the socket, <i>s</i>, is unbound, unique values are assigned to the local association by the system and the socket is marked as bound.

For connection-oriented sockets (for example, type SOCK_STREAM), an active connection is initiated to the specified host using <i>name</i> (an address in the namespace of the socket. For a detailed description, see <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>. When this call completes successfully, the socket is ready to send and receive data. If the address member of the **name** structure is all zeroes, **LPWSPConnect** will return the error <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEADDRNOTAVAIL">WSAEADDRNOTAVAIL</a>. Any attempt to reconnect an active connection will fail with the error code <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEISCONN">WSAEISCONN</a>.

For connection-oriented, nonblocking sockets it is often not possible to complete the connection immediately. In such a case, this function returns with the error <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEWOULDBLOCK">WSAEWOULDBLOCK</a> but the operation proceeds. When the success or failure outcome becomes known, it may be reported in one of several ways depending on how the client registers for notification. If the client uses <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspselect">LPWSPSelect</a></b>, success is reported in the <i>writefds</i> set and failure is reported in the <i>exceptfds</i> set. If the client uses **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** or <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">LPWSPEventSelect</a></b>, the notification is announced with FD_CONNECT and the error code associated with the FD_CONNECT indicates either success or a specific reason for failure.

For a connectionless socket (for example, type SOCK_DGRAM), the operation performed by **LPWSPConnect** is to establish a default destination address so the socket can be used with subsequent connection-oriented send and receive operations (<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b>). Any datagrams received from an address other than the destination address specified will be discarded. If the address member of the <i>name</i> structure is all zeroes, the socket will be disconnected— the default remote address will be indeterminate, so **LPWSPSend** and **LPWSPRecv** calls will return the error code <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a>. However, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b> and <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecvfrom">LPWSPRecvFrom</a></b> can still be used. The default destination can be changed by simply calling **LPWSPConnect** again, even if the socket is already connected. Any datagrams queued for receipt are discarded if <i>name</i> is different from the previous **LPWSPConnect**.

For connectionless sockets, <i>name</i> can indicate any valid address, including a broadcast address. However, to connect to a broadcast address, a socket must have <b><a href="/previous-versions/windows/hardware/network/ff566318(v=vs.85)">WSPSetSockOpt</a></b> SO_BROADCAST enabled. Otherwise, **LPWSPConnect** will fail with the error code <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEACCES">WSAEACCES</a>.

On connectionless sockets, exchange of user-to-user data is not possible and the corresponding parameters will be silently ignored.

The Winsock SPI client is responsible for allocating any memory space pointed to directly or indirectly by any of the parameters it specifies.

The <i>lpCallerData</i> is a value parameter that contains any user data to be sent along with the connection request. If <i>lpCallerData</i> is null, no user data will be passed to the peer. The <i>lpCalleeData</i> is a result parameter that will reference any user data passed back from the peer as part of the connection establishment. The <i>lpCalleeData</i>-&gt;**len** initially contains the length of the buffer allocated by the Winsock SPI client and pointed to by <i>lpCalleeData</i>-&gt;**buf**. The <i>lpCalleeData</i>-&gt;**len** will be set to zero if no user data has been passed back. The <i>lpCalleeData</i> information will be valid when the connection operation is complete. For blocking sockets, this will be when the **LPWSPConnect** function returns. For nonblocking sockets, this will be after the FD_CONNECT notification has occurred. If <i>lpCalleeData</i> is null, no user data will be passed back. The exact format of the user data is specific to the address family the socket belongs to and/or the applications involved.

At connect time, a Winsock SPI client can use the <i>lpSQOS</i> parameter to override any previous QoS specification made for the socket through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b> with the SIO_SET_QOS opcode.

The <i>lpSQOS</i> specifies the flow specifications for socket <i>s</i>, one for each direction, followed by any additional provider-specific parameters. If either the associated transport provider in general or the specific type of socket in particular cannot honor the QoS request, an error will be returned as indicated below. The sending or receiving flow specification values will be ignored, respectively, for any unidirectional sockets. If no provider-specific parameters are supplied, the **buf** and **len** members of <i>lpSQOS</i>-&gt;**ProviderSpecific** should be set to null and zero, respectively. A null value for <i>lpSQOS</i> indicates that no application supplied quality of service.

> [!Note]  
> When connected sockets break (that is, become closed for whatever reason), they should be discarded and recreated. It is safest to assume that when things go awry for any reason on a connected socket, the Winsock SPI client must discard and recreate the needed sockets in order to return to a stable point.

## -see-also

[LPWSPAccept](nc-ws2spi-lpwspaccept.md)

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspenumnetworkevents">LPWSPEnumNetworkEvents</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">LPWSPEventSelect</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockname">LPWSPGetSockName</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspselect">LPWSPSelect</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>