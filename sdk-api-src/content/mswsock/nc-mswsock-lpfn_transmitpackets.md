---
UID: NC:mswsock.LPFN_TRANSMITPACKETS
title: LPFN_TRANSMITPACKETS
author: windows-sdk-content
description: Transmits in-memory data or file data over a connected socket.
old-location: winsock\transmitpackets_2.htm
tech.root: winsock
ms.assetid: c574d320-2a90-40bb-b34c-6023e80514e6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: LPFN_TRANSMITPACKETS, LPFN_TRANSMITPACKETS callback, LPFN_TRANSMITPACKETS callback function [Winsock], TF_DISCONNECT, TF_REUSE_SOCKET, TF_USE_DEFAULT_WORKER, TF_USE_KERNEL_APC, TF_USE_SYSTEM_THREAD, _win32_transmitpackets_2, mswsock/LPFN_TRANSMITPACKETS, winsock.transmitpackets_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: mswsock.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mswsock.h
api_name:
 - LPFN_TRANSMITPACKETS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPFN_TRANSMITPACKETS callback function


## -description


The 
<b>TransmitPackets</b> function transmits in-memory data or file data over a connected socket. The 
<b>TransmitPackets</b> function uses the operating system cache manager to retrieve file data, locking memory for the minimum time required to transmit and resulting in efficient, high-performance transmission.<div class="alert"><b>Note</b>  This function is a Microsoft-specific extension to the Windows Sockets specification.</div>
<div> </div>



## -parameters




### -param hSocket

A handle to the connected socket to be used in the transmission. Although the socket does not need to be a connection-oriented circuit, the default destination/peer should have been established using the 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>, 
<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>, 
<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>, 
<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>, 
<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>, or 
<a href="https://msdn.microsoft.com/ef9efa03-feed-4f0d-b874-c646cce745c9">WSAJoinLeaf</a> function.


### -param lpPacketArray

An array of type <a href="https://msdn.microsoft.com/cf9f8cd1-284d-4aed-bb43-af02bd012f01">TRANSMIT_PACKETS_ELEMENT</a>, describing the data to be transmitted.


### -param nElementCount

The number of elements in <i>lpPacketArray</i>.


### -param nSendSize

The size, in bytes, of the data block used in the 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> operation. Set <i>nSendSize</i> to zero to let the sockets layer select a default 
<b>send</b> size. 




Setting <i>nSendSize</i> to 0xFFFFFFF enables the caller to control the size and content of each 
<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> request, achieved by using the TP_ELEMENT_EOP flag in the 
<a href="https://msdn.microsoft.com/cf9f8cd1-284d-4aed-bb43-af02bd012f01">TRANSMIT_PACKETS_ELEMENT</a> array pointed to in the <i>lpPacketArray</i> parameter. This capability is useful for message protocols that place limitations on the size of individual 
<b>send</b> requests.


### -param lpOverlapped

A pointer to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure. If the socket handle specified in the <i>hSocket</i> parameter has been opened as overlapped, use this parameter to achieve asynchronous (overlapped) I/O operation. Socket handles are opened as overlapped by default.


### -param dwFlags

A set of flags used to customize processing of the 
<b>TransmitPackets</b> function. The following table outlines the use of the <i>dwFlags</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_DISCONNECT"></a><a id="tf_disconnect"></a><dl>
<dt><b>TF_DISCONNECT</b></dt>
</dl>
</td>
<td width="60%">
Starts a transport-level disconnect after all the file data has been queued for transmission. Applies only to connection-oriented sockets. Specifying this flag for sockets that do not support disconnect semantics (such as datagram sockets) results in an error.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_REUSE_SOCKET"></a><a id="tf_reuse_socket"></a><dl>
<dt><b>TF_REUSE_SOCKET</b></dt>
</dl>
</td>
<td width="60%">
Prepares the socket handle to be reused. When the 
<b>TransmitPackets</b> function completes, the socket handle can be passed to the 
<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a> function. Valid only when a connection-oriented socket and TF_DISCONNECT are specified.

<div class="alert"><b>Note</b>  The socket level packet transmit is subject to the behavior of the underlying transport. For example, a TCP socket may be subject to the TCP TIME_WAIT state, causing  the <b>TransmitPackets</b> call to be delayed.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="TF_USE_DEFAULT_WORKER"></a><a id="tf_use_default_worker"></a><dl>
<dt><b>TF_USE_DEFAULT_WORKER</b></dt>
</dl>
</td>
<td width="60%">
Directs Winsock to use the system's default thread to process long 
<b>TransmitPackets</b> requests. Long 
<b>TransmitPackets</b> requests are defined as requests that require more than a single read from the file or a cache; the long request definition therefore depends on the size of the file and the specified length of the send packet. 




The system default thread can be adjusted using the following registry parameter as a REG_DWORD:<b>HKEY_LOCAL_MACHINE</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>AFD</b>\<b>Parameters</b>\<b>TransmitWorker</b>



</td>
</tr>
<tr>
<td width="40%"><a id="TF_USE_SYSTEM_THREAD"></a><a id="tf_use_system_thread"></a><dl>
<dt><b>TF_USE_SYSTEM_THREAD</b></dt>
</dl>
</td>
<td width="60%">
Directs Winsock to use system threads to process long 
<b>TransmitPackets</b> requests. Long 
<b>TransmitPackets</b> requests are defined as requests that require more than a single read from the file or a cache; the long request definition therefore depends on the size of the file and the specified length of the send packet.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_USE_KERNEL_APC"></a><a id="tf_use_kernel_apc"></a><dl>
<dt><b>TF_USE_KERNEL_APC</b></dt>
</dl>
</td>
<td width="60%">
Directs Winsock to use kernel 
<a href="https://msdn.microsoft.com/0197d78e-a4dc-414b-88ba-c5ec5f2ed614">Asynchronous Procedure Calls</a> (APCs) instead of worker threads to process long 
<b>TransmitPackets</b> requests. Long 
<b>TransmitPackets</b> requests are defined as requests that require more than a single read from the file or a cache; the long request definition therefore depends on the size of the file and the specified length of the send packet. See Remarks for more information.

</td>
</tr>
</table>
 


## -returns



If the 
<b>TransmitPackets</b> function succeeds, the return value is <b>TRUE</b>. Otherwise, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>. An error code 
of <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_IO_PENDING</a> or ERROR_IO_PENDING indicates that the overlapped operation has been successfully initiated and that completion will be indicated at a later time. Any other error code indicates that the overlapped operation was not successfully initiated and no completion indication will occur. Applications should handle either ERROR_IO_PENDING or WSA_IO_PENDING in this case.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
An established connection was aborted by the software in your host machine. This error is returned if the virtual circuit was terminated due to a time-out or other failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAECONNRESET</a></b></dt>
</dl>
</td>
<td width="60%">
An existing connection was forcibly closed by the remote host. This error is returned for a stream socket when the virtual circuit was reset by the remote side. The application should close the socket as it is no longer usable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The system detected an invalid pointer address in attempting to use a pointer argument in a call. This error is returned if the <i>lpPacketArray</i> or the <i>lpOverlapped</i> parameter is not totally contained in a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was supplied. This error is returned if the <i>dwFlags</i> parameter has the  <b>TF_REUSE_SOCKET</b> flag set, but the <b>TF_DISCONNECT</b> flag was not set. This error is also returned if the offset specified in the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure pointed to by the <i>lpOverlapped</i> is not within the file. This error is also returned if the total number of bytes to be transmitted is a value greater than  2,147,483,646, the maximum value for a 32-bit integer minus 1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
A socket operation encountered a dead network.This error is returned if the network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENETRESET</a></b></dt>
</dl>
</td>
<td width="60%">
The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress. This error is returned for a stream socket where the connection was broken due to keep-alive activity detecting a failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full. This error is also returned if the Windows Sockets provider reports a buffer deadlock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
A request to send or receive data was disallowed because the socket is not connected. This error is returned for a stream socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
An operation was attempted on something that is not a socket. This error is returned if the <i>hSocket</i> parameter is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAESHUTDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call. This error is returned if a stream socket has been shut down for sending. It is not possible to 
call <a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a> on a stream socket after 
the <a href="https://msdn.microsoft.com/6998f0c6-adc9-481f-b9fb-75f9c9f5caaf">shutdown</a> function has been called on the socket with the <i>how</i> parameter set to <b>SD_SEND</b> or <b>SD_BOTH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
Either the application has not called the <a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> function, or <b>WSAStartup</b> failed. A successful 
<b>WSAStartup</b> call must occur before using the <a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_IO_PENDING</a></b></dt>
</dl>
</td>
<td width="60%">
An overlapped I/O operation is in progress. This value is returned if an overlapped I/O operation was successfully initiated and indicates that completion will be indicated at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_OPERATION_ABORTED</a></b></dt>
</dl>
</td>
<td width="60%">
The I/O operation has been aborted because of either a thread exit or an application request. This error is returned if the overlapped operation has been canceled due to the closure of the socket, the execution of the "SIO_FLUSH" command in 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>, or the thread that initiated the overlapped request exited before the operation completed.

<div class="alert"><b>Note</b>  All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  asynchronous operations complete. For more information, see <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>.</div>
<div> </div>
</td>
</tr>
</table>
 




## -remarks



The 
<b>TransmitPackets</b> function is optimized according to the operating system on which it is used:


<ul>
<li>On Windows server editions, the 
<b>TransmitPackets</b> function is optimized for high performance.</li>
<li>On Windows client editions, the 
<b>TransmitPackets</b> function is optimized for minimum memory and resource utilization.</li>
</ul>


The maximum number of bytes that can be transmitted using a single call to the <b>TransmitPackets</b> function is 2,147,483,646, the maximum value for a 32-bit integer minus 1. If an application needs to transmit data larger than 2,147,483,646 bytes, then multiple calls to the <b>TransmitPackets</b> function can be used with each call transferring no more than 2,147,483,646 bytes. 


<div class="alert"><b>Note</b>  The function pointer for the 
<b>TransmitPackets</b> function must be obtained at run time by making a call to the 
<a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a> function with the <b>SIO_GET_EXTENSION_FUNCTION_POINTER</b> opcode specified. The input buffer passed to the <b>WSAIoctl</b> function must contain <b>WSAID_TRANSMITPACKETS</b>, a globally unique identifier (GUID) whose value identifies the <b>TransmitPackets</b> extension function. On success, the output returned by the <b>WSAIoctl</b> function contains a pointer to the <b>TransmitPackets</b> function. The <b>WSAID_TRANSMITPACKETS</b> GUID is defined in the <i>Mswsock.h</i> header file.</div>
<div> </div>


Expect better performance results when using the 
<b>TransmitPackets</b> function on Windows Server 2003.

When <i>lpOverlapped</i> is not <b>NULL</b>, overlapped I/O might not finish before the 
<b>TransmitPackets</b> function returns. When this occurs, the 
<b>TransmitPackets</b> function returns fails, and a call to the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function returns ERROR_IO_PENDING, allowing the caller to continue processing while the transmission completes.

<div class="alert"><b>Note</b>   All I/O initiated by a given thread is canceled when that thread exits. For overlapped sockets, pending asynchronous operations can fail if the thread is closed before the  operations complete. See <a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> for more information.</div>
<div> </div>
When the 
<b>TransmitPackets</b> function returns <b>TRUE</b> or returns <b>FALSE</b> and 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> returns ERROR_IO_PENDING, Windows sets the event specified by the <b>hEvent</b> member of the 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure or the socket specified by <i>hSocket</i> to the signaled state, and upon completion, delivers notification to any completion port associated with the socket. Use 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>, or 
<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>, or 
<a href="https://msdn.microsoft.com/en-us/library/Aa364986(v=VS.85).aspx">GetQueuedCompletionStatus</a> to retrieve final status and number of bytes transmitted.

TransmitPackets and Asynchronous Procedure Calls (APCs)

Use of the TF_USE_KERNEL_APC flag can deliver significant performance benefits. If the thread initiating the 
<b>TransmitPackets</b> function call is being used for heavy computations, it is possible, though unlikely, that APCs could be prevented from launching.

<div class="alert"><b>Note</b>  There is a difference between kernel and user-mode APCs:<ul>
<li>Kernel APCs launch when a thread is in a wait state.</li>
<li>User-mode APCs launch when a thread is in an alertable wait state.</li>
</ul>
</div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/cfd4c169-a8af-46cc-9b0e-fd7fb5aad61b">AcceptEx</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa364986(v=VS.85).aspx">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/cf9f8cd1-284d-4aed-bb43-af02bd012f01">TRANSMIT_PACKETS_ELEMENT</a>



<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>



<a href="https://msdn.microsoft.com/f385f63f-49b2-4eb7-8717-ad4cca1a2252">WSAAccept</a>



<a href="https://msdn.microsoft.com/3b32cc6e-3df7-4104-a0d4-317fd445c7b2">WSAConnect</a>



<a href="https://msdn.microsoft.com/3c43ccfd-0fe7-4ecc-9517-e0a1c448f7e4">WSAGetOverlappedResult</a>



<a href="https://msdn.microsoft.com/ef9efa03-feed-4f0d-b874-c646cce745c9">WSAJoinLeaf</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a>
 

 

