---
UID: NF:winsock2.WSAJoinLeaf
title: WSAJoinLeaf function
author: windows-sdk-content
description: The WSAJoinLeaf function joins a leaf node into a multipoint session, exchanges connect data, and specifies needed quality of service based on the specified FLOWSPEC structures.
old-location: winsock\wsajoinleaf_2.htm
old-project: winsock
ms.assetid: ef9efa03-feed-4f0d-b874-c646cce745c9
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: WSAJoinLeaf, WSAJoinLeaf function [Winsock], _win32_wsajoinleaf_2, winsock.wsajoinleaf_2, winsock2/WSAJoinLeaf
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.typenames: WSAECOMPARATOR, *PWSAECOMPARATOR, *LPWSAECOMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAJoinLeaf
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAJoinLeaf function


## -description


The 
<b>WSAJoinLeaf</b> function joins a leaf node into a multipoint session, exchanges connect data, and specifies needed quality of service based on the specified 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures.


## -parameters




### -param s [in]

Descriptor identifying a multipoint socket.


### -param name [in]

Name of the peer to which the socket is to be joined.


### -param namelen [in]

Length of <i>name</i>, in bytes.


### -param lpCallerData [in]

Pointer to the user data that is to be transferred to the peer during multipoint session establishment.


### -param lpCalleeData [out]

Pointer to the user data that is to be transferred back from the peer during multipoint session establishment.


### -param lpSQOS [in]

Pointer to the 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for socket <i>s</i>, one for each direction.


### -param lpGQOS [in]

Reserved for future use with socket groups. A pointer to the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for the socket group (if applicable).


### -param dwFlags [in]

Flags to indicate that the socket is acting as a sender (JL_SENDER_ONLY), receiver (JL_RECEIVER_ONLY), or both (JL_BOTH).


## -returns



If no error occurs, 
<b>WSAJoinLeaf</b> returns a value of type SOCKET that is a descriptor for the newly created multipoint socket. Otherwise, a value of INVALID_SOCKET is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

On a blocking socket, the return value indicates success or failure of the join operation.

With a nonblocking socket, successful initiation of a join operation is indicated by a return of a valid socket descriptor. Subsequently, an FD_CONNECT indication will be given on the original socket <i>s</i> when the join operation completes, either successfully or otherwise. The application must use either 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> or 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> with interest registered for the FD_CONNECT event in order to determine when the join operation has completed and checks the associated error code to determine the success or failure of the operation. The 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> function cannot be used to determine when the join operation completes.

Also, until the multipoint session join attempt completes all subsequent calls to 
<b>WSAJoinLeaf</b> on the same socket will fail with the error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEALREADY</a>. After the 
<b>WSAJoinLeaf</b> operation completes successfully, a subsequent attempt will usually fail with the error code 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEISCONN</a>. An exception to the WSAEISCONN rule occurs for a c_root socket that allows root-initiated joins. In such a case, another join may be initiated after a prior 
<b>WSAJoinLeaf</b> operation completes.

If the return error code indicates the multipoint session join attempt failed (that is, 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNREFUSED</a>, 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETUNREACH</a>, 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a>) the application can call 
<b>WSAJoinLeaf</b> again for the same socket.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEADDRINUSE</a></b></dt>
</dl>
</td>
<td width="60%">
The socket's local address is already in use and the socket was not marked to allow address reuse with SO_REUSEADDR. This error usually occurs at the time of 
<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>, but could be delayed until this function if the 
<b>bind</b> was to a partially wildcard address (involving ADDR_ANY) and if a specific address needs to be committed at the time of this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEADDRNOTAVAIL</a></b></dt>
</dl>
</td>
<td width="60%">
The remote address is not a valid address (such as ADDR_ANY).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEAFNOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
Addresses in the specified family cannot be used with this socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEALREADY</a></b></dt>
</dl>
</td>
<td width="60%">
A nonblocking 
<a href="https://msdn.microsoft.com/ef9efa03-feed-4f0d-b874-c646cce745c9">WSAJoinLeaf</a> call is in progress on the specified socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNREFUSED</a></b></dt>
</dl>
</td>
<td width="60%">
The attempt to join was forcefully rejected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, the <i>namelen</i> parameter is too small, the buffer length for <i>lpCalleeData</i>, <i>lpSQOS</i>, and <i>lpGQOS</i> are too small, or the buffer length for <i>lpCallerData</i> is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
A 
<a href="https://msdn.microsoft.com/ef9efa03-feed-4f0d-b874-c646cce745c9">WSAJoinLeaf</a> function call was performed on a UDP socket that was opened without setting its WSA_FLAG_MULTIPOINT_C_LEAF or WSA_FLAG_MULTIPOINT_D_LEAF multipoint flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEISCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is already a member of the multipoint session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Socket 1.1 call was canceled through 
<a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETUNREACH</a></b></dt>
</dl>
</td>
<td width="60%">
The network cannot be reached from this host at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
No buffer space is available. The socket cannot be joined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures specified in <i>lpSQOS</i> and <i>lpGQOS</i> cannot be satisfied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEPROTONOSUPPORT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>lpCallerData</i> augment is not supported by the service provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAETIMEDOUT</a></b></dt>
</dl>
</td>
<td width="60%">
The attempt to join timed out without establishing a multipoint session.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAJoinLeaf</b> function is used to join a leaf node to a multipoint session, and to perform a number of other ancillary operations that occur at session join time as well. If the socket <i>s</i> is unbound, unique values are assigned to the local association by the system, and the socket is marked as bound.

The 
<b>WSAJoinLeaf</b> function has the same parameters and semantics as 
<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a> except that it returns a socket descriptor (as in 
<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>), and it has an additional <i>dwFlags</i> parameter. Only multipoint sockets created using 
<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a> with appropriate multipoint flags set can be used for input parameter <i>s</i> in this function. The returned socket descriptor will not be usable until after the join operation completes. For example, if the socket is in nonblocking mode after a corresponding FD_CONNECT indication has been received from 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> or 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> on the original socket <i>s</i>, except that 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> may be invoked on this new socket descriptor to cancel a pending join operation. A root application in a multipoint session may call 
<b>WSAJoinLeaf</b> one or more times in order to add a number of leaf nodes, however at most one multipoint connection request may be outstanding at a time. Refer to 
<a href="https://msdn.microsoft.com/7e9c55dc-8b19-4730-ad76-ed83db0b7b64">Multipoint and Multicast Semantics</a> for additional information.

For nonblocking sockets it is often not possible to complete the connection immediately. In such a case, this function returns an as-yet unusable socket descriptor and the operation proceeds. There is no error code such as 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a> in this case, since the function has effectively returned a successful start indication. When the final outcome success or failure becomes known, it may be reported through 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> or 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> depending on how the client registers for notification on the original socket <i>s</i>. In either case, the notification is announced with FD_CONNECT and the error code associated with the FD_CONNECT indicates either success or a specific reason for failure. The 
<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a> function cannot be used to detect completion notification for 
<b>WSAJoinLeaf</b>.

The socket descriptor returned by 
<b>WSAJoinLeaf</b> is different depending on whether the input socket descriptor, <i>s</i>, is a c_root or a c_leaf. When used with a c_root socket, the <i>name</i> parameter designates a particular leaf node to be added and the returned socket descriptor is a c_leaf socket corresponding to the newly added leaf node. The newly created socket has the same properties as <i>s</i>, including asynchronous events registered with 
<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a> or with 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>. It is not intended to be used for exchange of multipoint data, but rather is used to receive network event indications (for example, FD_CLOSE) for the connection that exists to the particular c_leaf. Some multipoint implementations can also allow this socket to be used for side chats between the root and an individual leaf node. An FD_CLOSE indication will be received for this socket if the corresponding leaf node calls 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> to drop out of the multipoint session. Symmetrically, invoking 
<b>closesocket</b> on the c_leaf socket returned from 
<b>WSAJoinLeaf</b> will cause the socket in the corresponding leaf node to get an FD_CLOSE notification.

When 
<b>WSAJoinLeaf</b> is invoked with a c_leaf socket, the <i>name</i> parameter contains the address of the root application (for a rooted control scheme) or an existing multipoint session (nonrooted control scheme), and the returned socket descriptor is the same as the input socket descriptor. In other words, a new socket descriptor is not allocated. In a rooted control scheme, the root application would put its c_root socket in listening mode by calling 
<a href="https://msdn.microsoft.com/1233feeb-a8c1-49ac-ab34-82af224ecf00">listen</a>. The standard FD_ACCEPT notification will be delivered when the leaf node requests to join itself to the multipoint session. The root application uses the usual 
<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a> or 
				<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a> functions to admit the new leaf node. The value returned from either 
<b>accept</b> or 
<b>WSAAccept</b> is also a c_leaf socket descriptor just like those returned from 
<b>WSAJoinLeaf</b>. To accommodate multipoint schemes that allow both root-initiated and leaf-initiated joins, it is acceptable for a c_root socket that is already in listening mode to be used as an input to 
<b>WSAJoinLeaf</b>.

The application is responsible for allocating any memory space pointed to directly or indirectly by any of the parameters it specifies.

The <i>lpCallerData</i> is a value parameter that contains any user data that is to be sent along with the multipoint session join request. If <i>lpCallerData</i> is <b>NULL</b>, no user data will be passed to the peer. The <i>lpCalleeData</i> is a result parameter that will contain any user data passed back from the peer as part of the multipoint session establishment. The <b>len</b> member of the <a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structure pointed to by the <i>lpCalleeData</i> parameter initially contains the length of the buffer allocated by the application and pointed to by the <b>buf</b> member of the <b>WSABUF</b> structure. The <b>len</b> member of the <b>WSABUF</b> structure pointed to by the <i>lpCalleeData</i> parameter will be set to zero if no user data has been passed back. The <i>lpCalleeData</i> information will be valid when the multipoint join operation is complete.

For blocking sockets, this will be when the 
<b>WSAJoinLeaf</b> function returns. For nonblocking sockets, this will be after the join operation has completed. For example, this could occur after FD_CONNECT notification on the original socket <i>s</i>). If <i>lpCalleeData</i> is <b>NULL</b>, no user data will be passed back. The exact format of the user data is specific to the address family to which the socket belongs.

At multipoint session establishment time, an application can use the <i>lpSQOS</i> and/or <i>lpGQOS</i> parameters to override any previous quality of service specification made for the socket through 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> with the SIO_SET_QOS or  SIO_SET_GROUP_QOS opcodes.

The <i>lpSQOS</i> parameter specifies the 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for socket <i>s</i>, one for each direction, followed by any additional provider-specific parameters. If either the associated transport provider in general or the specific type of socket in particular cannot honor the quality of service request, an error will be returned as indicated in the following. The respective sending or receiving flow specification values will be ignored for any unidirectional sockets. If no provider-specific parameters are specified, the <b>buf</b> and <b>len</b> members of the <a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structure pointed to by the <i>lpCalleeData</i> parameter should be set to <b>NULL</b> and zero, respectively. A <b>NULL</b> value for <i>lpSQOS</i> indicates no application-supplied quality of service.

Reserved for future socket groups. The <i>lpGQOS</i> parameter specifies the 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structures for the socket group (if applicable), one for each direction, followed by any additional provider-specific parameters. If no provider-specific parameters are specified, the the <b>buf</b> and <b>len</b> members of the <a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a> structure pointed to by the <i>lpCalleeData</i> parameter should be set to should be set to <b>NULL</b> and zero, respectively. A <b>NULL</b> value for <i>lpGQOS</i> indicates no application-supplied group quality of service. This parameter will be ignored if <i>s</i> is not the creator of the socket group.

When connected sockets break (that is, become closed for whatever reason), they should be discarded and recreated. It is safest to assume that when things go awry for any reason on a connected socket, the application must discard and recreate the needed sockets in order to return to a stable point.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSAJoinLeaf</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>



<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/a012c3ba-67fd-4fcf-84d1-85e9d495c29c">WSABUF</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/dcf2e543-de54-43d9-9e45-4cb935da3548">WSASocket</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/f9f1092d-7e15-41cd-a42f-abe8a4f33e15">select</a>
 

 

