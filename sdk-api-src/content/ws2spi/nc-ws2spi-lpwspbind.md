---
UID: NC:ws2spi.LPWSPBIND
title: LPWSPBIND
description: The LPWSPBind function associates a local address (that is, name) with a socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPBIND"]
ms.date: 9/12/2019
ms.keywords: LPWSPBIND
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
 - LPWSPBIND
f1_keywords:
 - LPWSPBIND
 - ws2spi/LPWSPBIND
---

## -description

The **LPWSPBind** function associates a local address (that is, name) with a socket.

## -parameters

### -param s [in]

A descriptor identifying an unbound socket.

### -param name [in]

The address to assign to the socket, in the form of a <a href="/windows/win32/winsock/sockaddr-2">**sockaddr**</a> structure.

Except for the **sa_family** member, <a href="/windows/win32/winsock/sockaddr-2">**sockaddr**</a> contents are expressed in network byte order. In Windows Sockets 2, the <i>name</i> parameter is not strictly interpreted as a pointer to a **sockaddr** structure. It is cast this way for Winsock compatibility. The actual structure is interpreted differently in the context of different address families. The only requirements are that the first **u_short** is the address family and the total size of the memory buffer, in bytes, is <i>namelen</i>.

### -param namelen [in]

The length, in bytes, of structure pointed to by the <i>name</i> parameter.

### -param lpErrno [out]

A pointer to the error code.

## -returns

If no error occurs, **LPWSPBind** returns zero. Otherwise, it returns SOCKET_ERROR, and a specific error code is available in <i>lpErrno</i>.

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
Some process on the local computer has already bound to the same fully qualified address (for example, IP address and port in the **AF_INET** case) and the socket has not been marked to allow address reuse with SO_REUSEADDR. (See the SO_REUSEADDR socket option under <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsetsockopt">LPWSPSetSockOpt</a>.) 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEADDRNOTAVAIL">WSAEADDRNOTAVAIL</a></b></dl>
</dl>
</td>
<td width="60%">
The specified address is not a valid address for this computer.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, the <i>namelen</i> parameter is too small, the <i>name</i> parameter contains incorrect address format for the associated address family, or the first two bytes of the memory block specified by <i>name</i> do not match the address family associated with the socket descriptor <i>s</i>. 
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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
The socket is already bound to an address.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
There are not enough buffers available, there are too many connections.
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

The **LPWSPBind** function is used on an unconnected connectionless or connection-oriented socket, before subsequent calls to the <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">**LPWSPConnect**</a> or <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">**LPWSPListen**</a> functions. When a socket is created with <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">**LPWSPSocket**</a>, it exists in a namespace (address family), but it has no name or local address assigned. The **LPWSPBind** function establishes the local association of the socket by assigning a local name to an unnamed socket.

As an example, in the Internet address family, a name consists of three parts: the address family, a host address, and a port number that identifies the Winsock SPI client. In Windows Sockets 2, the <i>name</i> parameter is not strictly interpreted as a pointer to a <a href="/windows/win32/winsock/sockaddr-2">**sockaddr**</a> structure. Service providers are free to regard it as a pointer to a block of memory of size <i>namelen</i>. The first two bytes in this block (corresponding to **sa_family** in the **sockaddr** declaration) must contain the address family that was used to create the socket. Otherwise, the error <a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEFAULT">WSAEFAULT</a></b> will be indicated.

If a Windows Sockets 2 SPI client does not care what local address is assigned to it, it will specify the manifest constant value **ADDR_ANY** for the **sa_data** member of the <i>name</i> parameter. This instructs the service provider to use any appropriate network address. For TCP/IP, if the port is specified as zero, the service provider will assign a unique port to the Winsock SPI client with a value between 1024 and 5000. The SPI client can use <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockname">**LPWSPGetSockName**</a> after **LPWSPBind** to learn the address and the port that has been assigned to it. However, note that if the Internet address is equal to INADDR_ANY, <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">**LPWSPGetSockOpt**</a> will not necessarily be able to supply the address until the socket is connected, since several addresses can be valid if the host is multihomed.

## -see-also

<a href="/windows/win32/winsock/sockaddr-2">sockaddr</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockname">LPWSPGetSockName</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsplisten">LPWSPListen</a>

<a href="/previous-versions/windows/hardware/network/ff566318(v=vs.85)">WSPSetSockOpt</a>

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a>