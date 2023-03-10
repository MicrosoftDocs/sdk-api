---
UID: NC:ws2spi.LPWSPSHUTDOWN
title: LPWSPSHUTDOWN
description: The LPWSPShutdown function disables sends and/or receives on a socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPSHUTDOWN"]
ms.date: 9/12/2019
ms.keywords: LPWSPSHUTDOWN
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
 - LPWSPSHUTDOWN
f1_keywords:
 - LPWSPSHUTDOWN
 - ws2spi/LPWSPSHUTDOWN
---

## -description

The **LPWSPShutdown** function disables sends and/or receives on a socket.

## -parameters

### -param s [in]

Descriptor identifying a socket.

### -param how [in]

Flag that describes what types of operation will no longer be allowed.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPShutdown** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
The <i>how</i> is not valid, or is not consistent with the socket type. For example, SD_SEND is used with a UNI_RECV socket type.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></dt>
</dl>
</td>
<td width="60%">
Function is invoked when a callback is in progress.
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

The **LPWSPShutdown** function is used on all types of sockets to disable reception, transmission, or both.

If <i>how</i> is SD_RECEIVE, subsequent receives on the socket will be disallowed. This has no effect on the lower protocol layers. For TCP sockets, if there is still data queued on the socket waiting to be received, or data arrives subsequently, the connection is reset, since the data cannot be delivered to the user. For UDP sockets, incoming datagrams are accepted and queued. In no case will an ICMP error packet be generated.

If <i>how</i> is SD_SEND, subsequent sends on the socket are disallowed. For TCP sockets, a FIN will be sent. Setting <i>how</i> to SD_BOTH disables both sends and receives as described above.

Note that **LPWSPShutdown** does not close the socket, and resources attached to the socket will not be freed until <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b> is invoked.

> [!Note]  
> The **LPWSPShutdown** function does not block regardless of the SO_LINGER setting on the socket. A Windows Sockets SPI client should not rely on being able to reuse a socket after it has been shut down. In particular, a Windows Sockets service provider is not required to support the use of <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> on such a socket.

## -see-also

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

