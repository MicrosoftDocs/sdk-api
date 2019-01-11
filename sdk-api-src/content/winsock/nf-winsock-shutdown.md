---
UID: NF:winsock.shutdown
title: shutdown function
author: windows-sdk-content
description: The shutdown function disables sends or receives on a socket.
old-location: winsock\shutdown_2.htm
tech.root: WinSock
ms.assetid: 6998f0c6-adc9-481f-b9fb-75f9c9f5caaf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SD_BOTH, SD_RECEIVE, SD_SEND, _win32_shutdown_2, shutdown, shutdown function [Winsock], winsock.shutdown_2, winsock/shutdown
ms.topic: function
req.header: winsock.h
req.include-header: Winsock2.h, Webhost.h
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
 - wsock32.dll
api_name:
 - shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# shutdown function


## -description


The 
<b>shutdown</b> function disables sends or receives on a socket.


## -parameters




### -param s [in]

A descriptor identifying a socket.


### -param how [in]

A flag that describes what types of operation will no longer be allowed. Possible values for this flag are listed in the <i>Winsock2.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SD_RECEIVE"></a><a id="sd_receive"></a><dl>
<dt><b>SD_RECEIVE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Shutdown receive operations.

</td>
</tr>
<tr>
<td width="40%"><a id="SD_SEND"></a><a id="sd_send"></a><dl>
<dt><b>SD_SEND</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Shutdown send operations.

</td>
</tr>
<tr>
<td width="40%"><a id="SD_BOTH"></a><a id="sd_both"></a><dl>
<dt><b>SD_BOTH</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Shutdown both send and receive operations.

</td>
</tr>
</table>
 


## -returns



If no error occurs, 
<b>shutdown</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was terminated due to a time-out or other failure. The application should close the socket as it is no longer usable.

 This error applies only to a connection-oriented socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The virtual circuit was reset by the remote side executing a hard or abortive close. The application should close the socket as it is no longer usable. 

This error applies only to a connection-oriented socket.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>how</i> parameter is not valid, or is not consistent with the socket type. For example, SD_SEND is used with a UNI_RECV socket type.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.  This error applies only to a connection-oriented socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
<div class="alert"><b>Note</b>  The descriptor is not a socket.</div>
<div> </div>
</td>
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
</table>
 




## -remarks



The 
<b>shutdown</b> function is used on all types of sockets to disable reception, transmission, or both.

If the <i>how</i> parameter is SD_RECEIVE, subsequent calls to the 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function on the socket will be disallowed. This has no effect on the lower protocol layers. For TCP sockets, if there is still data queued on the socket waiting to be received, or data arrives subsequently, the connection is reset, since the data cannot be delivered to the user. For UDP sockets, incoming datagrams are accepted and queued. In no case will an ICMP error packet be generated.

If the <i>how</i> parameter is SD_SEND, subsequent calls to the 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> function are disallowed. For TCP sockets, a FIN will be sent after all data is sent and acknowledged by the receiver.

Setting <i>how</i> to SD_BOTH disables both sends and receives as described above.

The 
<b>shutdown</b> function does not close the socket. Any resources attached to the socket will not be freed until 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> is invoked.

To assure that all data is sent and received on a connected socket before it is closed, an application should use 
<b>shutdown</b> to close connection before calling 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>. One method to wait for notification that the remote end has sent all its data and initiated a graceful disconnect uses the <a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> function as follows :

<ol>
<li>Call 
<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a> to register for FD_CLOSE notification.</li>
<li>Call 
<b>shutdown</b> with <i>how</i>=SD_SEND.</li>
<li>When FD_CLOSE received, call 
the <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a>  or <a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> until the function completes with success and indicates that zero bytes were received. If SOCKET_ERROR is returned, then the graceful disconnect is not possible.</li>
<li>Call 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>.</li>
</ol>
Another method to wait for notification that the remote end has sent all its data and initiated a graceful disconnect uses overlapped receive calls follows :

<ol>
<li>Call 
<b>shutdown</b> with <i>how</i>=SD_SEND.</li>
<li>Call 
<a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> or <a href="https://msdn.microsoft.com/bfe66e11-e9a7-4321-ad55-3141113e9a03">WSARecv</a> until the function completes with success and indicates zero bytes were received. If SOCKET_ERROR is returned, then the graceful disconnect is not possible.</li>
<li>Call 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a>.</li>
</ol>

<div class="alert"><b>Note</b>  The 
<b>shutdown</b> function does not block regardless of the SO_LINGER setting on the socket.</div>
<div> </div>


For more information, see the section on <a href="https://msdn.microsoft.com/383747c3-dd3d-4a18-b4e8-2815d5e5c0c7">Graceful Shutdown, Linger Options, and Socket Closure</a>.

Once the <b>shutdown</b> function is called to disable send, receive, or both, there is no method to re-enable send or receive for the existing socket connection. 


An application should not rely on being able to reuse a socket after it has been shut down. In particular, a Windows Sockets provider is not required to support the use of 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> on a socket that has been shut down.

If an application wants to reuse a socket, then the <a href="https://msdn.microsoft.com/220ba610-1694-470d-8b5e-e6b5fc3b4d0b">DisconnectEx</a> function should be called with the <i>dwFlags</i> parameter set to <b>TF_REUSE_SOCKET</b> to close a connection on a socket and prepare the socket handle to be reused.  When the 
<b>DisconnectEx</b> request completes, the socket handle can be passed to the 
<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a> or 
<a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a> function.   

If an application wants to reuse a socket, the <a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a> or <a href="https://msdn.microsoft.com/c574d320-2a90-40bb-b34c-6023e80514e6">TransmitPackets</a> functions can be called with the <i>dwFlags</i> parameter set with <b>TF_DISCONNECT</b> and <b>TF_REUSE_SOCKET</b> to disconnect after all the data has been queued for transmission and prepare the socket handle to be reused. When the <b>TransmitFile</b> request completes, the socket handle can be passed to the 
function call previously used to establish the connection, such as <a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>  or <a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>. When the 
<b>TransmitPackets</b> function completes, the socket handle can be passed to the 
<b>AcceptEx</b> function. 


<div class="alert"><b>Note</b>  The socket level disconnect is subject to the behavior of the underlying transport. For example, a TCP socket may be subject to the TCP TIME_WAIT state, causing  the <a href="https://msdn.microsoft.com/220ba610-1694-470d-8b5e-e6b5fc3b4d0b">DisconnectEx</a>, <a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>, or <a href="https://msdn.microsoft.com/c574d320-2a90-40bb-b34c-6023e80514e6">TransmitPackets</a> call to be delayed.</div>
<div> </div>
<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>shutdown</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>


<h3><a id="Notes_for_ATM"></a><a id="notes_for_atm"></a><a id="NOTES_FOR_ATM"></a>Notes for ATM</h3>
There are important issues associated with connection teardown when using Asynchronous Transfer Mode (ATM) and Windows Sockets 2. For more information about these important considerations, see the section titled Notes for ATM in the Remarks section of the 
<a href="https://msdn.microsoft.com/2f357aa8-389b-4c92-8a9f-289e048cc41c">closesocket</a> function reference.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>



<a href="https://msdn.microsoft.com/a4552366-eafa-4f24-b6c2-e6a7edc4b021">ConnectEx</a>



<a href="https://msdn.microsoft.com/220ba610-1694-470d-8b5e-e6b5fc3b4d0b">DisconnectEx</a>



<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>



<a href="https://msdn.microsoft.com/c574d320-2a90-40bb-b34c-6023e80514e6">TransmitPackets</a>



<a href="https://msdn.microsoft.com/f98a71e4-47fb-47a4-b37e-e4cc801a8f98">WSAEventSelect</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

