---
UID: NF:winsock.getpeername
title: getpeername function
author: windows-sdk-content
description: The getpeername function retrieves the address of the peer to which a socket is connected.
old-location: winsock\getpeername_2.htm
old-project: winsock
ms.assetid: df2679a5-cdd9-468b-823a-f98044189f65
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_win32_getpeername_2, getpeername, getpeername function [Winsock], winsock.getpeername_2, winsock/getpeername"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock.h
req.include-header: Winsock2.h
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
req.typenames: smiVENDORINFO, *smiLPVENDORINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - getpeername
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR</a> structure that receives the address of the peer.


### -param namelen [in, out]

A pointer to the size, in bytes, of the <i>name</i> parameter.


## -returns



If no error occurs, 
<b>getpeername</b> returns zero. Otherwise, a value of SOCKET_ERROR is returned, and a specific error code can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
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
The <i>name</i> or the <i>namelen</i> parameter is not in a valid part of the user address space, or the <i>namelen</i> parameter is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTCONN</a></b></dt>
</dl>
</td>
<td width="60%">
The socket is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAENOTSOCK</a></b></dt>
</dl>
</td>
<td width="60%">
The descriptor is not a socket.

</td>
</tr>
</table>
 




## -remarks



The 
<b>getpeername</b> function retrieves the address of the peer connected to the socket <i>s</i> and stores the address in the <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">SOCKADDR</a> structure identified by the <i>name</i> parameter. This function works with any address family and it simply returns the address to which the socket is connected. The 
<b>getpeername</b> function can be used only on a connected socket. 

For datagram sockets, only the address of a peer specified in a previous 
<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a> call will be returned. Any address specified by a previous 
<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a> call will not be returned by 
<b>getpeername</b>.

On call, the <i>namelen</i> parameter contains the size, in bytes, of the <i>name</i> buffer. On return, the <i>namelen</i> parameter contains the actual size, in bytes, of the <i>name</i> parameter returned.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/3a651daa-7404-4ef7-8cff-0d3dff41a8e8">bind</a>



<a href="https://msdn.microsoft.com/13468139-dc03-45bd-850c-7ac2dbcb6e60">connect</a>



<a href="https://msdn.microsoft.com/be20a731-cdfc-48ae-90b2-43f2cf9ecf6d">getsockname</a>



<a href="https://msdn.microsoft.com/a1c89c6b-d11d-4d3e-a664-af2beed0cd09">sendto</a>



<a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a>
 

 

