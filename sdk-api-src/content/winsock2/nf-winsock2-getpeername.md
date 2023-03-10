---
UID: NF:winsock2.getpeername
title: getpeername function (winsock2.h)
description: The getpeername function (winsock2.h) retrieves the address of the peer to which a socket is connected.  
helpviewer_keywords: ["_win32_getpeername_2","getpeername","getpeername function [Winsock]","winsock.getpeername_2","winsock/getpeername"]
old-location: winsock\getpeername_2.htm
tech.root: WinSock
ms.assetid: df2679a5-cdd9-468b-823a-f98044189f65
ms.date: 08/03/2022
ms.keywords: _win32_getpeername_2, getpeername, getpeername function [Winsock], winsock.getpeername_2, winsock/getpeername
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - getpeername
 - winsock2/getpeername
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
 - getpeername
---

# getpeername function


## -description

The 
<b>getpeername</b> function retrieves the address of the peer to which a socket is connected.

## -parameters

### -param s [in]

A descriptor identifying a connected socket.

### -param name [out]

The 
<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> structure that receives the address of the peer.

### -param namelen [in, out]

A pointer to the size, in bytes, of the <i>name</i> parameter.

## -returns

If no error occurs, 
<b>getpeername</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a>.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> or the <i>namelen</i> parameter is not in a valid part of the user address space, or the <i>namelen</i> parameter is too small.

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
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
</table>

## -remarks

The 
<b>getpeername</b> function retrieves the address of the peer connected to the socket <i>s</i> and stores the address in the <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> structure identified by the <i>name</i> parameter. This function works with any address family and it simply returns the address to which the socket is connected. The 
<b>getpeername</b> function can be used only on a connected socket. 

For datagram sockets, only the address of a peer specified in a previous 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> call will be returned. Any address specified by a previous 
<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a> call will not be returned by 
<b>getpeername</b>.

On call, the <i>namelen</i> parameter contains the size, in bytes, of the <i>name</i> buffer. On return, the <i>namelen</i> parameter contains the actual size, in bytes, of the <i>name</i> parameter returned.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getsockname">getsockname</a>



<a href="/windows/desktop/api/winsock/nf-winsock-sendto">sendto</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
