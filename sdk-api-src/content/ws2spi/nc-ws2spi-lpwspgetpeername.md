---
UID: NC:ws2spi.LPWSPGETPEERNAME
title: LPWSPGETPEERNAME
description: The LPWSPGetPeerName function gets the address of the peer to which a socket is connected.
tech.root: winsock
helpviewer_keywords: ["LPWSPGETPEERNAME"]
ms.date: 9/12/2019
ms.keywords: LPWSPGETPEERNAME
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
 - LPWSPGETPEERNAME
f1_keywords:
 - LPWSPGETPEERNAME
 - ws2spi/LPWSPGETPEERNAME
---

## -description

The **LPWSPGetPeerName** function gets the address of the peer to which a socket is connected.

## -parameters

### -param s [in]

Descriptor identifying a connected socket.

### -param name [out]

Pointer to the <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> structure to receive the name of the peer.

### -param namelen [in, out]

On input, pointer to an integer that indicates the size of the structure pointed to by <i>name</i>, in bytes. On output, indicates the size of the returned name, in bytes.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPGetPeerName** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error Code</th>
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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, or the <i>namelen</i> parameter is too small.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
Function is invoked when a callback is in progress.
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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTCONN">WSAENOTCONN</a></b></dl>
</dl>
</td>
<td width="60%">
Socket is not connected.
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
</table>

## -remarks

The **LPWSPGetPeerName** function supplies the name of the peer connected to the socket <i>s</i> and stores it in the structure <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> referenced by <i>name</i>. It can be used only on a connected socket. For datagram sockets, only the name of a peer specified in a previous <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> call will be returned and any name specified by a previous <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsendto">LPWSPSendTo</a></b> call will not be returned by **LPWSPGetPeerName**.

On return, the <i>namelen</i> parameter contains the actual size of the name returned in bytes.

## -see-also

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockname">LPWSPGetSockName</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

