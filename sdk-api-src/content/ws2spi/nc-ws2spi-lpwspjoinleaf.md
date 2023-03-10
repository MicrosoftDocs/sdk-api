---
UID: NC:ws2spi.LPWSPJOINLEAF
title: LPWSPJOINLEAF (ws2spi.h)
description: The LPWSPJoinLeaf function joins a leaf node into a multipoint session, exchanges connect data, and specifies needed quality of service based on the supplied flow specifications.
helpviewer_keywords: ["LPWSPJOINLEAF","WSPJoinLeaf","WSPJoinLeaf function [Winsock]","_win32_wspjoinleaf_2","winsock.wspjoinleaf_2","ws2spi/WSPJoinLeaf"]
old-location: winsock\wspjoinleaf_2.htm
tech.root: WinSock
ms.assetid: 3b0451e2-0e4c-4da7-b16c-37c242632bdd
ms.date: 12/05/2018
ms.keywords: LPWSPJOINLEAF, WSPJoinLeaf, WSPJoinLeaf function [Winsock], _win32_wspjoinleaf_2, winsock.wspjoinleaf_2, ws2spi/WSPJoinLeaf
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
 - LPWSPJOINLEAF
 - ws2spi/LPWSPJOINLEAF
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
 - WSPJoinLeaf
---

# LPWSPJOINLEAF callback function


## -description

The **WSPJoinLeaf** function joins a leaf node into a multipoint session, exchanges connect data, and specifies needed quality of service based on the supplied flow specifications.

## -parameters

### -param s [in]

Descriptor identifying a multipoint socket.

### -param name [in]

Name of the peer to which the socket in the 
<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure is to be joined.

### -param namelen [in]

Length of the <i>name</i>, in bytes.

### -param lpCallerData [in]

Pointer to the user data that is to be transferred to the peer during multipoint session establishment.

### -param lpCalleeData [out]

Pointer to the user data that is to be transferred back from the peer during multipoint session establishment.

### -param lpSQOS [in]

Pointer to the flow specifications for socket <i>s</i>, one for each direction.

### -param lpGQOS [in]

Reserved.

### -param dwFlags [in]

Flags to indicate that the socket is acting as a sender, receiver, or both.

### -param lpErrno [out]

Pointer to the error code.

## -returns

If no error occurs, 
**WSPJoinLeaf** returns a value of type **SOCKET** that is a descriptor for the newly created multipoint socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code is available in <i>lpErrno</i>.

On a blocking socket, the return value indicates success or failure of the join operation.

With a nonblocking socket, successful initiation of a join operation is indicated by a return value of a valid socket descriptor. Subsequently, an FD_CONNECT indication is given when the join operation completes, either successfully or otherwise. The error code associated with the FD_CONNECT indicates the success or failure of the 
**WSPJoinLeaf**.

Also, until the multipoint session join attempt completes all subsequent calls to 
**WSPJoinLeaf** on the same socket will fail with the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a>. After the 
**WSPJoinLeaf** completes successfully a subsequent attempt will usually fail with the error code 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a>. An exception to the WSAEISCONN rule occurs for a c_root socket that allows root-initiated joins. In such a case another join may be initiated after a prior 
**WSPJoinLeaf** completes.

If the return error code indicates the multipoint session join attempt failed (that is, <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a>, <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a>, <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>) the Windows Sockets SPI client can call 
**WSPJoinLeaf** again for the same socket.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRINUSE</a></b></dl>
</dl>
</td>
<td width="60%">
Socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs at the time of 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, but could be delayed until this function if the 
**bind** was to a partially wild-card address (involving ADDR_ANY) and if a specific address needs to be "committed" at the time of this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dl>
</dl>
</td>
<td width="60%">
(Blocking) call was canceled through 
<a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspcancelblockingcall">WSPCancelBlockingCall</a>.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEALREADY</a></b></dl>
</dl>
</td>
<td width="60%">
Nonblocking 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpwspjoinleaf">WSPJoinLeaf</a> call is in progress on the specified socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a></b></dl>
</dl>
</td>
<td width="60%">
Remote address is not a valid address (for example, ADDR_ANY).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dl>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a></b></dl>
</dl>
</td>
<td width="60%">
The attempt to join was forcefully rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, the <i>namelen</i> parameter is too small, the buffer length for <i>lpCalleeData</i>, <i>lpSQOS</i>, and <i>lpGQOS</i> are too small, or the buffer length for <i>lpCallerData</i> is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dl>
</dl>
</td>
<td width="60%">
Socket is already member of the multipoint session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></b></dl>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dl>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be joined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dl>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></b></dl>
</dl>
</td>
<td width="60%">
Flow specifications specified in <i>lpSQOS</i> cannot be satisfied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEPROTONOSUPPORT</a></b></dl>
</dl>
</td>
<td width="60%">
The <i>lpCallerData</i> augment is not supported by the service provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></b></dl>
</dl>
</td>
<td width="60%">
An attempt to join timed out without establishing a multipoint session.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

This function is used to join a leaf node to a multipoint session, and to perform a number of other ancillary operations that occur at session join time as well. If the socket, <i>s</i>, is unbound, unique values are assigned to the local association by the system, and the socket is marked as bound.

**WSPJoinLeaf** has the same parameters and semantics as 
[LPWSPConnect](nc-ws2spi-lpwspconnect.md) except that it returns a socket descriptor (as in 
[LPWSPAccept](nc-ws2spi-lpwspaccept.md)), and it has an additional <i>dwFlags</i> parameter. Only multipoint sockets created using 
[LPWSPSocket](nc-ws2spi-lpwspsocket.md) with appropriate multipoint flags set can be used for input parameter <i>s</i> in this function. If the socket is in the nonblocking mode, the returned socket descriptor will not be usable until after a corresponding FD_CONNECT indication on the original socket <i>s</i> has been received, except that 
<a href="/windows/desktop/api/winsock/nf-winsock-closesocket">closesocket</a> can be invoked on this new socket descriptor to cancel a pending join operation. A root node in a multipoint session can call 
**WSPJoinLeaf** one or more times in order to add a number of leaf nodes, however at most one multipoint connection request can be outstanding at a time. Refer to 
<a href="/windows/desktop/WinSock/protocol-independent-multicast-and-multipoint-in-the-spi-2">Protocol-Independent Multicast and Multipoint in the SPI</a> for additional information.

For nonblocking sockets it is often not possible to complete the connection immediately. In such a case, this function returns an as-yet unusable socket descriptor and the operation proceeds. There is no error code such as <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a> in this case, since the function has effectively returned a "successful start" indication. When the final outcome success or failure becomes known, it may be reported through 
[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md) or 
[LPWSPEventSelect](nc-ws2spi-lpwspeventselect.md) depending on how the client registers for notification on the original socket <i>s</i>. In either case, the notification is announced with FD_CONNECT and the error code associated with the FD_CONNECT indicates either success or a specific reason for failure. Note that 
[LPWSPSelect](nc-ws2spi-lpwspselect.md) cannot be used to detect completion notification for 
**WSPJoinLeaf**.

The socket descriptor returned by 
**WSPJoinLeaf** is different depending on whether the input socket descriptor, <i>s</i>, is a c_root or a c_leaf. When used with a c_root socket, the <i>name</i> parameter designates a particular leaf node to be added and the returned socket descriptor is a c_leaf socket corresponding to the newly added leaf node. (As is described in section 
<a href="/windows/desktop/WinSock/descriptor-allocation-2">Descriptor Allocation</a>, when new socket descriptors are allocated IFS providers must call 
<a href="/windows/desktop/api/ws2spi/nf-ws2spi-wpumodifyifshandle">WPUModifyIFSHandle</a> and non-IFS providers must call 
<a href="/windows/win32/api/ws2spi/nf-ws2spi-wpucreatesockethandle">WPUCreateSocketHandle</a>). The newly created socket has the same properties as <i>s</i> including asynchronous events registered with 
[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md) or with 
[LPWSPEventSelect](nc-ws2spi-lpwspeventselect.md). It is not intended to be used for exchange of multipoint data, but rather is used to receive network event indications (for example, FD_CLOSE) for the connection that exists to the particular c_leaf. Some multipoint implementations can also allow this socket to be used for "side chats" between the root and an individual leaf node. An FD_CLOSE indication will be received for this socket if the corresponding leaf node calls 
[LPWSPCloseSocket](nc-ws2spi-lpwspclosesocket.md) to drop out of the multipoint session. Symmetrically, invoking 
**WSPCloseSocket** on the c_leaf socket returned from 
**WSPJoinLeaf** will cause the socket in the corresponding leaf node to get FD_CLOSE notification.

When 
**WSPJoinLeaf** is invoked with a c_leaf socket, the <i>name</i> parameter contains the address of the root node (for a rooted control scheme) or an existing multipoint session (nonrooted control scheme), and the returned socket descriptor is the same as the input socket descriptor. In other words, a new socket descriptor is not allocated. In a rooted control scheme, the root application would put its c_root socket in the listening mode by calling 
[LPWSPListen](nc-ws2spi-lpwsplisten.md). The standard FD_ACCEPT notification will be delivered when the leaf node requests to join itself to the multipoint session. The root application uses the usual 
[LPWSPAccept](nc-ws2spi-lpwspaccept.md) functions to admit the new leaf node. The value returned from 
**WSPAccept** is also a c_leaf socket descriptor just like those returned from 
**WSPJoinLeaf**. To accommodate multipoint schemes that allow both root-initiated and leaf-initiated joins, it is acceptable for a c_root socket that is already in listening mode to be used as an input to 
**WSPJoinLeaf**.

The Windows Sockets SPI client is responsible for allocating any memory space pointed to directly or indirectly by any of the parameters it specifies.

The <i>lpCallerData</i> is a value parameter that contains any user data that is to be sent along with the multipoint session join request. If <i>lpCallerData</i> is **NULL**, no user data will be passed to the peer. The <i>lpCalleeData</i> is a result parameter that will contain any user data passed back from the peer as part of the multipoint session establishment. <i>lpCalleeData</i>-&gt;**len** initially contains the length of the buffer allocated by the Windows Sockets SPI client and pointed to by <i>lpCalleeData</i>-&gt;**buf**. <i>lpCalleeData</i>-&gt;**len** will be set to zero if no user data has been passed back. The <i>lpCalleeData</i> information will be valid when the multipoint join operation is complete. For blocking sockets, this will be when the 
**WSPJoinLeaf** function returns. For nonblocking sockets, this will be after the FD_CONNECT notification has occurred on the original socket <i>s</i>. If <i>lpCalleeData</i> is **NULL**, no user data will be passed back. The exact format of the user data is specific to the address family to which the socket belongs and/or the applications involved.

At multipoint session establishment time, a Windows Sockets SPI client can use the <i>lpSQOS</i> parameters to override any previous QoS specification made for the socket through 
[LPWSPIoctl](nc-ws2spi-lpwspioctl.md) with the SIO_SET_QOS opcode.

<i>lpSQOS</i> specifies the flow specifications for socket <i>s</i>, one for each direction, followed by any additional provider-specific parameters. If either the associated transport provider in general or the specific type of socket in particular cannot honor the QoS request, an error will be returned as indicated below. The sending or receiving flow specification values will be ignored, respectively, for any unidirectional sockets. If no provider-specific parameters are supplied, the **buf** and **len** members of <i>lpSQOS</i>-&gt;**ProviderSpecific** should be set to **NULL** and zero, respectively. A **NULL** value for <i>lpSQOS</i> indicates no application supplied quality of service.

The <i>dwFlags</i> parameter is used to indicate whether the socket will be acting only as a sender (JL_SENDER_ONLY), only as a receiver (JL_RECEIVER_ONLY), or both (JL_BOTH).

<div class="alert">**Note**  When connected sockets break (that is, become closed for whatever reason), they should be discarded and recreated. It is safest to assume that when things go awry for any reason on a connected socket, the Windows Sockets SPI client must discard and recreate the needed sockets in order to return to a stable point.</div>
<div> </div>

## -see-also

[LPWSPAccept](nc-ws2spi-lpwspaccept.md)



[LPWSPAsyncSelect](nc-ws2spi-lpwspasyncselect.md)



[LPWSPBind](nc-ws2spi-lpwspbind.md)



[LPWSPEventSelect](nc-ws2spi-lpwspeventselect.md)



[LPWSPSelect](nc-ws2spi-lpwspselect.md)



[LPWSPSocket](nc-ws2spi-lpwspsocket.md)

