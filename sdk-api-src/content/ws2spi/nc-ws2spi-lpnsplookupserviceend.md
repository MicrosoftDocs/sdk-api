---
UID: NC:ws2spi.LPNSPLOOKUPSERVICEEND
title: LPNSPLOOKUPSERVICEEND
author: windows-sdk-content
description: Called to free the handle after previous calls to NSPLookupServiceBegin and NSPLookupServiceNext.
old-location: winsock\nsplookupserviceend_2.htm
old-project: winsock
ms.assetid: ec72c89a-a74b-449c-996a-02057dff9137
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: LPNSPLOOKUPSERVICEEND, NSPLookupServiceEnd, NSPLookupServiceEnd function [Winsock], _win32_nsplookupserviceend_2, winsock.nsplookupserviceend_2, ws2spi/NSPLookupServiceEnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SOCKADDR_INET, *PSOCKADDR_INET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPLookupServiceEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPLOOKUPSERVICEEND callback function


## -description



			The 
<b>NSPLookupServiceEnd</b> function is called to free the handle after previous calls to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> and 
<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>.

It is possible to receive an 
<b>NSPLookupServiceEnd</b> call on another thread while processing an 
<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>. This indicates that the client has canceled the request and the provider should close the handle and return from the 
<b>NSPLookupServiceNext</b> call as well, setting the last error to <b>WSA_E_CANCELLED</b>.


## -parameters




### -param hLookup [in]

The handle obtained previously by a call to  
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>.


## -returns




						The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (–1) if the routine fails and it must set the appropriate error code using <a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



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
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
</table>
 




## -remarks



In Windows Sockets 2, conflicting error codes are defined for <b>WSAECANCELLED</b> and <a href="https://msdn.microsoft.com/library/ms740668(v=VS.85).aspx">WSA_E_CANCELLED</a>. The error code <b>WSAECANCELLED</b> will be removed in a future version and only WSA_E_CANCELLED will remain. Namespace Providers should use the WSA_E_CANCELLED error code to maintain compatibility with the widest possible range of applications.




## -see-also




<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>



<a href="https://msdn.microsoft.com/321732e4-5d48-48f4-8795-ffac208852dc">NSPLookupServiceNext</a>



<a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

