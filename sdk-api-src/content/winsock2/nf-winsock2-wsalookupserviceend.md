---
UID: NF:winsock2.WSALookupServiceEnd
title: WSALookupServiceEnd function
author: windows-sdk-content
description: The WSALookupServiceEnd function is called to free the handle after previous calls to WSALookupServiceBegin and WSALookupServiceNext.
old-location: winsock\wsalookupserviceend_2.htm
old-project: winsock
ms.assetid: f9d2ac54-a818-464d-918e-80ebb5b1b106
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: WSALookupServiceEnd, WSALookupServiceEnd function [Winsock], _win32_wsalookupserviceend_2, winsock.wsalookupserviceend_2, winsock2/WSALookupServiceEnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - WSALookupServiceEnd
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSALookupServiceEnd function


## -description



			The 
<b>WSALookupServiceEnd</b> function is called to free the handle after previous calls to 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a> and 
<a href="https://msdn.microsoft.com/ab4f1830-b38d-4224-a6a9-6d4512245ad6">WSALookupServiceNext</a>.
			

If you call 
<b>WSALookupServiceEnd</b> from another thread while an existing 
<a href="https://msdn.microsoft.com/ab4f1830-b38d-4224-a6a9-6d4512245ad6">WSALookupServiceNext</a> is blocked, the end call will have the same effect as a cancel and will cause the 
<b>WSALookupServiceNext</b> call to return immediately.


## -parameters




### -param hLookup [in]

Handle previously obtained by calling 
<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>.


## -returns



The return value is zero if the operation was successful. Otherwise, the value SOCKET_ERROR is returned, and a specific error number can be retrieved by calling 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The WS2_32.DLL has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to perform the operation.

</td>
</tr>
</table>
 




## -remarks



<b>Windows Phone 8:</b> This function is supported for Windows Phone Store apps on Windows Phone 8 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/3f901176-2433-4d51-ae52-648abbd2e318">Bluetooth and WSALookupServiceEnd</a>



<a href="https://msdn.microsoft.com/448309ef-b9dd-4960-8016-d26691df59ec">WSALookupServiceBegin</a>



<a href="https://msdn.microsoft.com/ab4f1830-b38d-4224-a6a9-6d4512245ad6">WSALookupServiceNext</a>



<a href="https://msdn.microsoft.com/edafb5f9-09fe-4f8e-9651-4002b6f622f4">Winsock Functions</a>



<a href="https://msdn.microsoft.com/baae2bf9-f505-4365-b60e-e3247a0218c8">Winsock Reference</a>
 

 

