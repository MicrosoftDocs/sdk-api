---
UID: NC:ws2spi.LPNSPLOOKUPSERVICEEND
title: LPNSPLOOKUPSERVICEEND (ws2spi.h)
author: windows-sdk-content
description: Called to free the handle after previous calls to NSPLookupServiceBegin and NSPLookupServiceNext.
old-location: winsock\nsplookupserviceend_2.htm
tech.root: WinSock
ms.assetid: ec72c89a-a74b-449c-996a-02057dff9137
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPNSPLOOKUPSERVICEEND, NSPLookupServiceEnd, NSPLookupServiceEnd function [Winsock], _win32_nsplookupserviceend_2, winsock.nsplookupserviceend_2, ws2spi/NSPLookupServiceEnd
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPNSPLOOKUPSERVICEEND callback function


## -description


The 
<b>NSPLookupServiceEnd</b> function is called to free the handle after previous calls to 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>.

It is possible to receive an 
<b>NSPLookupServiceEnd</b> call on another thread while processing an 
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>. This indicates that the client has canceled the request and the provider should close the handle and return from the 
<b>NSPLookupServiceNext</b> call as well, setting the last error to <b>WSA_E_CANCELLED</b>.


## -parameters




### -param hLookup [in]

The handle obtained previously by a call to  
<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>.


## -returns



The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (–1) if the routine fails and it must set the appropriate error code using <a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
</table>
 




## -remarks



In Windows Sockets 2, conflicting error codes are defined for <b>WSAECANCELLED</b> and <a href="https://docs.microsoft.com/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_E_CANCELLED</a>. The error code <b>WSAECANCELLED</b> will be removed in a future version and only WSA_E_CANCELLED will remain. Namespace Providers should use the WSA_E_CANCELLED error code to maintain compatibility with the widest possible range of applications.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ws2spi/ns-ws2spi-_nsp_routine">NSP_ROUTINE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>
 

 

