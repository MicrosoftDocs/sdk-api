---
UID: NF:winsock2.select
title: select function (winsock2.h)
description: The select function determines the status of one or more sockets, waiting if necessary, to perform synchronous I/O.
helpviewer_keywords: ["_win32_select_2","select","select function [Winsock]","winsock.select_2","winsock2/select"]
old-location: winsock\select_2.htm
tech.root: WinSock
ms.assetid: f9f1092d-7e15-41cd-a42f-abe8a4f33e15
ms.date: 12/05/2018
ms.keywords: _win32_select_2, select, select function [Winsock], winsock.select_2, winsock2/select
req.header: winsock2.h
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - select
 - winsock2/select
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - select
---

# select function


## -description

The 
<b>select</b> function determines the status of one or more sockets, waiting if necessary, to perform synchronous I/O.

## -parameters

### -param nfds [in]

Ignored. The <i>nfds</i> parameter is included only for compatibility with Berkeley sockets.

### -param readfds [in, out]

An optional pointer to a set of sockets to be checked for readability.

### -param writefds [in, out]

An optional pointer to a set of sockets to be checked for writability.

### -param exceptfds [in, out]

An optional pointer to a set of sockets to be checked for errors.

### -param timeout [in]

The maximum time for 
<b>select</b> to wait, provided in the form of a 
<a href="/windows/desktop/api/winsock/ns-winsock-timeval">TIMEVAL</a> structure. Set the <i>timeout</i> parameter to <b>null</b> for blocking operations.

## -returns

The 
<b>select</b> function returns the total number of socket handles that are ready and contained in the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-fd_set">fd_set</a> structures, zero if the time limit expired, or SOCKET_ERROR if an error occurred. If the return value is SOCKET_ERROR, 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> can be used to retrieve a specific error code.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
A successful 
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The Windows Sockets implementation was unable to allocate needed resources for its internal operations, or the <i>readfds</i>, <i>writefds</i>, <i>exceptfds</i>, or <i>timeval</i> parameters are not part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
<b>WSAEINVAL</b> is returned if the <i>time-out</i> value is invalid, or if all three descriptor parameters are either <b>null</b> pointers or valid pointers to empty <i>fd_set</i> structures containing no sockets.
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINTR</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Socket 1.1 call was canceled through 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
One of the descriptor sets contains an entry that is not a socket.

</td>
</tr>
</table>

## -remarks

The 
<b>select</b> function is used to determine the status of one or more sockets. For each socket, the caller can request information on read, write, or error status. The set of sockets for which a given status is requested is indicated by an 
<a href="/windows/desktop/api/winsock2/ns-winsock2-fd_set">fd_set</a> structure. The sockets contained within the 
<b>fd_set</b> structures must be associated with a single service provider. For the purpose of this restriction, sockets are considered to be from the same service provider if the 
<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structures describing their protocols have the same <i>providerId</i> value. Upon return, the structures are updated to reflect the subset of these sockets that meet the specified condition. The 
<b>select</b> function returns the number of sockets meeting the conditions. A set of macros is provided for manipulating an 
<b>fd_set</b> structure. These macros are compatible with those used in the Berkeley software, but the underlying representation is completely different.

The parameter <i>readfds</i> identifies the sockets that are to be checked for readability. If the socket is currently in the 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> state, it will be marked as readable if an incoming connection request has been received such that an 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> is guaranteed to complete without blocking. For other sockets, readability means that queued data is available for reading such that a call to 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecv">WSARecv</a>, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom">WSARecvFrom</a>, or 
<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a> is guaranteed not to block.

For connection-oriented sockets, readability can also indicate that a request to close the socket has been received from the peer. If the virtual circuit was closed gracefully, and all data was received, then a 
<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a> will return immediately with zero bytes read. If the virtual circuit was reset, then a 
<b>recv</b> will complete immediately with an error code such as 
<a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAECONNRESET</a>. The presence of OOB data will be checked if the socket option SO_OOBINLINE has been enabled (see 
<a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>).

The parameter <i>writefds</i> identifies the sockets that are to be checked for writability. If a socket is processing a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> call (nonblocking), a socket is writable if the connection establishment successfully completes. If the socket is not processing a 
<b>connect</b> call, writability means a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>, 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>, or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsasendto">WSASendto</a> are guaranteed to succeed. However, they can block on a blocking socket if the <i>len</i> parameter exceeds the amount of outgoing system buffer space available. It is not specified how long these guarantees can be assumed to be valid, particularly in a multithreaded environment.

The parameter <i>exceptfds</i> identifies the sockets that are to be checked for the presence of OOB data or any exceptional error conditions.

<div class="alert"><b>Note</b>  Out-of-band data will only be reported in this way if the option SO_OOBINLINE is <b>FALSE</b>. If a socket is processing a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> call (nonblocking), failure of the connect attempt is indicated in <i>exceptfds</i> (application must then call 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> SO_ERROR to determine the error value to describe why the failure occurred). This document does not define which other errors will be included.</div>
<div> </div>
Any two of the parameters, <i>readfds</i>, <i>writefds</i>, or <i>exceptfds</i>, can be given as <b>null</b>. At least one must be non-<b>null</b>, and any non-<b>null</b> descriptor set must contain at least one handle to a socket.

In summary, a socket will be identified in a particular set when 
<b>select</b> returns if:

<i>readfds</i>:

<ul>
<li>If 
<a href="/windows/desktop/api/winsock2/nf-winsock2-listen">listen</a> has been called and a connection is pending, 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> will succeed.</li>
<li>Data is available for reading (includes OOB data if SO_OOBINLINE is enabled).</li>
<li>Connection has been closed/reset/terminated.</li>
</ul>
<i>writefds</i>:

<ul>
<li>If processing a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> call (nonblocking), connection has succeeded.</li>
<li>Data can be sent.</li>
</ul>
<i>exceptfds</i>:

<ul>
<li>If processing a 
<b>connect</b> call (nonblocking), connection attempt failed.</li>
<li>OOB data is available for reading (only if SO_OOBINLINE is disabled).</li>
</ul>
Four macros are defined in the header file Winsock2.h for manipulating and checking the descriptor sets. The variable FD_SETSIZE determines the maximum number of descriptors in a set. (The default value of FD_SETSIZE is 64, which can be modified by defining FD_SETSIZE to another value before including Winsock2.h.) Internally, socket handles in an 
<a href="/windows/desktop/api/winsock2/ns-winsock2-fd_set">fd_set</a> structure are not represented as bit flags as in Berkeley Unix. Their data representation is opaque. Use of these macros will maintain software portability between different socket environments. The macros to manipulate and check 
<b>fd_set</b> contents are:
<ul>
<li><i>FD_ZERO(*set)</i> - Initializes set to the empty set. A set should always be cleared before using.</li>
<li><i>FD_CLR(s, *set)</i> - Removes socket s from set.</li>
<li><i>FD_ISSET(s, *set)</i> - Checks to see if s is a member of set and returns TRUE if so.</li>
<li><i>FD_SET(s, *set)</i> - Adds socket s to set.</li>
</ul>


The parameter <i>time-out</i> controls how long the 
<b>select</b> can take to complete. If <i>time-out</i> is a <b>null</b> pointer, 
<b>select</b> will block indefinitely until at least one descriptor meets the specified criteria. Otherwise, <i>time-out</i> points to a 
<a href="/windows/desktop/api/winsock/ns-winsock-timeval">TIMEVAL</a> structure that specifies the maximum time that 
<b>select</b> should wait before returning. When 
<b>select</b> returns, the contents of the <b>TIMEVAL</b> structure are not altered. If <b>TIMEVAL</b> is initialized to {0, 0}, 
<b>select</b> will return immediately; this is used to poll the state of the selected sockets. If 
<b>select</b> returns immediately, then the 
<b>select</b> call is considered nonblocking and the standard assumptions for nonblocking calls apply. For example, the blocking hook will not be called, and Windows Sockets will not yield.

<div class="alert"><b>Note</b>  The 
<b>select</b> function has no effect on the persistence of socket events registered with 
<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>.</div>
<div> </div>
<div class="alert"><b>Note</b>  When issuing a blocking Winsock call such as <b>select</b> with the <i>timeout</i> parameter set to <b>NULL</b>, Winsock may need to wait for a network event before the call can complete. Winsock performs an alertable wait in this situation, which can be interrupted by an asynchronous procedure call (APC) scheduled on the same thread. Issuing another blocking Winsock call inside an APC that interrupted an ongoing blocking Winsock call on the same thread will lead to undefined behavior, and must never be attempted by Winsock clients. </div>
<div> </div>
<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/winsock/ns-winsock-timeval">TIMEVAL</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsaasyncselect">WSAAsyncSelect</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-wsaeventselect">WSAEventSelect</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recv">recv</a>



<a href="/windows/desktop/api/winsock/nf-winsock-recvfrom">recvfrom</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-send">send</a>
