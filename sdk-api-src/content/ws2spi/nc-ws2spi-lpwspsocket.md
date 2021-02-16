---
UID: NC:ws2spi.LPWSPSOCKET
title: LPWSPSOCKET (ws2spi.h)
description: The LPWSPSocket function creates a socket.
helpviewer_keywords: ["LPWSPSOCKET","WSPSocket","LPWSPSocket function [Winsock]","_win32_wspsocket_2","winsock.wspsocket_2","ws2spi/LPWSPSocket"]
old-location: winsock\wspsocket_2.htm
tech.root: WinSock
ms.assetid: 16735fd1-289d-425a-8ad2-c20d73888b1b
ms.date: 12/05/2018
ms.keywords: LPWSPSOCKET, WSPSocket, LPWSPSocket function [Winsock], _win32_wspsocket_2, winsock.wspsocket_2, ws2spi/LPWSPSocket
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPWSPSOCKET
 - ws2spi/LPWSPSOCKET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - LPWSPSocket
---

## -description

The **LPWSPSocket** function creates a socket. For info about the part played by **LPWSPSocket** in creating a shared socket, see [Shared sockets](/windows/win32/winsock/shared-sockets-2) and [Shared sockets in the SPI](/windows/win32/winsock/shared-sockets-in-the-spi-2).

## -parameters

### -param af [in]

Address family specification.

### -param type [in]

Type specification for the new socket.

### -param protocol [in]

Protocol to be used with the socket that is specific to the indicated address family.

### -param lpProtocolInfo [in]

Pointer to a 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure that defines the characteristics of the socket to be created.

### -param g [in]

Reserved.

### -param dwFlags

Socket attribute specification.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**LPWSPSocket** returns a descriptor referencing the new socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code is available in <i>lpErrno</i>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dl>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dl>
</dl>
</td>
<td width="60%">
The specified address family is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dl>
</dl>
</td>
<td width="60%">
Blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEMFILE</a></b></dl>
</dl>
</td>
<td width="60%">
No more socket descriptors are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTONOSUPPORT</a></b></dl>
</dl>
</td>
<td width="60%">
The specified protocol is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTOTYPE</a></b></dl>
</dl>
</td>
<td width="60%">
The specified protocol is the wrong type for this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAESOCKTNOSUPPORT</a></b></dl>
</dl>
</td>
<td width="60%">
The specified socket type is not supported in this address family.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dl>
</dl>
</td>
<td width="60%">
Parameter <i>g</i> specified is not valid.

</td>
</tr>
</table>

<div> </div>

## -remarks

The **LPWSPSocket** function causes a socket descriptor and any related resources to be allocated. By default, the created socket will not have the overlapped attribute. Windows Sockets providers are encouraged to be realized as Windows installable file systems, and supply system file handles as socket descriptors. These providers must call 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a> prior to returning from this function. For nonfile-system Windows Sockets providers, 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a> must be used to acquire a unique socket descriptor from the Ws2_32.dll prior to returning from this function. See  
<a href="/windows/desktop/WinSock/descriptor-allocation-2">Descriptor Allocation</a> for more information.

The values for <i>af</i>, <i>type</i>, and <i>protocol</i> are those supplied by the application in the corresponding API functions 
[socket](/windows/desktop/api/winsock2/nf-winsock2-socket) or 
[WSASocket](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa). A service provider is free to ignore or pay attention to any or all of these values as is appropriate for the particular protocol. However, the provider must be willing to accept the value of zero for <i>af</i> and <i>type</i>, since the Ws2_32.dll considers these to be wildcard values. Also the value of manifest constant **FROM_PROTOCOL_INFO** must be accepted for any of <i>af</i>, <i>type</i>, and <i>protocol</i>. This value indicates that the Windows Sockets 2 application needs to use the corresponding values from the 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure (**iAddressFamily**, **iSocketType**, **iProtocol**).

The <i>dwFlags</i> parameter can be used to specify the attributes of the socket by using the bitwise OR operator with any of the following flags.

|Flag|Meaning|
|-|-|
|WSA_FLAG_OVERLAPPED|This flag causes an overlapped socket to be created. Overlapped sockets can utilize [LPWSPSend](nc-ws2spi-lpwspsend.md), [LPWSPSendTo](nc-ws2spi-lpwspsendto.md), [LPWSPRecv](nc-ws2spi-lpwsprecv.md), [LPWSPRecvFrom](nc-ws2spi-lpwsprecvfrom.md), and [LPWSPIoctl](nc-ws2spi-lpwspioctl.md) for overlapped I/O operations, which allow multiple operations to be initiated and in process simultaneously. All functions that allow overlapped operations also support nonoverlapped usage on an overlapped socket if the values for parameters related to overlapped operation are null.|
|WSA_FLAG_MULTIPOINT_C_ROOT|Indicates that the socket created will be a c_root in a multipoint session. Only allowed if a rooted control plane is indicated in the protocol's <a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure.|
|WSA_FLAG_MULTIPOINT_C_LEAF|Indicates that the socket created will be a c_leaf in a multicast session. Only allowed if XP1_SUPPORT_MULTIPOINT is indicated in the protocol's <a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure.|
|WSA_FLAG_MULTIPOINT_D_ROOT|Indicates that the socket created will be a d_root in a multipoint session. Only allowed if a rooted data plane is indicated in the protocol's <a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure.|
|WSA_FLAG_MULTIPOINT_D_LEAF|Indicates that the socket created will be a d_leaf in a multipoint session. Only allowed if XP1_SUPPORT_MULTIPOINT is indicated in the protocol's <a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure.|

> [!NOTE]
> For multipoint sockets, exactly one WSA_FLAG_MULTIPOINT_C_ROOT or WSA_FLAG_MULTIPOINT_C_LEAF must be specified, and exactly one of WSA_FLAG_MULTIPOINT_D_ROOT or WSA_FLAG_MULTIPOINT_D_LEAF must be specified. Refer to <a href="/windows/desktop/WinSock/protocol-independent-multicast-and-multipoint-in-the-spi-2">Protocol-Independent Multicast and Multipoint in the SPI</a> for additional information.

Connection-oriented sockets such as SOCK_STREAM provide full-duplex connections, and must be in a connected state before any data can be sent or received on them. A connection to another socket is created with a 
[LPWSPConnect](nc-ws2spi-lpwspconnect.md) call. Once connected, data can be transferred using 
[LPWSPSend](nc-ws2spi-lpwspsend.md) and 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md) calls. When a session has been completed, a 
[LPWSPCloseSocket](nc-ws2spi-lpwspclosesocket.md) must be performed.

The communications protocols used to implement a reliable, connection-oriented socket ensure that data is not lost or duplicated. If data for which the peer protocol has buffer space cannot be successfully transmitted within a reasonable length of time, the connection is considered broken and subsequent calls will fail with the error code set to <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>.

Connectionless, message-oriented sockets allow sending and receiving of datagrams to and from arbitrary peers using 
[LPWSPSendTo](nc-ws2spi-lpwspsendto.md) and 
[LPWSPRecvFrom](nc-ws2spi-lpwsprecvfrom.md). If such a socket is connected by using 
[LPWSPConnect](nc-ws2spi-lpwspconnect.md) to a specific peer, datagrams can be sent to that peer using 
[LPWSPSend](nc-ws2spi-lpwspsend.md) and can be received from (only) this peer using 
[LPWSPRecv](nc-ws2spi-lpwsprecv.md).

Support for sockets with type **SOCK RAW** is not required but service providers are encouraged to support raw sockets whenever it makes sense to do so.

A layered service provider supplies an implementation of this function, but it is also a client of this function if and when it calls 
**LPWSPSocket** of the next layer in the protocol chain. Some special considerations apply to this function's <i>lpProtocolInfo</i> parameter as it is propagated down through the layers of the protocol chain.

If the next layer in the protocol chain is another layer then when the next layer's 
**LPWSPSocket** is called, this layer must pass to the next layer a <i>lpProtocolInfo</i> that references the same unmodified 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure with the same unmodified chain information. However, if the next layer is the base protocol (that is, the last element in the chain), this layer performs a substitution when calling the base provider's 
**LPWSPSocket**. In this case, the base provider's 
**WSAPROTOCOL_INFO** structure should be referenced by the <i>lpProtocolInfo</i> parameter.

One vital benefit of this policy is that base service providers do not have to be aware of protocol chains.

This same propagation policy applies when propagating a 
<a href="/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAProtocol_Info</a> structure through a layered sequence of other functions such as 
[LPWSPAddressToString](nc-ws2spi-lpwspaddresstostring.md), 
[LPWSPDuplicateSocket](nc-ws2spi-lpwspduplicatesocket.md), 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wspstartup">WSPStartup</a>, or 
[LPWSPStringToAddress](nc-ws2spi-lpwspstringtoaddress.md).

## -see-also

* <a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>
* [LPWSPAccept](nc-ws2spi-lpwspaccept.md)
* [LPWSPBind](nc-ws2spi-lpwspbind.md)
* [LPWSPConnect](nc-ws2spi-lpwspconnect.md)
* [LPWSPCloseSocket](nc-ws2spi-lpwspclosesocket.md)
* [LPWSPGetSockName](nc-ws2spi-lpwspgetsockname.md)
* [LPWSPGetSockOpt](nc-ws2spi-lpwspgetsockopt.md)
* [LPWSPIoctl](nc-ws2spi-lpwspioctl.md)
* [LPWSPListen](nc-ws2spi-lpwsplisten.md)
* [LPWSPRecv](nc-ws2spi-lpwsprecv.md)
* [LPWSPRecvFrom](nc-ws2spi-lpwsprecvfrom.md)
* [LPWSPSend](nc-ws2spi-lpwspsend.md)
* [LPWSPSendTo](nc-ws2spi-lpwspsendto.md)
* [LPWSPSetSockOpt](nc-ws2spi-lpwspsetsockopt.md)
* [LPWSPShutdown](nc-ws2spi-lpwspshutdown.md)

