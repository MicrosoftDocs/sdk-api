---
UID: NC:ws2spi.LPNSPV2LOOKUPSERVICEEND
title: LPNSPV2LOOKUPSERVICEEND (ws2spi.h)
description: Called to free the handle after previous calls to NSPv2LookupServiceBegin and NSPv2LookupServiceNextEx.
helpviewer_keywords: ["LPNSPV2LOOKUPSERVICEEND","NSPv2LookupServiceEnd","NSPv2LookupServiceEnd function [Winsock]","winsock.nspv2lookupserviceend","ws2spi/NSPv2LookupServiceEnd"]
old-location: winsock\nspv2lookupserviceend.htm
tech.root: WinSock
ms.assetid: 5f2b56c5-3a8e-4bf9-8f28-d2a06543227b
ms.date: 12/05/2018
ms.keywords: LPNSPV2LOOKUPSERVICEEND, NSPv2LookupServiceEnd, NSPv2LookupServiceEnd function [Winsock], winsock.nspv2lookupserviceend, ws2spi/NSPv2LookupServiceEnd
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - LPNSPV2LOOKUPSERVICEEND
 - ws2spi/LPNSPV2LOOKUPSERVICEEND
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
 - NSPv2LookupServiceEnd
---

# LPNSPV2LOOKUPSERVICEEND callback function


## -description

The 
**NSPv2LookupServiceEnd** function is called to free the handle after previous calls to 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a> and 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a>.

## -parameters

### -param hLookup [in]

The handle obtained previously by a call to  
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>.

## -returns

The function should return **NO_ERROR** (zero) if the routine succeeds. It should return **SOCKET_ERROR** (that is, 1) if the routine fails and it must set the appropriate error code using <a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>.



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
</table>

## -remarks

The 
**NSPv2LookupServiceEnd** function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the **NSPv2LookupServiceEnd** function can only be used for operations on NS_EMAIL namespace providers.

It is possible to receive an 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a> function call on another thread while processing an 
<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a>. This indicates that the client has canceled the request and the provider should close the handle and return from the 
**NSPv2LookupServiceNextEx** function call as well, setting the last error to **WSA_E_CANCELLED**.

In Windows Sockets 2, conflicting error codes are defined for **WSAECANCELLED** and <a href="/windows/desktop/WinSock/windows-sockets-error-codes-2">WSA_E_CANCELLED</a>. The error code **WSAECANCELLED** will be removed in a future version and only WSA_E_CANCELLED will remain. Namespace Providers should use the WSA_E_CANCELLED error code to maintain compatibility with the widest possible range of applications.

## -see-also

<a href="/windows/desktop/api/ws2spi/ns-ws2spi-nspv2_routine">NSPV2_ROUTINE</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2cleanup">NSPv2Cleanup</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2clientsessionrundown">NSPv2ClientSessionRundown</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnsplookupservicebegin">NSPv2LookupServiceBegin</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2lookupservicenextex">NSPv2LookupServiceNextEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2setserviceex">NSPv2SetServiceEx</a>



<a href="/windows/desktop/api/ws2spi/nc-ws2spi-lpnspv2startup">NSPv2Startup</a>



<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaqueryset2w">WSAQUERYSET2</a>



<a href="/windows/desktop/api/winsock/nf-winsock-wsasetlasterror">WSASetLastError</a>

