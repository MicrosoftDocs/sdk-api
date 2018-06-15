---
UID: NC:ws2spi.LPNSPV2LOOKUPSERVICEEND
title: LPNSPV2LOOKUPSERVICEEND
author: windows-sdk-content
description: Called to free the handle after previous calls to NSPv2LookupServiceBegin and NSPv2LookupServiceNextEx.
old-location: winsock\nspv2lookupserviceend.htm
old-project: WinSock
ms.assetid: 5f2b56c5-3a8e-4bf9-8f28-d2a06543227b
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: LPNSPV2LOOKUPSERVICEEND, NSPv2LookupServiceEnd, NSPv2LookupServiceEnd function [Winsock], winsock.nspv2lookupserviceend, ws2spi/NSPv2LookupServiceEnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - NSPv2LookupServiceEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPV2LOOKUPSERVICEEND callback function


## -description


The 
<b>NSPv2LookupServiceEnd</b> function is called to free the handle after previous calls to 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> and 
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>.


## -parameters




### -param hLookup [in]

The handle obtained previously by a call to  
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>.


## -returns




						The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (â€“1) if the routine fails and it must set the appropriate error code using <a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSA_INVALID_HANDLE</a></b></dt>
</dl>
</td>
<td width="60%">
The handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
</table>
 




## -remarks



The 
<b>NSPv2LookupServiceEnd</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>NSPv2LookupServiceEnd</b> function can only be used for operations on NS_EMAIL namespace providers.

It is possible to receive an 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> function call on another thread while processing an 
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>. This indicates that the client has canceled the request and the provider should close the handle and return from the 
<b>NSPv2LookupServiceNextEx</b> function call as well, setting the last error to <b>WSA_E_CANCELLED</b>.

In Windows Sockets 2, conflicting error codes are defined for <b>WSAECANCELLED</b> and <a href="https://docs.microsoft.com/windows/desktop//WinSock/windows-sockets-error-codes-2">WSA_E_CANCELLED</a>. The error code <b>WSAECANCELLED</b> will be removed in a future version and only WSA_E_CANCELLED will remain. Namespace Providers should use the WSA_E_CANCELLED error code to maintain compatibility with the widest possible range of applications.




## -see-also




<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a>



<a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>



<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>



<a href="https://msdn.microsoft.com/596fe0bd-ec11-44f3-bffe-333758171ea6">NSPv2SetServiceEx</a>



<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

