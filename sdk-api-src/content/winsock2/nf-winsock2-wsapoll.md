---
UID: NF:winsock2.WSAPoll
title: WSAPoll function
author: windows-sdk-content
description: The WSAPoll function determines status of one or more sockets.
old-location: winsock\wsapoll.htm
tech.root: WinSock
ms.assetid: 3f6f872c-5cee-49f3-bf22-2e8a5d147987
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: WSAPoll, WSAPoll function [Winsock], mswsock/WSAPoll, winsock.wsapoll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - WSAPoll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WSAPoll
: 
---

# WSAPoll function


## -description


The <b>WSAPoll</b> function determines status of one or more sockets.


## -parameters




### -param fdArray [in, out]

An array of one or more <b>POLLFD</b> structures specifying the set  of sockets for which status is requested. The   array must contain at least one structure with a valid socket. Upon return, this parameter receives the updated sockets with the <b>revents</b> status flags member set on each one that matches the status query criteria.


### -param fds [in]

The number of <b>WSAPOLLFD</b> structures in <i>fdarray</i>. This is not necessarily the number of sockets for which status is requested.


### -param timeout [in]

A value that specifies the wait behavior, based on the following values.
			

<table>
<tr>
<th>Return value</th>
<th>Meaning</th>
</tr>
<tr>
<td>Greater than zero</td>
<td>The time, in milliseconds, to wait.</td>
</tr>
<tr>
<td>Zero</td>
<td>Return immediately.</td>
</tr>
<tr>
<td>Less than zero</td>
<td>Wait indefinitely.</td>
</tr>
</table>
 


## -returns



Returns one of the following values.
			<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>Zero</td>
<td>No sockets were in the queried state before the timer expired.</td>
</tr>
<tr>
<td>Greater than zero</td>
<td>The number of elements in <i>fdarray</i> for which an <b>revents</b> member of the <b>POLLFD</b> structure is nonzero.</td>
</tr>
<tr>
<td>SOCKET_ERROR</td>
<td>An error occurred. Call the <a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function to retrieve the extended error code.</td>
</tr>
</table>
 



<table>
<tr>
<th>Extended Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while reading user input parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. This error is returned if the <i>fdarray</i> parameter contains a <b>NULL</b> pointer. This error is also returned if invalid flags were specified in the <b>events</b> member of any of the <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structures  pointed to by the <i>fdarray</i> parameter when requesting socket
                       status. This error is also returned if none of the sockets specified in the <b>fd</b> member of any of the <b>WSAPOLLFD</b> structures  pointed to by the <i>fdarray</i> parameter were valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOBUFS</a></b></dt>
</dl>
</td>
<td width="60%">
The function was unable to allocate sufficient memory.

</td>
</tr>
</table>
 




## -remarks



The <b>WSAPoll</b> function is defined on Windows Vista and later. 

The <b>WSAPoll</b> function is used to determine the status of one or more sockets. The set of sockets for which status is requested is specified in <i>fdarray</i> parameter, which is an array of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structures.  An application sets the appropriate flags in the <b>events</b> member of the <b>WSAPOLLFD</b> structure to specify the type of status requested for each corresponding socket.  The <b>WSAPoll</b> function returns the status of a socket in the <b>revents</b> member of the <b>WSAPOLLFD</b> structure.

For each socket, a caller can request information on read or write status.  Error conditions are always returned, so information on them need not be requested.

The <i>fdarray</i> parameter must contain at least one valid non-negative socket. Upon return, all of the supplied sockets that either satisfy the requested status conditions or have an error condition will have the appropriate flags set on the <b>revents</b> member of their corresponding <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structure pointed to by the <i>fdarray</i> parameter. All sockets that do not meet these criteria and have no error condition will have the corresponding  <b>revents</b> member set to 0.

A combination of the following flags can be set in the <b>events</b> member of the <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structure for a given socket when requesting status for that socket:<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>POLLPRI</td>
<td>Priority data may be read without blocking. This flag is not supported by the Microsoft Winsock provider.</td>
</tr>
<tr>
<td>POLLRDBAND</td>
<td>Priority band (out-of-band) data may be read without blocking.</td>
</tr>
<tr>
<td>POLLRDNORM</td>
<td>Normal data may be read without blocking.</td>
</tr>
<tr>
<td>POLLWRNORM</td>
<td>Normal data may be written without blocking.</td>
</tr>
</table>
 



The <b>POLLIN</b> flag is defined as the combination of the <b>POLLRDNORM</b>  and <b>POLLRDBAND</b> flag values. The <b>POLLOUT</b> flag is defined as the same as the <b>POLLWRNORM</b>  flag value.

The <b>events</b> member of the <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structure must only contain a combination of the above flags that are supported by the Winsock provider. Any other values are considered errors and  <b>WSAPoll</b> will return <b>SOCKET_ERROR</b>. A subsequent call to  the <a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function will retrieve the extended error code of <a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a>. If the <b>POLLPRI</b> flag is set on a socket for the Microsoft Winsock provider, the <b>WSAPoll</b> function will fail.  

When the <b>WSAPoll</b> function returns a positive value, a combination of the following flags are returned in the <b>revents</b> member of the <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structures pointed to by the <i>fdarray</i> parameter to indicate socket  status:<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>POLLERR</td>
<td>An error has occurred.</td>
</tr>
<tr>
<td>POLLHUP</td>
<td>A stream-oriented connection was either disconnected or aborted.</td>
</tr>
<tr>
<td>POLLNVAL</td>
<td>An invalid socket was used.</td>
</tr>
<tr>
<td>POLLPRI</td>
<td>Priority data may be read without blocking. This flag is not returned by the Microsoft Winsock provider.</td>
</tr>
<tr>
<td>POLLRDBAND</td>
<td>Priority band (out-of-band) data may be read without blocking.</td>
</tr>
<tr>
<td>POLLRDNORM</td>
<td>Normal data may be read without blocking.</td>
</tr>
<tr>
<td>POLLWRNORM</td>
<td>Normal data may be written without blocking.</td>
</tr>
</table>
 




With regard to TCP and UDP sockets:

<ul>
<li>All regular TCP data and all UDP data is considered normal. So if SO_OOBINLINE has been enabled for a socket, out-of-band data will be indicated  in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structure as  normal data as <b>POLLRDNORM</b>.</li>
<li>When normal data is indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structure, a subsequent <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> operation is guaranteed to complete without blocking.</li>
<li>Pending <a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> requests are indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a> structure by <b>POLLWRNORM</b>.</li>
<li>Pending connections on a listening socket are indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a>  structure by <b>POLLRDNORM</b>. A subsequent call to <a href="https://msdn.microsoft.com/72246263-4806-4ab2-9b26-89a1782a954b">accept</a> is guaranteed to complete without blocking.</li>
<li>Any out-of-band data is considered priority band for TCP, and is indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a>  structure by <b>POLLRDBAND</b>.</li>
<li><b>POLLRDNORM</b> is indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a>  structure when a remote peer shuts down a <a href="https://msdn.microsoft.com/902bb9cf-d847-43fc-8282-394d619b8f1b">send</a> operation (a TCP FIN was received). A subsequent <a href="https://msdn.microsoft.com/8c247cd3-479f-45d0-a038-a24e80cc7c73">recv</a> function request will return zero bytes.</li>
<li><b>POLLHUP</b> is indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a>  structure when the remote peer initiates a graceful disconnect.</li>
<li>The <b>POLLHUP</b> and <b>POLLERR</b> are indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a>  structure returned when a remote peer suddenly disconnects.</li>
<li><b>POLLERR</b> is indicated in the returned <b>revents</b> member of <a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a>  structure when the local socket is closed.</li>
</ul>


The number of elements (not sockets) in <i>fdarray</i> is indicated by <i>nfds</i>. Members of <i>fdarray</i> which have their <b>fd</b> member set to a negative value are ignored and their <b>revents</b> will be cleared upon return. This behavior is useful to an application which maintains a fixed <i>fdarray</i> allocation and will not compact the array to remove unused entries or to reallocate memory. It is not necessary to clear <b>revents</b> for any element prior to calling <b>WSAPoll</b>.

The timeout argument specifies how long the function is to wait before returning. A positive value contains the number of milliseconds to wait before returning. A zero value forces <b>WSAPoll</b> to return immediately, and a negative value indicates that <b>WSAPoll</b> should wait indefinitely.

<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>WSAPoll</b> with the <i>timeout</i> parameter set to a negative number, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This   function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>



<a href="https://msdn.microsoft.com/88f122ce-e2ca-44ce-bd53-d73d0962e7ef">WSAPOLLFD</a>
 

 

