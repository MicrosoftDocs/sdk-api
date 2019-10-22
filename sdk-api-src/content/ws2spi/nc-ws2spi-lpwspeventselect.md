---
UID: NC:ws2spi.LPWSPEVENTSELECT
title: LPWSPEVENTSELECT
description: The LPWSPEventSelect function specifies an event object to be associated with the supplied set of network events.
ms.date: 9/12/2019
ms.keywords: LPWSPEVENTSELECT
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
 - LPWSPEVENTSELECT
---

## -description
The <b>LPWSPEventSelect</b> function specifies an event object to be associated with the supplied set of network events.

## -parameters

### -param s [in]
Descriptor identifying the socket.

### -param hEventObject [in]
Handle identifying the event object to be associated with the supplied set of network events.

### -param lNetworkEvents [in]
Bitmask that specifies the combination of network events in which the Windows Sockets SPI client has interest.

### -param lpErrno [out]
Pointer to the error code.

## -returns
The return value is zero if the Windows Sockets SPI client's specification of the network events and the associated event object was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error Code</th>
<th>Meaning</th>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENETDOWN">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINVAL">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
Indicates that one of the specified parameters was invalid, or the specified socket is in an invalid state.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAEINPROGRESS">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
Blocking Windows Sockets call is in progress or the service provider is still processing a callback function.
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="https://docs.microsoft.com/en-us/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOTSOCK">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.
</td>
</tr>
</table>

## -remarks
This function is used to specify an event object, <i>hEventObject</i>, to be associated with the selected network events, <i>lNetworkEvents</i>. The socket for which an event object is specified is identified by <i>s</i>. The event object is set when any of the nominated network events occur.

<b>LPWSPEventSelect</b> operates very similarly to <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspasyncselect">LPWSPAsyncSelect</a></b>, the difference being in the actions taken when a nominated network event occurs. Whereas <b>WSPAsyncSelect</b> causes a Windows Sockets SPI client-specified Windows message to be posted, <b>LPWSPEventSelect</b> sets the associated event object and records the occurrence of this event in an internal network event record. A Windows Sockets SPI client can use <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspenumnetworkevents">LPWSPEnumNetworkEvents</a></b> to retrieve the contents of the internal network event record and thus determine which of the nominated network events have occurred.

<b>LPWSPEventSelect</b> is the only function that causes network activity and errors to be recorded and retrievable through <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspenumnetworkevents">LPWSPEnumNetworkEvents</a></b>. See the descriptions of <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspselect">LPWSPSelect</a></b> and <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspasyncselect">LPWSPAsyncSelect</a></b> to find out how those functions report network activity and errors.

This function automatically sets socket <i>s</i> to nonblocking mode, regardless of the value of <i>lNetworkEvents</i>.

The <i>lNetworkEvents</i> parameter is constructed by using the bitwise OR operator with any of the values specified in the following list.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_READ
</dt>
</dl>
</td>
<td width="40%">
Issues notification of readiness for reading.  
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_WRITE
</dt>
</dl>
</td>
<td width="40%">
Issues notification of readiness for writing.  
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_OOB
</dt>
</dl>
</td>
<td width="40%">
Issues notification of the arrival of OOB data.  
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_ACCEPT
</dt>
</dl>
</td>
<td width="40%">
Issues notification of incoming connections.  
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_CONNECT
</dt>
</dl>
</td>
<td width="40%">
Issues notification of completed connection.   
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_CLOSE
</dt>
</dl>
</td>
<td width="40%">
Issues notification of socket closure.   
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_QOS
</dt>
</dl>
</td>
<td width="40%">
Issues notification of socket (QoS) changes.   
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_GROUP_QOS
</dt>
</dl>
</td>
<td width="40%">
Reserved.   
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_ROUTING_INTERFACE_CHANGE
</dt>
</dl>
</td>
<td width="40%">
Issues notification of routing interface changes for the specified destination(s).   
</td>
</tr>

<tr>
<td width="60%">
<dl>                                              
<dt>
FD_ADDRESS_LIST_CHANGE
</dt>
</dl>
</td>
<td width="40%">
Issues notification of local address list changes for the socket's address family.   
</td>
</tr>
</table>

Issuing a <b>LPWSPEventSelect</b> for a socket cancels any previous <b><a href="https://docs.microsoft.com/en-us/windows/win32/api/ws2spi/nc-ws2spi-lpwspasyncselect">LPWSPAsyncSelect</a></b> or <b>LPWSPEventSelect</b> for the same socket and clears the internal network event record. For example, to associate an event object with both reading and writing network events, the Windows Sockets SPI client must call <b>LPWSPEventSelect</b> with both FD_READ and FD_WRITE, as follows:


```C++
rc = LPWSPEventSelect(s, hEventObject1, FD_READ);
rc = LPWSPEventSelect(s, hEventObject2, FD_WRITE);   //bad
```



To cancel the association and selection of network events on a socket, <i>lNetworkEvents</i> should be set to zero, in which case the <i>hEventObject</i> parameter will be ignored.

## -see-also

