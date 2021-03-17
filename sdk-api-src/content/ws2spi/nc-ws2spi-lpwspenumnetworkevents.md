---
UID: NC:ws2spi.LPWSPENUMNETWORKEVENTS
title: LPWSPENUMNETWORKEVENTS
description: The LPWSPEnumNetworkEvents function reports occurrences of network events for the indicated socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPENUMNETWORKEVENTS"]
ms.date: 9/12/2019
ms.keywords: LPWSPENUMNETWORKEVENTS
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
 - LPWSPENUMNETWORKEVENTS
f1_keywords:
 - LPWSPENUMNETWORKEVENTS
 - ws2spi/LPWSPENUMNETWORKEVENTS
---

## -description

The **LPWSPEnumNetworkEvents** function reports occurrences of network events for the indicated socket.

## -parameters

### -param s [in]

Descriptor identifying the socket.

### -param hEventObject [in]

Optional handle identifying an associated event object to be reset.

### -param lpNetworkEvents [out]

Pointer to a <a href="/windows/win32/api/winsock2/ns-winsock2-wsanetworkevents">WSANETWORKEVENTS</a> structure that is filled with a record of occurred network events and any associated error codes. The **WSANETWORKEVENTS** structure is defined in the following text.

### -param lpErrno [out]

Pointer to the error code.

## -returns

The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number is available in <i>lpErrno</i>.

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
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
Indicates that one of the specified parameters was invalid.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.
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

This function is used to report which network events have occurred for the indicated socket since the last invocation of this function. It is intended for use in conjunction with [LPWSPEventSelect](./nc-ws2spi-lpwspeventselect.md) and [LPWSPAsyncSelect](./nc-ws2spi-lpwspasyncselect.md), which associate an event object with one or more network events. Recording of network events commences when **LPWSPEventSelect** or **LPWSPAsyncSelect** is called with a nonzero <i>lNetworkEvents</i> argument, and remains in effect until another corresponding call is made to **LPWSPEventSelect** or **LPWSPAsyncSelect** with the <i>lNetworkEvents</i> argument set to zero.

**LPWSPEnumNetworkEvents** only reports network activity and errors nominated through <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">LPWSPEventSelect</a></b>. See the descriptions of <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspselect">LPWSPSelect</a></b> and **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** to find out how those functions report network activity and errors.

The socket's internal record of network events is copied to the structure referenced by <i>lpNetworkEvents</i>, whereafter the internal network events record is cleared. If <i>hEventObject</i> is non-null, the indicated event object is also reset. The Windows Sockets provider guarantees that the operations of copying the network event record, clearing it, and resetting any associated event object are atomic, such that the next occurrence of a nominated network event will cause the event object to become set. In the case of this function returning SOCKET_ERROR, the associated event object is not reset and the record of network events is not cleared.

The <a href="/windows/win32/api/winsock2/ns-winsock2-wsanetworkevents">WSANETWORKEVENTS</a> structure is defined on the <a href="/windows/win32/api/winsock2/ns-winsock2-wsanetworkevents">WSANETWORKEVENTS</a> reference page.

The **lNetworkEvents** member of the <a href="/windows/win32/api/winsock2/ns-winsock2-wsanetworkevents">WSANETWORKEVENTS</a> structure indicates which of the FD_XXX network events have occurred. The <i>iErrorCode</i> array is used to contain any associated error codes, with array index corresponding to the position of event bits in **lNetworkEvents**. The identifiers such as FD_READ_BIT and FD_WRITE_BIT can be used to index the <i>iErrorCode</i> array.

Note that only those elements of the <i>iErrorCode</i> array are set that correspond to the bits set in the **lNetworkEvents** member. Other members are not modified (this is important for backward compatibility with the Windows Socket 2 SPI clients that are not aware of new FD_ROUTING_INTERFACE_CHANGE and FD_ADDRESS_LIST_CHANGE events).

The following error codes can be returned along with the respective network event.

### Event: FD_CONNECT

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEAFNOSUPPORT">WSAEAFNOSUPPORT</a></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNREFUSED">WSAECONNREFUSED</a></dt>
</dl>
</td>
<td width="60%">
An attempt to connect was forcefully rejected. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETUNREACH">WSAENETUNREACH</a></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time. 
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be connected.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAETIMEDOUT">WSAETIMEDOUT</a></dt>
</dl>
</td>
<td width="60%">
An attempt to connect timed out without establishing a connection.
</td>
</tr>
</table>

### Event: FD_CLOSE

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
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNRESET">WSAECONNRESET</a></dt>
</dl>
</td>
<td width="60%">
The connection was reset by the remote side.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAECONNABORTED">WSAECONNABORTED</a></dt>
</dl>
</td>
<td width="60%">
The connection was terminated due to a time-out or other failure.  
</td>
</tr>
</table>

### Event: FD_READ, FD_WRITE, FD_OOB, FD_ACCEPT, FD_QOS, FD_GROUP_QOS, FD_ADDRESS_LIST_CHANGE

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
</table>

### Event: FD_ROUTING_INTERFACE_CHANGE

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETUNREACH">WSAENETUNREACH</a></dt>
</dl>
</td>
<td width="60%">
The specified destination is no longer reachable. 
</td>
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
</table>

## -see-also

<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">LPWSPEventSelect</a>