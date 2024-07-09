---
UID: NC:ws2spi.LPWSPDUPLICATESOCKET
title: LPWSPDUPLICATESOCKET
description: The LPWSPDuplicateSocket function returns a WSAPROTOCOL_INFO structure that can be used to create a new socket descriptor for a shared socket.
tech.root: winsock
helpviewer_keywords: ["LPWSPDUPLICATESOCKET"]
ms.date: 9/12/2019
ms.keywords: LPWSPDUPLICATESOCKET
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
 - LPWSPDUPLICATESOCKET
f1_keywords:
 - LPWSPDUPLICATESOCKET
 - ws2spi/LPWSPDUPLICATESOCKET
---

## -description

The **LPWSPDuplicateSocket** function returns a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure that can be used to create a new socket descriptor for a shared socket.

## -parameters

### -param s [in]

Local socket descriptor.

### -param dwProcessId [in]

Identifier of the target process for which the shared socket will be used.

### -param lpProtocolInfo [out]

Pointer to a buffer allocated by the client that is large enough to contain a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure. The service provider copies the protocol information structure contents to this buffer.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, **LPWSPDuplicateSocket** returns zero. Otherwise, the value of SOCKET_ERROR is returned, and a specific error number is available in <i>lpErrno</i>.

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
Blocking Windows Sockets call is in progress or the service provider is still processing a callback function.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAEMFILE">WSAEMFILE</a></b></dl>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.  
</td>
</tr>

<tr>
<td width="40%">
<dl>                                              
<dt><b><a href="/windows/win32/winsock/windows-sockets-error-codes-2#WSAENOBUFS">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be created.  
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

A source process calls **LPWSPDuplicateSocket** to obtain a special <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure. It uses some interprocess communications (IPC) mechanism to pass the contents of this structure to a target process, which in turn uses it in a call to <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a></b> to obtain a descriptor for the duplicated socket. Note that the special **WSAPROTOCOL_INFO** structure can only be used once by the target process.

It is the service provider's responsibility to perform whatever operations are needed in the source process context and to create a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure that will be recognized when it subsequently appears as a parameter to <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a></b> in the target processes' context. The provider must then return a socket descriptor that references a common underlying socket. The **dwProviderReserved** member of the **WSAPROTOCOL_INFO** structure is available for the service provider's use and can be used to store any useful context information, including a duplicated handle.

When a new socket descriptor is allocated, an installable file system (IFS) provider must call [WPUModifyIFSHandle](./nf-ws2spi-wpumodifyifshandle.md), and a non-IFS provider must call [WPUCreateSocketHandle](./nf-ws2spi-wpucreatesockethandle.md). An IFS provider can use the [DuplicateHandle](../handleapi/nf-handleapi-duplicatehandle.md) function. To ensure proper execution of socket duplication, a non-IFS service provider must use the **LPWSPDuplicateSocket** function.

One possible scenario for establishing and using a shared socket in handoff mode is illustrated in the following.

<table>
<tr>
<th>Source process</th>
<th>IPC</th>
<th>Meaning</th>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>
1) <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspconnect">LPWSPConnect</a></b>
</dt>
</dl>
</td>
<td width="10%">
  
</td>
<td width="45%">
  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>
2) Requests target process identifier.
</dt>
</dl>
</td>
<td width="10%">
==&gt;
</td>
<td width="45%">
  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>

</dt>
</dl>
</td>
<td width="10%">

</td>
<td width="45%">
3) Receives process identifier request and respond.  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>
4) Receives process identifier.
</dt>
</dl>
</td>
<td width="10%">
&lt;==
</td>
<td width="45%">
  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>
5) Calls **LPWSPDuplicateSocket** to get a special <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure.
</dt>
</dl>
</td>
<td width="10%">

</td>
<td width="45%">
  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>
6) Sends <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure to target.
</dt>
</dl>
</td>
<td width="10%">

</td>
<td width="45%">
  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>

</dt>
</dl>
</td>
<td width="10%">
==&gt;
</td>
<td width="45%">
7) Receives <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure.  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>

</dt>
</dl>
</td>
<td width="10%">

</td>
<td width="45%">
8) Calls <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a></b> to create shared socket descriptor.  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>
  
</dt>
</dl>
</td>
<td width="10%">

</td>
<td width="45%">
9) Uses shared socket for data exchange.  
</td>
</tr>

<tr>
<td width="45%">
<dl>                                              
<dt>
 10) <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a></b>
</dt>
</dl>
</td>
<td width="10%">
&lt;==
</td>
<td width="45%">
  
</td>
</tr>
</table>

The descriptors that reference a shared socket can be used independently as far as I/O is concerned. However, the Windows Sockets interface does not implement any type of access control, so it is up to the processes involved to coordinate their operations on a shared socket. A typical use for shared sockets is to have one process that is responsible for creating sockets and establishing connections, hand off sockets to other processes that are responsible for information exchange.

Since what is duplicated are the socket descriptors and not the underlying socket, all the states associated with a socket are held in common across all the descriptors. For example a <b><a href="/previous-versions/windows/hardware/network/ff566318(v=vs.85)">WSPSetSockOpt</a></b> operation performed using one descriptor is subsequently visible using a <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspgetsockopt">LPWSPGetSockopt</a></b> from any or all descriptors. A process can call <a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspclosesocket">LPWSPCloseSocket</a> on a duplicated socket and the descriptor will become deallocated. The underlying socket, however, will remain open until **LPWSPClosesocket** is called by the last remaining descriptor.

Notification on shared sockets is subject to the usual constraints of **[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)** and <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspeventselect">LPWSPEventSelect</a></b>. Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration. Thus, for example, a shared socket cannot deliver FD_READ events to process A and FD_WRITE events to process B. For situations when such tight coordination is required, it is suggested that developers use threads instead of separate processes.

A layered service provider supplies an implementation of this function, but it is also a client of this function if and when it calls **LPWSPDuplicateSocket** of the next layer in the protocol chain. Some special considerations apply to this function's <i>lpProtocolInfo</i> parameter as it is propagated down through the layers of the protocol chain.

If the next layer in the protocol chain is another layer then when the next layer's **LPWSPDuplicateSocket** is called, this layer must pass to the next layer a <i>lpProtocolInfo</i> that references the same unmodified <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure with the same unmodified chain information. However, if the next layer is the base protocol (that is, the last element in the chain), this layer performs a substitution when calling the base provider's **LPWSPDuplicateSocket**. In this case, the base provider's **WSAPROTOCOL_INFO** structure should be referenced by the <i>lpProtocolInfo</i> parameter.

One vital benefit of this policy is that base service providers do not have to be aware of protocol chains. This same policy applies when propagating a <b><a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a></b> structure through a layered sequence of other functions such as <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspaddresstostring">LPWSPAddressToString</a></b>, <b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a></b>, <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsocket">LPWSPSocket</a></b>, or <b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspstringtoaddress">LPWSPStringToAddress</a></b>.

## -see-also

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>

<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a>