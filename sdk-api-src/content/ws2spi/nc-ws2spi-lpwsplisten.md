---
UID: NC:ws2spi.LPWSPLISTEN
title: LPWSPLISTEN
description: The WSPListen function establishes a socket to listen for incoming connections.
ms.date: 9/12/2019
ms.keywords: LPWSPLISTEN
ms.topic: language-reference
targetos: Windows
product: Windows
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
---

## -description
The <b>LPWSPListen</b> function establishes a socket to listen for incoming connections.
## -parameters

### -param s [in]
Descriptor identifying a bound, unconnected socket.

### -param backlog [in]
Maximum length to which the queue of pending connections can grow. If this value is SOMAXCONN, then the service provider should set the backlog to a maximum "reasonable" value. There is no standard provision to find out the actual backlog value.

### -param lpErrno [out]
Pointer to the error code.

## -returns
If no error occurs, <b>LPWSPListen</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEADDRINUSE">WSAEADDRINUSE</a></dt>
</dl>
</td>
<td width="60%">
Socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs at the time of <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/winsock/nf-winsock-bind">Bind</a></b>, but could be delayed until this function if the <b>bind</b> was to a partially wildcard address (involving ADDR_ANY) and if a specific address needs to be committed at the time of this function.
</td>
</tr>
</table>
  
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md#wsaeinprogress)**   | Function is invoked when a callback is in progress.<br/>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md#wsaeinval)**             | Socket has not been bound with <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>.<br/>                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**[WSAEISCONN](windows-sockets-error-codes-2.md#wsaeisconn)**           | Socket is already connected.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**[WSAEMFILE](windows-sockets-error-codes-2.md#wsaemfile)**             | No more socket descriptors are available.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <dl> <dt>**[WSAENOBUFS](windows-sockets-error-codes-2.md#wsaenobufs)**           | No buffer space is available.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md#wsaenotsock)**         | The descriptor is not a socket.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**[WSAEOPNOTSUPP](windows-sockets-error-codes-2.md#wsaeopnotsupp)**     | Referenced socket is not of a type that supports the <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a></b> operation.<br/>                                                                                                                                                                                                                                                                                    |

## -remarks
To accept connections, a socket is first created with <a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a> bound to a local address with <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspbind">LPWSPBind</a></b>, a backlog for incoming connections is specified with <b>LPWSPListen</b>, and then the connections are accepted with <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspaccept">LPWSPAccept</a></b>. <b>LPWSPListen</b> applies only to sockets that are connection oriented (for example, SOCK_STREAM). The socket <i>s</i> is put into passive mode where incoming connection requests are acknowledged and queued pending acceptance by the Windows Sockets SPI client.

This function is typically used by servers that could have more than one connection request at a time: if a connection request arrives with the queue full, the client will receive an error with an indication of <a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNREFUSED">WSAECONNREFUSED</a>.

<b>LPWSPListen</b> should continue to function rationally when there are no available descriptors. It should accept connections until the queue is emptied. If descriptors become available, a later call to <b>LPWSPListen</b> or <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspaccept">LPWSPAccept</a></b> will refill the queue to the current or most recent backlog, if possible, and resume listening for incoming connections.

A Windows Sockets SPI client can call <b>LPWSPListen</b> more than once on the same socket. This has the effect of updating the current backlog for the listening socket. Should there be more pending connections than the new <i>backlog</i> value, the excess pending connections will be reset and dropped.

The <i>backlog</i> parameter is limited (silently) to a reasonable value as determined by the service provider. Illegal values are replaced by the nearest legal value. There is no standard provision to find out the actual backlog value.

## -see-also
<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspaccept">LPWSPAccept</a></b>
   

<b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>
   

<a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>
  
