---
UID: NC:ws2spi.LPNSPV2CLEANUP
title: LPNSPV2CLEANUP
author: windows-sdk-content
description: Notifies a namespace service provider version-2 (NSPv2) provider that a client session has terminated.
old-location: winsock\nspv2cleanup.htm
tech.root: WinSock
ms.assetid: 36064c0e-c83c-4819-a3e4-c89df50eb659
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: LPNSPV2CLEANUP, NSPv2Cleanup, NSPv2Cleanup function [Winsock], winsock.nspv2cleanup, ws2spi/NSPv2Cleanup
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
 - NSPv2Cleanup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPNSPV2CLEANUP callback function


## -description


The 
<b>NSPv2Cleanup</b> function notifies a namespace service provider version-2 (NSPv2) provider that a client session has terminated.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the namespace provider to be notified.


### -param pvClientSessionArg [in]

A pointer to the client session. 


## -returns



The function should return <b>NO_ERROR</b> (zero) if the routine succeeds. It should return <b>SOCKET_ERROR</b> (â€“1) if the routine fails and it must set the appropriate error code using 
<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to initialize the service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
One or more parameters were invalid, or missing, for this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSASERVICE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
Service is unknown. The service cannot be found in the specified namespace.

</td>
</tr>
</table>
 




## -remarks



The 
<b>NSPv2Cleanup</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>NSPv2Cleanup</b> function can only be used for operations on NS_EMAIL namespace providers.

The 
<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a> function is called each time a new client process begins using namespace provider.  Providers may use the 
client session argument pointed to by the <i>ppvClientSessionArg</i> parameter to store information about this session. If a value was specified for the client session argument in the call to the <b>NSPv2Startup</b> function, then this same client session argument can be passed in the  pvClientSessionArg parameter to the <b>NSPv2Cleanup</b> function to notify namespace provider that the client session has terminated.

The 
<b>NSPv2Cleanup</b> function is called when an application is finished using a Windows Sockets namespace service provider. The 
<b>NSPv2Cleanup</b> allows the namespace provider to free any of namespace provider resources that were allocated for the client session.

The 
<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a> function must be called successfully before calling the <b>NSPv2Cleanup</b> function. It is permissible to make more than one 
<b>NSPv2Startup</b> call. However, for each 
<b>NSPv2Startup</b> call, a corresponding 
<b>NSPv2Cleanup</b> call must also be issued. Only the final 
<b>NSPv2Cleanup</b> for the service provider does the actual cleanup; the preceding calls decrement an internal reference count in the service provider.

The <a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>,  <a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a>, and  <b>NSPv2Cleanup</b> functions are optional, dependent on the requirements of the NSPv2 provider.

 If the <b>NSPv2Cleanup</b> function isn't implemented, then calls to that function should be intercepted by a stub function that returns <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>.  The NSPv2 function pointer to the unimplemented <b>NSPv2Cleanup</b> function in the <a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a> structure should point be to the stub function. 




## -see-also




<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>



<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a>



<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>



<a href="https://msdn.microsoft.com/596fe0bd-ec11-44f3-bffe-333758171ea6">NSPv2SetServiceEx</a>



<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

