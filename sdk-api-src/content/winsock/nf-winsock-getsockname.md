---
UID: NF:winsock.getsockname
title: getsockname function (winsock.h)
description: The getsockname function (winsock.h) retrieves the local name for a socket.
helpviewer_keywords: ["_win32_getsockname_2","getsockname","getsockname function [Winsock]","winsock.getsockname_2","winsock/getsockname"]
old-location: winsock\getsockname_2.htm
tech.root: WinSock
ms.assetid: be20a731-cdfc-48ae-90b2-43f2cf9ecf6d
ms.date: 08/15/2022
ms.keywords: _win32_getsockname_2, getsockname, getsockname function [Winsock], winsock.getsockname_2, winsock/getsockname
req.header: winsock.h
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
 - getsockname
 - winsock/getsockname
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
 - getsockname
---

# getsockname function


## -description

The 
<b>getsockname</b> function retrieves the local name for a socket.

## -parameters

### -param s [in]

Descriptor identifying a socket.

### -param name [out]

Pointer to a 
<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a> structure that receives the address (name) of the socket.

### -param namelen [in, out]

Size of the <i>name</i> buffer, in bytes.

## -returns

If no error occurs, 
<b>getsockname</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
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
<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a> call must occur before using this API.

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
The <i>name</i> or the <i>namelen</i> parameter is not a valid part of the user address space, or the <i>namelen</i> parameter is too small.

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
The descriptor is not a socket.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The socket has not been bound to an address with 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>, or ADDR_ANY is specified in 
<b>bind</b> but connection has not yet occurred.

</td>
</tr>
</table>

## -remarks

The 
<b>getsockname</b> function retrieves the current name for the specified socket descriptor in <i>name</i>. It is used on the bound or connected socket specified by the <i>s</i> parameter. The local association is returned. This call is especially useful when a 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> call has been made without doing a 
<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a> first; the 
<b>getsockname</b> function provides the only way to determine the local association that has been set by the system.

On call, the <i>namelen</i> parameter contains the size of the <i>name</i> buffer, in bytes. On return, the <i>namelen</i> parameter contains the actual size in bytes of the <i>name</i> parameter.

The 
<b>getsockname</b> function does not always return information about the host address when the socket has been bound to an unspecified address, unless the socket has been connected with 
<a href="/windows/desktop/api/winsock2/nf-winsock2-connect">connect</a> or 
<a href="/windows/desktop/api/winsock2/nf-winsock2-accept">accept</a> (for example, using ADDR_ANY). A Windows Sockets application must not assume that the address will be specified unless the socket is connected. The address that will be used for the socket is unknown unless the socket is connected when used in a multihomed host. If the socket is using a connectionless protocol, the address may not be available until I/O occurs on the socket.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR</a>



<a href="/windows/desktop/WinSock/winsock-functions">Winsock Functions</a>



<a href="/windows/desktop/WinSock/winsock-reference">Winsock Reference</a>



<a href="/windows/desktop/api/winsock/nf-winsock-bind">bind</a>



<a href="/windows/desktop/api/winsock/nf-winsock-getpeername">getpeername</a>



<a href="/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a>
