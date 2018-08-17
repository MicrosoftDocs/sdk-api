---
UID: NF:winsock.getservbyname
title: getservbyname function
author: windows-sdk-content
description: The getservbyname function retrieves service information corresponding to a service name and protocol.
old-location: winsock\getservbyname_2.htm
old-project: winsock
ms.assetid: 730fa372-f620-4d21-99b9-3e7b79932792
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_win32_getservbyname_2, getservbyname, getservbyname function [Winsock], winsock.getservbyname_2, winsock/getservbyname"
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
 - getservbyname
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# getservbyname function


## -description


The 
<b>getservbyname</b> function retrieves service information corresponding to a service name and protocol.


## -parameters




### -param name [in]

A pointer to a <b>null</b>-terminated service name.


### -param proto [in]

A pointer to a <b>null</b>-terminated protocol name. If this pointer is <b>NULL</b>, 
the <b>getservbyname</b> function returns the first service entry where <i>name</i> matches the <b>s_name</b> member of the 
<a href="https://msdn.microsoft.com/8696b854-4d37-4d1b-8383-169b5dc7a2ae">servent</a> structure or the <b>s_aliases</b> member of the 
<b>servent</b> structure. Otherwise, 
<b>getservbyname</b> matches both the <i>name</i> and the <i>proto</i>.


## -returns



If no error occurs, 
<b>getservbyname</b> returns a pointer to the 
<a href="https://msdn.microsoft.com/8696b854-4d37-4d1b-8383-169b5dc7a2ae">servent</a> structure. Otherwise, it returns a <b>null</b> pointer and a specific error number can be retrieved by calling 
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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative Answer Service not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
A nonauthoritative Service not found, or server failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors, the services database is not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
Valid name, no data record of requested type.

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
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINTR</a></b></dt>
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
<b>getservbyname</b> function returns a pointer to the 
<a href="https://msdn.microsoft.com/8696b854-4d37-4d1b-8383-169b5dc7a2ae">servent</a> structure containing the name(s) and service number that match the string in the <i>name</i> parameter. All strings are <b>null</b>-terminated.

The pointer that is returned points to the 
<b>servent</b> structure allocated by the Windows Sockets library. The application must never attempt to modify this structure or to free any of its components. Furthermore, only one copy of this structure is allocated per thread, so the application should copy any information it needs before issuing any other Windows Sockets function calls.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/d3524197-cd7a-4863-8fbb-a05e6f5d38e0">WSAAsyncGetServByName</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/afd63c2d-4f77-49df-aeff-bfe56598fcbf">getservbyport</a>
 

 

