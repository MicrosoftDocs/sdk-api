---
UID: NC:ws2spi.LPNSPLOOKUPSERVICEEND
title: LPNSPLOOKUPSERVICEEND (ws2spi.h)
description: Called to free the handle after previous calls to NSPLookupServiceBegin and NSPLookupServiceNext.
helpviewer_keywords: ["LPNSPLOOKUPSERVICEEND","NSPLookupServiceEnd","NSPLookupServiceEnd function [Winsock]","_win32_nsplookupserviceend_2","winsock.nsplookupserviceend_2","ws2spi/NSPLookupServiceEnd"]
old-location: winsock\nsplookupserviceend_2.htm
tech.root: WinSock
ms.assetid: ec72c89a-a74b-449c-996a-02057dff9137
ms.date: 12/05/2018
ms.keywords: LPNSPLOOKUPSERVICEEND, NSPLookupServiceEnd, NSPLookupServiceEnd function [Winsock], _win32_nsplookupserviceend_2, winsock.nsplookupserviceend_2, ws2spi/NSPLookupServiceEnd
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNSPLOOKUPSERVICEEND
 - ws2spi/LPNSPLOOKUPSERVICEEND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPLookupServiceEnd
---

# LPNSPLOOKUPSERVICEEND callback function


## -description

The 
**NSPLookupServiceEnd** function is called to free the handle after previous calls to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a> and 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>.

It is possible to receive an 
**NSPLookupServiceEnd** call on another thread while processing an 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>. This indicates that the client has canceled the request and the provider should close the handle and return from the 
**NSPLookupServiceNext** call as well, setting the last error to **WSA_E_CANCELLED**.

## -parameters

### -param hLookup [in]

The handle obtained previously by a call to  
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>.

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (–1) if the routine fails and it must set the appropriate error code using <a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dl>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dl>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/WinSock/windows-sockets-error-codes-2#WSAEOPNOTSUPP">WSAEOPNOTSUPP</a></b></dl>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
</table>

## -remarks

In Windows Sockets 2, conflicting error codes are defined for **WSAECANCELLED** and <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_E_CANCELLED</a>. The error code **WSAECANCELLED** will be removed in a future version and only WSA_E_CANCELLED will remain. Namespace Providers should use the WSA_E_CANCELLED error code to maintain compatibility with the widest possible range of applications.

## -see-also

<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPLookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicenext">NSPLookupServiceNext</a>



<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nsp_routine">NSP_ROUTINE</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

