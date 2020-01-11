---
UID: NC:ws2spi.LPWSPASYNCSELECT
title: LPWSPASYNCSELECT
description: The LPWSPAsyncSelect function requests Windows message-based event notification of network events for a socket.
ms.date: 9/12/2019
ms.keywords: LPWSPASYNCSELECT
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- LPWSPASYNCSELECT
---

## -description
The **LPWSPAsyncSelect** function requests Windows message-based event notification of network events for a socket.

## -parameters

### -param s [in]

Descriptor identifying the socket for which event notification is required.

### -param hWnd [in]

Handle identifying the window that should receive a message when a network event occurs.

### -param wMsg [in]

Message to be sent when a network event occurs.

### -param lEvent [in]

Bitmask that specifies a combination of network events in which the Windows Sockets SPI client is interested.

### -param lpErrno [out]

Pointer to the error code.

## -returns

The return value is zero if the Winsock SPI client's declaration of interest in the network event set was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error Code </th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></b></dl>
</dl>
</td>
<td width="60%">
The network subsystem has failed. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></b></dl>
</dl>
</td>
<td width="60%">
The network subsystem has failed. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
Indicates that one of the specified parameters was invalid such as the window handle not referring to an existing window, or the specified socket is in an invalid state. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></b></dl>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.
</td>
</tr>
</table>

Additional error codes can be set when an application window receives a message. This error code is extracted from the <i>lParam</i> in the reply message using the **WSAGETSELECTERROR** macro. Possible error codes for each network event are listed in the following table.

### Event: FD_CONNECT
<table>
<tr>
<th> Error Code </th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEAFNOSUPPORT">WSAEAFNOSUPPORT</a></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNREFUSED">WSAECONNREFUSED</a></dt>
</dl>
</td>
<td width="60%">
The attempt to connect was rejected. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETUNREACH">WSAENETUNREACH</a></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></dt>
</dl>
</td>
<td width="60%">
The <i>namelen</i> parameter is invalid.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
The socket is already bound to an address.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEISCONN">WSAEISCONN</a></dt>
</dl>
</td>
<td width="60%">
The socket is already connected.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMFILE">WSAEMFILE</a></dt>
</dl>
</td>
<td width="60%">
No more file descriptors are available.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be connected.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAETIMEDOUT">WSAETIMEDOUT</a></dt>
</dl>
</td>
<td width="60%">
Attempt to connect timed out without establishing a connection.
</td>
</tr>

</table>

### Event: FD_CLOSE
<table>
<tr>
<th> Error Code </th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></dt>
</dl>
</td>
<td width="60%">
The network subsystem failed. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNRESET">WSAECONNRESET</a></dt>
</dl>
</td>
<td width="60%">
The connection was reset by the remote side.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNABORTED">WSAECONNABORTED</a></dt>
</dl>
</td>
<td width="60%">
The connection was terminated due to a time-out or other failure.
</td>
</tr>

</table>

### Event...: FD_ACCEPT, FD_ADDRESS_LIST_CHANGE, FD_GROUP_QOS, FD_OOB, FD_QOS, FD_READ, FD_WRITE

<table>
<tr>
<th> Error Code </th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></dt>
</dl>
</td>
<td width="60%">
The network subsystem failed.
</td>
</tr>
</table>

### Event: FD_ROUTING_INTERFACE_CHANGE

<table>
<tr>
<th> Error Code </th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETUNREACH">WSAENETUNREACH</a></dt>
</dl>
</td>
<td width="60%">
The specified destination is no longer reachable.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></dt>
</dl>
</td>
<td width="60%">
The network subsystem failed.
</td>
</tr>
</table>

## -remarks

This function is used to request that the service provider send a Windows message to the client's window <i>hWnd</i> whenever it detects any of the network events specified by the <i>lEvent</i> parameter. The service provider should use the <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nf-ws2spi-wpupostmessage">WPUPostMessage</a>  function to post the message. The message to be sent is specified by the <i>wMsg</i> parameter. The socket for which notification is required is identified by <i>s</i>.

This function automatically sets socket <i>s</i> to nonblocking mode, regardless of the value of <i>lEvent</i>. See <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b> about how to set the socket back to blocking mode.

The <i>lEvent</i> parameter is constructed by using the bitwise OR operator with any of the values specified in the following list.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_READ
</dt>
</dl>
</td>
<td width="60%">
Issues notification of readiness for reading.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_WRITE
</dt>
</dl>
</td>
<td width="60%">
Issues notification of readiness for writing.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_OOB
</dt>
</dl>
</td>
<td width="60%">
Issues notification of the arrival of OOB data.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_ACCEPT
</dt>
</dl>
</td>
<td width="60%">
Issues notification of incoming connections.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_CONNECT
</dt>
</dl>
</td>
<td width="60%">
Issues notification of completed connections.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_CLOSE
</dt>
</dl>
</td>
<td width="60%">
Issues notification of socket closure.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_QOS
</dt>
</dl>
</td>
<td width="60%">
Issues notification of socket (QoS) changes.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_GROUP_QOS
</dt>
</dl>
</td>
<td width="60%">
Reserved.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_ROUTING_INTERFACE_CHANGE
</dt>
</dl>
</td>
<td width="60%">
Issues notification of routing interface change for the specified destination.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt>
FD_ADDRESS_ LIST_CHANGE
</dt>
</dl>
</td>
<td width="60%">
Issues notification of local address list change for the socket's protocol family.
</td>
</tr>
</table>

Invoking **LPWSPAsyncSelect** for a socket cancels any previous **LPWSPAsyncSelect** or <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">**LPWSPEventSelect**</a> for the same socket. For example, to receive notification for both reading and writing, the Winsock SPI client must call **LPWSPAsyncSelect** with both FD_READ and FD_WRITE, as follows:


```C++
rc = LPWSPAsyncSelect(s, hWnd, wMsg1, FD_READ, &amp;error);
rc = LPWSPAsyncSelect(s, hWnd, wMsg2, FD_WRITE, &amp;error);
```

To cancel all notification (for example, to indicate that the service provider should send no further messages related to network events on the socket) <i>LPWSPAsyncSelect</i> will be set to zero.


## -see-also

