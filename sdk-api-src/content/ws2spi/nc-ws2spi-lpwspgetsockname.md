---
UID: NC:ws2spi.LPWSPGETSOCKNAME
title: LPWSPGETSOCKNAME
description: The LPWSPGetSockName function gets the local name for a socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPGETSOCKNAME"]
ms.date: 9/12/2019
ms.keywords: LPWSPGETSOCKNAME
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
 - LPWSPGETSOCKNAME
f1_keywords:
 - LPWSPGETSOCKNAME
 - ws2spi/LPWSPGETSOCKNAME
---

## -description

The **LPWSPGetSockName** function gets the local name for a socket.

## -parameters

### -param s [in]

Descriptor identifying a bound socket.

### -param name [out]

Pointer to a <b><a href="/windows/win32/winsock/sockaddr-2">sockaddr</a></b> structure used to supply the address (name) of the socket.

### -param namelen [in, out]

On input, pointer to an integer that indicates the size of the structure pointed to by <i>name</i>, in bytes. On output indicates the size of the returned name, in bytes.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPGetSockName** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
Socket has not been bound to an address with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>, or ADDR_ANY is specified in **LPWSPBind** but connection has not yet occurred.  
</td>
</tr>
</table>

## -remarks

**LPWSPGetSockName** retrieves the current name for the specified socket descriptor in <i>name</i>. It is used on a bound and/or connected socket specified by the <i>s</i> parameter. The local association is returned. This call is especially useful when a <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> call has been made without doing a <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b> first; as this call provides the only means by which the local association that has been set by the service provider can be determined.

If a socket was bound to an unspecified address (for example, ADDR_ANY), indicating that any of the host's addresses within the specified address family should be used for the socket, **LPWSPGetSockName** will <i>not</i> necessarily return information about the host address, unless the socket has been connected with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b> or **[LPWSPAccept](nc-ws2spi-lpwspaccept.md)**. The Windows Sockets SPI client must not assume that an address will be specified unless the socket is connected. This is because for a multihomed host, the address that will be used for the socket is unknown until the socket is connected.

## -see-also

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetpeername">LPWSPGetPeerName</a></b>

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a></b>
</dt> </dl>

