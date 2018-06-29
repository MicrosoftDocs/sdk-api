---
UID: NF:winsock2.getprotobyname
title: getprotobyname function
author: windows-sdk-content
description: The getprotobyname function retrieves the protocol information corresponding to a protocol name.
old-location: winsock\getprotobyname_2.htm
old-project: WinSock
ms.assetid: 00669525-d477-4607-beaa-61ef5a8dbd4f
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: "_win32_getprotobyname_2, getprotobyname, getprotobyname function [Winsock], winsock.getprotobyname_2, winsock/getprotobyname"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsock2.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
 - getprotobyname
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# getprotobyname function


## -description


The 
<b>getprotobyname</b> function retrieves the protocol information corresponding to a protocol name.


## -parameters




### -param name [in]

Pointer to a null-terminated protocol name.


## -returns



If no error occurs, 
<b>getprotobyname</b> returns a pointer to the 
<a href="https://msdn.microsoft.com/8fc729dd-5a73-42a1-9c3f-adc68d83d863">protoent</a>. Otherwise, it returns a null pointer and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
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
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAENETDOWN</a></b></dt>
</dl>
</td>
<td width="60%">
The network subsystem has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAHOST_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Authoritative answer protocol not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSATRY_AGAIN</a></b></dt>
</dl>
</td>
<td width="60%">
A nonauthoritative protocol not found, or server failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANO_RECOVERY</a></b></dt>
</dl>
</td>
<td width="60%">
Nonrecoverable errors, the protocols database is not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
Valid name, no data record of requested type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINPROGRESS</a></b></dt>
</dl>
</td>
<td width="60%">
A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter is not a valid part of the user address space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEINTR</a></b></dt>
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
<b>getprotobyname</b> function returns a pointer to the 
<a href="https://msdn.microsoft.com/8fc729dd-5a73-42a1-9c3f-adc68d83d863">protoent</a> structure containing the name(s) and protocol number that correspond to the protocol specified in the <i>name</i> parameter. All strings are null-terminated. The 
<b>protoent</b> structure is allocated by the Windows Sockets library. An application must never attempt to modify this structure or to free any of its components. Furthermore, like 
<a href="https://msdn.microsoft.com/f194b9d5-dfaf-4a02-95c6-6d06015aad1d">hostent</a>, only one copy of this structure is allocated per thread, so the application should copy any information that it needs before issuing any other Windows Sockets function calls.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/747c40fd-5dc1-4533-896e-bc1c4368d7bd">WSAAsyncGetProtoByName</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/f1f55ab7-01ca-4ed7-b8f9-e7ddbaa95855">getprotobynumber</a>
 

 

