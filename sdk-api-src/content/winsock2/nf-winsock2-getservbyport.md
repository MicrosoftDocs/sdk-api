---
UID: NF:winsock2.getservbyport
title: getservbyport function
author: windows-sdk-content
description: The getservbyport function retrieves service information corresponding to a port and protocol.
old-location: winsock\getservbyport_2.htm
old-project: WinSock
ms.assetid: afd63c2d-4f77-49df-aeff-bfe56598fcbf
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "_win32_getservbyport_2, getservbyport, getservbyport function [Winsock], winsock.getservbyport_2, winsock/getservbyport"
ms.prod: windows
ms.technology: windows-sdk
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
 - getservbyport
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# getservbyport function


## -description


The 
<b>getservbyport</b> function retrieves service information corresponding to a port and protocol.


## -parameters




### -param port [in]

Port for a service, in network byte order.


### -param proto [in]

Optional pointer to a protocol name. If this is null, 
<b>getservbyport</b> returns the first service entry for which the <i>port</i> matches the <b>s_port</b> of the 
<a href="https://msdn.microsoft.com/8696b854-4d37-4d1b-8383-169b5dc7a2ae">servent</a> structure. Otherwise, 
<b>getservbyport</b> matches both the <i>port</i> and the <i>proto</i> parameters.


## -returns



If no error occurs, 
<b>getservbyport</b> returns a pointer to the 
<a href="https://msdn.microsoft.com/8696b854-4d37-4d1b-8383-169b5dc7a2ae">servent</a> structure. Otherwise, it returns a null pointer and a specific error number can be retrieved by calling 
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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative Answer Service not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
A nonauthoritative Service not found, or server failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors, the services database is not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
Valid name, no data record of requested type.

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
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>proto</i> parameter is not a valid part of the user address space.

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
</table>
 




## -remarks



The 
<b>getservbyport</b> function returns a pointer to a 
<a href="https://msdn.microsoft.com/8696b854-4d37-4d1b-8383-169b5dc7a2ae">servent</a> structure as it does in the 
<a href="https://msdn.microsoft.com/730fa372-f620-4d21-99b9-3e7b79932792">getservbyname</a> function.

The 
<b>servent</b> structure is allocated by Windows Sockets. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other Windows Sockets function calls.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/0d0bd09c-ea97-46fb-b7b0-6e3e0a41dbc1">WSAAsyncGetServByPort</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/730fa372-f620-4d21-99b9-3e7b79932792">getservbyname</a>
 

 

