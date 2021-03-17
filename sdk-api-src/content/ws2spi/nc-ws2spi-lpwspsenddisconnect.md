---
UID: NC:ws2spi.LPWSPSENDDISCONNECT
title: LPWSPSENDDISCONNECT
description: The LPWSPSendDisconnect function initiates termination of the connection for the socket and sends disconnect data.
tech.root: winsock
helpviewer_keywords: ["LPWSPSENDDISCONNECT"]
ms.date: 9/12/2019
ms.keywords: LPWSPSENDDISCONNECT
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
 - LPWSPSENDDISCONNECT
f1_keywords:
 - LPWSPSENDDISCONNECT
 - ws2spi/LPWSPSENDDISCONNECT
---

## -description

The **LPWSPSendDisconnect** function initiates termination of the connection for the socket and sends disconnect data.

## -parameters

### -param s [in]

Descriptor identifying a socket.

### -param lpOutboundDisconnectData [in]

Pointer to the outgoing disconnect data.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPSendDisconnect** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOPROTOOPT">WSAENOPROTOOPT</a></dt>
</dl>
</td>
<td width="60%">
Parameter <i>lpOutboundDisconnectData</i> is not null, and the disconnect data is not supported by the service provider.  
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

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></dt>
</dl>
</td>
<td width="60%">
The <i>lpOutboundDisconnectData</i> parameter is not totally contained in a valid part of the user address space.
</td>
</tr>
</table>

## -remarks

The **LPWSPSendDisconnect** function is used on connection-oriented sockets to disable transmission, and to initiate termination of the connection along with the transmission of disconnect data, if any.

After this function has been successfully issued, subsequent sends are disallowed.

The <i>lpOutboundDisconnectData</i> parameter, if not null, points to a buffer containing the outgoing disconnect data to be sent to the remote party.

Note that **LPWSPSendDisconnect** does not close the socket, and that resources attached to the socket will not be freed until <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b> is invoked.

> [!Note]  
> The **LPWSPSendDisconnect** function does not block regardless of the SO_LINGER setting on the socket. A Windows Sockets SPI client should not rely on being able to reuse a socket after it has been disconnected. In particular, a Windows Sockets provider is not required to support the use of <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> on such a socket.

## -see-also

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

