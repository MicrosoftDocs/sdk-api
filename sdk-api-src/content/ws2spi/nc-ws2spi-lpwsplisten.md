---
UID: NC:ws2spi.LPWSPLISTEN
title: LPWSPLISTEN
description: The LPWSPListen function establishes a socket to listen for incoming connections.
tech.root: winsock
helpviewer_keywords: ["LPWSPLISTEN"]
ms.date: 9/12/2019
ms.keywords: LPWSPLISTEN
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
 - LPWSPLISTEN
f1_keywords:
 - LPWSPLISTEN
 - ws2spi/LPWSPLISTEN
---

## -description

The **LPWSPListen** function establishes a socket to listen for incoming connections.

## -parameters

### -param s [in]

Descriptor identifying a bound, unconnected socket.

### -param backlog [in]

Maximum length to which the queue of pending connections can grow. If this value is SOMAXCONN, then the service provider should set the backlog to a maximum "reasonable" value. There is no standard provision to find out the actual backlog value.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPListen** returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEADDRINUSE">WSAEADDRINUSE</a></dt>
</dl>
</td>
<td width="60%">
Socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs at the time of <b><a href="/windows/win32/api/winsock/nf-winsock-bind">Bind</a></b>, but could be delayed until this function if the **bind** was to a partially wildcard address (involving ADDR_ANY) and if a specific address needs to be committed at the time of this function.
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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></dt>
</dl>
</td>
<td width="60%">
Socket has not been bound with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEISCONN">WSAEISCONN</a></dt>
</dl>
</td>
<td width="60%">
Socket is already connected.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMFILE">WSAEMFILE</a></dt>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></dt>
</dl>
</td>
<td width="60%">
No buffer space is available.
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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></dt>
</dl>
</td>
<td width="60%">
Referenced socket is not of a type that supports the <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b> operation.
</td>
</tr>
</table>

## -remarks

To accept connections, a socket is first created with <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a> bound to a local address with <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>, a backlog for incoming connections is specified with **LPWSPListen**, and then the connections are accepted with **[LPWSPAccept](nc-ws2spi-lpwspaccept.md)**. **LPWSPListen** applies only to sockets that are connection oriented (for example, SOCK_STREAM). The socket <i>s</i> is put into passive mode where incoming connection requests are acknowledged and queued pending acceptance by the Windows Sockets SPI client.

This function is typically used by servers that could have more than one connection request at a time: if a connection request arrives with the queue full, the client will receive an error with an indication of <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNREFUSED">WSAECONNREFUSED</a>.

**LPWSPListen** should continue to function rationally when there are no available descriptors. It should accept connections until the queue is emptied. If descriptors become available, a later call to **LPWSPListen** or **[LPWSPAccept](nc-ws2spi-lpwspaccept.md)** will refill the queue to the current or most recent backlog, if possible, and resume listening for incoming connections.

A Windows Sockets SPI client can call **LPWSPListen** more than once on the same socket. This has the effect of updating the current backlog for the listening socket. Should there be more pending connections than the new <i>backlog</i> value, the excess pending connections will be reset and dropped.

The <i>backlog</i> parameter is limited (silently) to a reasonable value as determined by the service provider. Illegal values are replaced by the nearest legal value. There is no standard provision to find out the actual backlog value.

## -see-also

**[LPWSPAccept](nc-ws2spi-lpwspaccept.md)**
   

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>
   

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>

