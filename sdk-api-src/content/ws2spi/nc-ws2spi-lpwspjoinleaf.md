---
UID: NC:ws2spi.LPWSPJOINLEAF
title: LPWSPJOINLEAF
author: windows-sdk-content
description: The WSPJoinLeaf function joins a leaf node into a multipoint session, exchanges connect data, and specifies needed quality of service based on the supplied flow specifications.
old-location: winsock\wspjoinleaf_2.htm
old-project: WinSock
ms.assetid: 3b0451e2-0e4c-4da7-b16c-37c242632bdd
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: LPWSPJOINLEAF, WSPJoinLeaf, WSPJoinLeaf function [Winsock], _win32_wspjoinleaf_2, winsock.wspjoinleaf_2, ws2spi/WSPJoinLeaf
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WSPJoinLeaf
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPWSPJOINLEAF callback function


## -description



			The 
<b>WSPJoinLeaf</b> function joins a leaf node into a multipoint session, exchanges connect data, and specifies needed quality of service based on the supplied flow specifications.


## -parameters




### -param s [in]

Descriptor identifying a multipoint socket.


### -param *name [in]

Name of the peer to which the socket in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure is to be joined.


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
<b>WSPJoinLeaf</b> returns a value of type <b>SOCKET</b> that is a descriptor for the newly created multipoint socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code is available in <i>lpErrno</i>.

On a blocking socket, the return value indicates success or failure of the join operation.

With a nonblocking socket, successful initiation of a join operation is indicated by a return value of a valid socket descriptor. Subsequently, an FD_CONNECT indication is given when the join operation completes, either successfully or otherwise. The error code associated with the FD_CONNECT indicates the success or failure of the 
<b>WSPJoinLeaf</b>.

Also, until the multipoint session join attempt completes all subsequent calls to 
<b>WSPJoinLeaf</b> on the same socket will fail with the error code 
<a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEALREADY</a>. After the 
<b>WSPJoinLeaf</b> completes successfully a subsequent attempt will usually fail with the error code 
<a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEISCONN</a>. An exception to the WSAEISCONN rule occurs for a c_root socket that allows root-initiated joins. In such a case another join may be initiated after a prior 
<b>WSPJoinLeaf</b> completes.

If the return error code indicates the multipoint session join attempt failed (that is, <a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a>, <a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a>, <a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a>) the Windows Sockets SPI client can call 
<b>WSPJoinLeaf</b> again for the same socket.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEADDRINUSE</a></b></dt>
</dl>
</td>
<td width="60%">
Socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs at the time of 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, but could be delayed until this function if the 
<b>bind</b> was to a partially wild-card address (involving ADDR_ANY) and if a specific address needs to be "committed" at the time of this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
(Blocking) call was canceled through 
<a href="https://msdn.microsoft.com/9219c733-43af-414b-8a38-78da52757bd1">WSPCancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
Blocking Windows Sockets call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonblocking 
<a href="https://msdn.microsoft.com/3b0451e2-0e4c-4da7-b16c-37c242632bdd">WSPJoinLeaf</a> call is in progress on the specified socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
Remote address is not a valid address (for example, ADDR_ANY).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAECONNREFUSED</a></b></dt>
</dl>
</td>
<td width="60%">
The attempt to join was forcefully rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, the <i>namelen</i> parameter is too small, the buffer length for <i>lpCalleeData</i>, <i>lpSQOS</i>, and <i>lpGQOS</i> are too small, or the buffer length for <i>lpCallerData</i> is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
Socket is already member of the multipoint session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAENETUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be joined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
Flow specifications specified in <i>lpSQOS</i> cannot be satisfied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEPROTONOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpCallerData</i> augment is not supported by the service provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAETIMEDOUT</a></b></dt>
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

<b>WSPJoinLeaf</b> has the same parameters and semantics as 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566275">WSPConnect</a> except that it returns a socket descriptor (as in 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566266">WSPAccept</a>), and it has an additional <i>dwFlags</i> parameter. Only multipoint sockets created using 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566319">WSPSocket</a> with appropriate multipoint flags set can be used for input parameter <i>s</i> in this function. If the socket is in the nonblocking mode, the returned socket descriptor will not be usable until after a corresponding FD_CONNECT indication on the original socket <i>s</i> has been received, except that 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> can be invoked on this new socket descriptor to cancel a pending join operation. A root node in a multipoint session can call 
<b>WSPJoinLeaf</b> one or more times in order to add a number of leaf nodes, however at most one multipoint connection request can be outstanding at a time. Refer to 
<a href="https://msdn.microsoft.com/861f457c-fe7e-4128-a3f3-786424a96ea5">Protocol-Independent Multicast and Multipoint in the SPI</a> for additional information.

For nonblocking sockets it is often not possible to complete the connection immediately. In such a case, this function returns an as-yet unusable socket descriptor and the operation proceeds. There is no error code such as <a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSAEWOULDBLOCK</a> in this case, since the function has effectively returned a "successful start" indication. When the final outcome success or failure becomes known, it may be reported through 
<a href="https://msdn.microsoft.com/a96e0c2f-8bd0-4fcf-b7bd-67b3f7f53005">WSPAsyncSelect</a> or 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566287">WSPEventSelect</a> depending on how the client registers for notification on the original socket <i>s</i>. In either case, the notification is announced with FD_CONNECT and the error code associated with the FD_CONNECT indicates either success or a specific reason for failure. Note that 
<a href="https://msdn.microsoft.com/a8f2922d-2474-406d-b1c7-631f05ccdd9c">WSPSelect</a> cannot be used to detect completion notification for 
<b>WSPJoinLeaf</b>.

The socket descriptor returned by 
<b>WSPJoinLeaf</b> is different depending on whether the input socket descriptor, <i>s</i>, is a c_root or a c_leaf. When used with a c_root socket, the <i>name</i> parameter designates a particular leaf node to be added and the returned socket descriptor is a c_leaf socket corresponding to the newly added leaf node. (As is described in section 
<a href="https://msdn.microsoft.com/ed5e10f4-fa17-4a07-9cac-43767915b8e9">Descriptor Allocation</a>, when new socket descriptors are allocated IFS providers must call 
<a href="https://msdn.microsoft.com/f58971eb-0948-4e16-a767-1d4cba9ec721">WPUModifyIFSHandle</a> and non-IFS providers must call 
<a href="https://msdn.microsoft.com/ecbf9d8b-b705-4160-ac77-afa5b1501534">WPUCreateSocketHandle</a>). The newly created socket has the same properties as <i>s</i> including asynchronous events registered with 
<a href="https://msdn.microsoft.com/a96e0c2f-8bd0-4fcf-b7bd-67b3f7f53005">WSPAsyncSelect</a> or with 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566287">WSPEventSelect</a>. It is not intended to be used for exchange of multipoint data, but rather is used to receive network event indications (for example, FD_CLOSE) for the connection that exists to the particular c_leaf. Some multipoint implementations can also allow this socket to be used for "side chats" between the root and an individual leaf node. An FD_CLOSE indication will be received for this socket if the corresponding leaf node calls 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566273">WSPCloseSocket</a> to drop out of the multipoint session. Symmetrically, invoking 
<b>WSPCloseSocket</b> on the c_leaf socket returned from 
<b>WSPJoinLeaf</b> will cause the socket in the corresponding leaf node to get FD_CLOSE notification.

When 
<b>WSPJoinLeaf</b> is invoked with a c_leaf socket, the <i>name</i> parameter contains the address of the root node (for a rooted control scheme) or an existing multipoint session (nonrooted control scheme), and the returned socket descriptor is the same as the input socket descriptor. In other words, a new socket descriptor is not allocated. In a rooted control scheme, the root application would put its c_root socket in the listening mode by calling 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566297">WSPListen</a>. The standard FD_ACCEPT notification will be delivered when the leaf node requests to join itself to the multipoint session. The root application uses the usual 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566266">WSPAccept</a> functions to admit the new leaf node. The value returned from 
<b>WSPAccept</b> is also a c_leaf socket descriptor just like those returned from 
<b>WSPJoinLeaf</b>. To accommodate multipoint schemes that allow both root-initiated and leaf-initiated joins, it is acceptable for a c_root socket that is already in listening mode to be used as an input to 
<b>WSPJoinLeaf</b>.

The Windows Sockets SPI client is responsible for allocating any memory space pointed to directly or indirectly by any of the parameters it specifies.

The <i>lpCallerData</i> is a value parameter that contains any user data that is to be sent along with the multipoint session join request. If <i>lpCallerData</i> is <b>NULL</b>, no user data will be passed to the peer. The <i>lpCalleeData</i> is a result parameter that will contain any user data passed back from the peer as part of the multipoint session establishment. <i>lpCalleeData</i>-&gt;<b>len</b> initially contains the length of the buffer allocated by the Windows Sockets SPI client and pointed to by <i>lpCalleeData</i>-&gt;<b>buf</b>. <i>lpCalleeData</i>-&gt;<b>len</b> will be set to zero if no user data has been passed back. The <i>lpCalleeData</i> information will be valid when the multipoint join operation is complete. For blocking sockets, this will be when the 
<b>WSPJoinLeaf</b> function returns. For nonblocking sockets, this will be after the FD_CONNECT notification has occurred on the original socket <i>s</i>. If <i>lpCalleeData</i> is <b>NULL</b>, no user data will be passed back. The exact format of the user data is specific to the address family to which the socket belongs and/or the applications involved.

At multipoint session establishment time, a Windows Sockets SPI client can use the <i>lpSQOS</i> parameters to override any previous QoS specification made for the socket through 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566296">WSPIoctl</a> with the SIO_SET_QOS opcode.

<i>lpSQOS</i> specifies the flow specifications for socket <i>s</i>, one for each direction, followed by any additional provider-specific parameters. If either the associated transport provider in general or the specific type of socket in particular cannot honor the QoS request, an error will be returned as indicated below. The sending or receiving flow specification values will be ignored, respectively, for any unidirectional sockets. If no provider-specific parameters are supplied, the <b>buf</b> and <b>len</b> members of <i>lpSQOS</i>-&gt;<b>ProviderSpecific</b> should be set to <b>NULL</b> and zero, respectively. A <b>NULL</b> value for <i>lpSQOS</i> indicates no application supplied quality of service.

The <i>dwFlags</i> parameter is used to indicate whether the socket will be acting only as a sender (JL_SENDER_ONLY), only as a receiver (JL_RECEIVER_ONLY), or both (JL_BOTH).

<div class="alert"><b>Note</b>  When connected sockets break (that is, become closed for whatever reason), they should be discarded and recreated. It is safest to assume that when things go awry for any reason on a connected socket, the Windows Sockets SPI client must discard and recreate the needed sockets in order to return to a stable point.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff566266">WSPAccept</a>



<a href="https://msdn.microsoft.com/a96e0c2f-8bd0-4fcf-b7bd-67b3f7f53005">WSPAsyncSelect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566268">WSPBind</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566287">WSPEventSelect</a>



<a href="https://msdn.microsoft.com/a8f2922d-2474-406d-b1c7-631f05ccdd9c">WSPSelect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566319">WSPSocket</a>
 

 

