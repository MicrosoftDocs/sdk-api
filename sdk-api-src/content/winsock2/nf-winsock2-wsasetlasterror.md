---
UID: NF:winsock2.WSASetLastError
title: WSASetLastError function
author: windows-sdk-content
description: The WSASetLastError function sets the error code that can be retrieved through the WSAGetLastError function.
old-location: winsock\wsasetlasterror_2.htm
tech.root: winsock
ms.assetid: 596155ee-3dcc-4ae3-97ab-0653e019cbee
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: WSASetLastError, WSASetLastError function [Winsock], _win32_wsasetlasterror_2, winsock.wsasetlasterror_2, winsock/WSASetLastError
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WSASetLastError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WSASetLastError
: 
---

# WSASetLastError function


## -description


The 
<b>WSASetLastError</b> function sets the error code that can be retrieved through the 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function.


## -parameters




### -param iError [in]

Integer that specifies the error code to be returned by a subsequent 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> call.


## -returns



This function generates no return values.

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
</table>
 




## -remarks



The 
<b>WSASetLastError</b> function allows an application to set the error code to be returned by a subsequent 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> call for the current thread. Note that any subsequent Windows Sockets routine called by the application will override the error code as set by this routine.

The error code set by 
<b>WSASetLastError</b> is different from the error code reset by calling the function 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> with SO_ERROR. 

The Windows Sockets error codes used by this function are listed under <a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">Windows Sockets Error Codes</a>.

<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>



<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">Windows Sockets Error Codes</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>



<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>
 

 

