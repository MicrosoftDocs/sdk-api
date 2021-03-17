---
UID: NC:ws2spi.LPWSPRECVDISCONNECT
title: LPWSPRECVDISCONNECT
description: The LPWSPRecvDisconnect function terminates reception on a socket and retrieves the disconnect data, if the socket is connection oriented.
tech.root: winsock
helpviewer_keywords: ["LPWSPRECVDISCONNECT"]
ms.date: 9/12/2019
ms.keywords: LPWSPRECVDISCONNECT
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
 - LPWSPRECVDISCONNECT
f1_keywords:
 - LPWSPRECVDISCONNECT
 - ws2spi/LPWSPRECVDISCONNECT
---

## -description

The **LPWSPRecvDisconnect** function terminates reception on a socket and retrieves the disconnect data, if the socket is connection oriented.

## -parameters

### -param s [in]

Descriptor identifying a socket.

### -param lpInboundDisconnectData [out]

Pointer to a buffer into which disconnect data is to be copied.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPRecvDisconnect** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></dt>
</dl>
</td>
<td width="60%">
Buffer referenced by the parameter <i>lpInboundDisconnectData</i> is too small.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a></dt>
</dl>
</td>
<td width="60%">
Disconnect data is not supported by the indicated protocol family.  
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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a></dt>
</dl>
</td>
<td width="60%">
Socket is not connected (connection-oriented sockets only).  
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
</table>

## -remarks

**LPWSPRecvDisconnect** is used on connection-oriented sockets to disable reception, and retrieve any incoming disconnect data from the remote party.

After this function has been successfully issued, subsequent receives on the socket will be disallowed. This has no effect on the lower protocol layers. For TCP, the TCP window is not changed and incoming data will be accepted (but not acknowledged) until the window is exhausted. For UDP, incoming datagrams are accepted and queued. In no case will an ICMP error packet be generated.

To successfully receive incoming disconnect data, a Windows Sockets SPI client must use other mechanisms to determine that the circuit has been closed. For example, a client needs to receive an FD_CLOSE notification, or get a zero return value, or a <b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEDISCON">WSAEDISCON</a></b> error code from <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b>.

Note that **LPWSPRecvDisconnect** does not close the socket, and resources attached to the socket will not be freed until <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b> is invoked.

> [!Note]  
> **LPWSPRecvDisconnect** does not block regardless of the SO_LINGER setting on the socket. A Windows Sockets SPI client should not rely on being able to reuse a socket after it has been **LPWSPRecvDisconnect**ed. In particular, a Windows Sockets provider is not required to support the use of <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> on such a socket.

## -see-also

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

