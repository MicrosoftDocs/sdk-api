---
UID: NF:winsock2.closesocket
title: closesocket function
author: windows-sdk-content
description: The closesocket function closes an existing socket.
old-location: winsock\closesocket_2.htm
tech.root: winsock
ms.assetid: 2f357aa8-389b-4c92-8a9f-289e048cc41c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_closesocket_2, closesocket, closesocket function [Winsock], winsock.closesocket_2, winsock/closesocket"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsock2.h
req.include-header: Winsock2.h
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - closesocket
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- closesocket
: 
---

# closesocket function


## -description


The 
<b>closesocket</b> function closes an existing socket.


## -parameters




### -param s [in]

A descriptor identifying the socket to close.


## -returns



If no error occurs, 
<b>closesocket</b> returns zero. Otherwise, a value of <b>SOCKET_ERROR</b> is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
The (blocking) Windows Socket 1.1 call was canceled through 
<a href="https://msdn.microsoft.com/b3597d29-51a5-410f-9925-4d678dd641c1">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is marked as nonblocking, but the 
 <b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure is set to nonzero and the <b>l_linger</b> member of the <b>linger</b> structure is set to a nonzero timeout value.

</td>
</tr>
</table>
 




## -remarks



The <b>closesocket</b> function closes a socket. Use it to release the socket descriptor passed in the <i>s</i> parameter. Note that the socket descriptor passed in the <i>s</i>  parameter may immediately be reused by the system as soon as <b>closesocket</b> function is issued. As a result, it is not reliable to expect further references to the socket descriptor passed in the <i>s</i> parameter to fail with the error <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a>. A Winsock client must never issue <b>closesocket</b> on <i>s</i> concurrently with another Winsock function call.

Any pending overlapped send and receive operations (
<a href="https://msdn.microsoft.com/764339e6-a1ac-455d-8ebd-ad0fa50dc3b0">WSASend</a>/
<a href="https://msdn.microsoft.com/e3a11522-871c-4d6b-a2e6-ca91ffc2b698">WSASendTo</a>/
<a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a>/
<a href="https://msdn.microsoft.com/8617dbb8-0e4e-4cd3-9597-5d20de6778f6">WSARecvFrom</a> with an overlapped socket) issued by any thread in this process are also canceled. Any event, completion routine, or completion port action specified for these overlapped operations is performed. The pending overlapped operations fail with the error status 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_OPERATION_ABORTED</a>.

An application should not assume that any outstanding I/O operations on a socket will all be guaranteed to completed when <b>closesocket</b> returns. The <b>closesocket</b> function will initiate cancellation on the outstanding I/O operations, but that does not mean that an application will receive I/O completion for these I/O operations by the time the <b>closesocket</b> function returns. Thus, an application should not cleanup any resources (<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a> structures, for example) referenced by the outstanding I/O requests until the I/O requests are indeed completed.

 


An application should always have a matching call to 
<b>closesocket</b> for each successful call to 
<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> to return any socket resources to the system.

The 
<a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure maintains information about a specific socket that specifies how that socket should behave when data is queued to be sent and the 
<b>closesocket</b> function is called on the socket.

The <b>l_onoff</b> member of the <b>linger</b> structure determines whether a socket should remain open for a specified amount of time after a 
<b>closesocket</b> function call to enable queued data to be sent. This member can be modified in two ways: <ul>
<li>Call the <a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> function with the <i>optname</i> parameter set to <b>SO_DONTLINGER</b>. The <i>optval</i> parameter determines how the <b>l_onoff</b> member is modified. </li>
<li>Call the <a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> function with the <i>optname</i> parameter set to <b>SO_LINGER</b>. The <i>optval</i> parameter specifies how both the <b>l_onoff</b> and <b>l_linger</b> members are modified. </li>
</ul>


The <b>l_linger</b> member of the <b>linger</b> structure determines the amount of time, in seconds, a socket should remain open. This member is only applicable if the <b>l_onoff</b> member of the <b>linger</b> structure is nonzero. 

The default parameters for a socket are the <b>l_onoff</b> member of the <b>linger</b> structure is zero, indicating that the socket should not remain open.  The default value for the <b>l_linger</b> member of the <b>linger</b> structure is zero, but this value is ignored when the <b>l_onoff</b> member is set to zero. 

To enable a socket to remain open, an application should set the <b>l_onoff</b> member to a nonzero value and set the <b>l_linger</b> member  to the desired timeout in seconds. To disable a socket from remaining open, an application only needs to set the  <b>l_onoff</b> member of the <b>linger</b> structure to zero.

 If an application calls the <a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> function with the <i>optname</i> parameter set to <b>SO_DONTLINGER</b> to set the <b>l_onoff</b> member to a nonzero value, the value for the <b>l_linger</b> member is not specified. In this case, the timeout used is implementation dependent. If a previous timeout has been established for a socket (by previously calling the <b>setsockopt</b> function with the <i>optname</i> parameter set to <b>SO_LINGER</b>), this timeout value should be reinstated by the service provider.

The semantics of 
the <b>closesocket</b> function are affected by the socket options that set members of <b>linger</b> structure.  <table>
<tr>
<th><b>l_onoff</b></th>
<th><b>l_linger</b></th>
<th>Type of close</th>
<th>Wait for close?</th>
</tr>
<tr>
<td>zero</td>
<td>Do not care</td>
<td>Graceful close</td>
<td>No</td>
</tr>
<tr>
<td>nonzero</td>
<td>zero</td>
<td>Hard</td>
<td>No</td>
</tr>
<tr>
<td>nonzero</td>
<td>nonzero</td>
<td>
Graceful if all data is sent within timeout value specified in the <b>l_linger</b> member. 

Hard if all data could not be sent within timeout value specified in the <b>l_linger</b> member.

</td>
<td>Yes</td>
</tr>
</table>
 



If the <b>l_onoff</b> member of the 
<a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">LINGER</a> structure is zero on a stream socket, the 
<b>closesocket</b> call will return immediately and does not receive 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a> whether the socket is blocking or nonblocking. However, any data queued for transmission will be sent, if possible, before the underlying socket is closed. This is also called a graceful disconnect or close. In this case, the Windows Sockets provider cannot release the socket and other resources for an arbitrary period, thus affecting applications that expect to use all available sockets. This is the default behavior for a socket.

If the 
<b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure is nonzero and <b>l_linger</b> member is zero, 
<b>closesocket</b> is not blocked even if queued data has not yet been sent or acknowledged. This is called a hard or abortive close, because the socket's virtual circuit is reset immediately, and any unsent data is lost. On Windows, any 
<b>recv</b> call on the remote side of the circuit will fail with 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a>.

If the 
<b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure is set to nonzero and <b>l_linger</b> member is set to a nonzero timeout on a blocking socket, the 
<b>closesocket</b> call blocks until the remaining data has been sent or until the timeout expires. This is called a graceful disconnect or close if all of the data is sent within timeout value specified in the <b>l_linger</b> member. If the timeout expires before all data has been sent, the Windows Sockets implementation terminates the connection before 
<b>closesocket</b> returns and this is called a hard or abortive close.

Setting the <b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure to nonzero and the <b>l_linger</b> member with a nonzero timeout interval on a nonblocking socket is not recommended. In this case, the call to 
<b>closesocket</b> will fail with an error of 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a> if the close operation cannot be completed immediately. If 
<b>closesocket</b> fails with <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEWOULDBLOCK</a> the socket handle is still valid, and a disconnect is not initiated. The application must call 
<b>closesocket</b> again to close the socket. 

If the <b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure is nonzero and the <b>l_linger</b> member is a nonzero timeout interval on a blocking socket, the result of the  <b>closesocket</b> function can't be used to determine whether all data has been sent to the peer. If the data is sent before the timeout specified in the <b>l_linger</b> member expires or if the connection was aborted, the <b>closesocket</b> function won't return an error code (the return value from the <b>closesocket</b> function is zero).  

The <b>closesocket</b> call will only block until all data has been delivered to the peer or the timeout expires. If the connection is reset because the timeout expires, then the socket will not go into TIME_WAIT state. If all data is sent within the timeout period, then the socket can go into TIME_WAIT state.



If the <b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure is nonzero and the <b>l_linger</b> member is a zero timeout interval on a blocking socket,  then a call to <b>closesocket</b> will reset the connection. The socket will not go to the TIME_WAIT state. 

The <a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> function can be called with the <i>optname</i> parameter set to <b>SO_LINGER</b> to retrieve the current value of the <b>linger</b> structure associated with a socket.


<div class="alert"><b>Note</b>  To assure that all data is sent and received on a connection, an application should call 
<a href="https://msdn.microsoft.com/6998f0c6-adc9-481f-b9fb-75f9c9f5caaf">shutdown</a> before calling 
<b>closesocket</b> (see 
<a href="https://msdn.microsoft.com/383747c3-dd3d-4a18-b4e8-2815d5e5c0c7">Graceful shutdown, linger options, and socket closure</a> for more information). Also note, an FD_CLOSE network event is not posted after 
<b>closesocket</b> is called.</div>
<div> </div>



Here is a summary of 
<b>closesocket</b> behavior:

<ul>
<li>If the <b>l_onoff</b> member of the 
<a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">LINGER</a> structure is zero (the default for a socket),  <b>closesocket</b> returns immediately and the connection is gracefully closed in the background.</li>
<li>If the 
<b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure is set to nonzero and the <b>l_linger</b> member is set to zero (no timeout) <b>closesocket</b> returns immediately and the connection is reset or terminated.</li>
<li>If the 
<b>l_onoff</b> member of the <a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a> structure is set to nonzero and the <b>l_linger</b> member is set to a nonzero timeout:–  For a blocking socket, <b>closesocket</b> blocks until all data is sent or the timeout expires.

– For a nonblocking socket, <b>closesocket</b> returns immediately indicating failure.

</li>
</ul>


For additional information please see 
<a href="https://msdn.microsoft.com/383747c3-dd3d-4a18-b4e8-2815d5e5c0c7">Graceful Shutdown, Linger Options, and Socket Closure</a> for more information.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>closesocket</b>,  Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<h3><a id="Notes_for_IrDA_Sockets"></a><a id="notes_for_irda_sockets"></a><a id="NOTES_FOR_IRDA_SOCKETS"></a>Notes for IrDA Sockets</h3>

Keep the following in mind:

<ul>
<li>The Af_irda.h header file must be explicitly included.</li>
<li>The standard linger options are supported.</li>
<li>Although IrDA does not provide a graceful close, IrDA will defer closing until receive queues are purged. Thus, an application can send data and immediately call the 
<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> function, and be confident that the receiver will copy the data before receiving an FD_CLOSE message.</li>
</ul>


<h3><a id="Notes_for_ATM"></a><a id="notes_for_atm"></a><a id="NOTES_FOR_ATM"></a>Notes for ATM</h3>

The following are important issues associated with connection teardown when using Asynchronous Transfer Mode (ATM) and Windows Sockets 2:

<ul>
<li>Using the 
<b>closesocket</b> or 
<a href="https://msdn.microsoft.com/6998f0c6-adc9-481f-b9fb-75f9c9f5caaf">shutdown</a> functions with SD_SEND or SD_BOTH results in a RELEASE signal being sent out on the control channel. Due to ATM's use of separate signal and data channels, it is possible that a RELEASE signal could reach the remote end before the last of the data reaches its destination, resulting in a loss of that data. One possible solutions is programming a sufficient delay between the last data sent and the <b>closesocket</b> or <a href="https://msdn.microsoft.com/6998f0c6-adc9-481f-b9fb-75f9c9f5caaf">shutdown</a> function calls for an ATM socket.</li>
<li>Half close is not supported by ATM.</li>
<li>Both abortive and graceful disconnects result in a RELEASE signal being sent out with the same cause field. In either case, received data at the remote end of the socket is still delivered to the application. See 
<a href="https://msdn.microsoft.com/383747c3-dd3d-4a18-b4e8-2815d5e5c0c7">Graceful Shutdown, Linger Options, and Socket Closure</a> for more information.</li>
</ul>


<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/383747c3-dd3d-4a18-b4e8-2815d5e5c0c7">Graceful Shutdown, Linger Options, and Socket Closure</a>



<a href="https://msdn.microsoft.com/a4d3f599-358c-4a94-91eb-7e1c80244250">WSAAsyncSelect</a>



<a href="https://msdn.microsoft.com/d4028461-bfa6-4074-9460-5d1371790d41">WSADuplicateSocket</a>



<a href="https://msdn.microsoft.com/91004241-e0ea-4bda-a0f5-71688ac83038">WSAOVERLAPPED</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>



<a href="https://msdn.microsoft.com/048fcb8d-acd3-4917-a997-dd133db399f8">ioctlsocket</a>



<a href="https://msdn.microsoft.com/c1dbabcf-b5cd-4a9d-9bf9-b04c62117d74">linger</a>



<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

