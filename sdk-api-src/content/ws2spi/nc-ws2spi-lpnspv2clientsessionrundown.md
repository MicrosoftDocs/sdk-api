---
UID: NC:ws2spi.LPNSPV2CLIENTSESSIONRUNDOWN
title: LPNSPV2CLIENTSESSIONRUNDOWN
author: windows-sdk-content
description: Notifies a namespace service provider version-2 (NSPv2) provider that the client session is terminating.
old-location: winsock\nspv2clientsessionrundown.htm
old-project: WinSock
ms.assetid: 7379b502-129a-4dac-b7eb-e6fae8fb23f8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LPNSPV2CLIENTSESSIONRUNDOWN, NSPv2ClientSessionRundown, NSPv2ClientSessionRundown function [Winsock], winsock.nspv2clientsessionrundown, ws2spi/NSPv2ClientSessionRundown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
req.redist: 
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
 - NSPv2ClientSessionRundown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# LPNSPV2CLIENTSESSIONRUNDOWN callback function


## -description


The 
<b>NSPv2ClientSessionRundown</b> function notifies a namespace service provider version-2 (NSPv2) provider that the client session is terminating.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider to notify.


### -param pvClientSessionArg [in]

A pointer to the client session that is terminating. 


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
The calling routine does not have sufficient privileges to install the service.

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
The operation is not supported. This error is returned if the namespace provider does not implement this function. This error can also be returned if the specified <i>dwControlCode</i> is an unrecognized command.

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
<b>NSPv2ClientSessionRundown</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>NSPv2ClientSessionRundown</b> function can only be used for operations on NS_EMAIL namespace providers.

The 
<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a> function is called each time a new client process begins using namespace provider.  Providers may use the 
client session argument pointed to by the <i>ppvClientSessionArg</i> parameter to store information about this session. If a value was specified for the client session argument in the call to the <b>NSPv2Startup</b> function, then this same client session argument is passed in the  <i>pvClientSessionArg</i> parameter to the <b>NSPv2ClientSessionRundown</b> function.

The <a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>,  <b>NSPv2ClientSessionRundown</b>, and  <a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a> functions are optional, dependent on the requirements of the NSPv2 provider.

 If the <b>NSPv2ClientSessionRundown</b> function isn't implemented, then calls to that function should be intercepted by a stub function that returns <a href="windows_sockets_error_codes_2.htm">WSAEOPNOTSUPP</a>.  The NSPv2 function pointer to the unimplemented <b>NSPv2ClientSessionRundown</b> function in the <a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a> structure should point be to the stub function. 




## -see-also




<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>



<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a>



<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>



<a href="https://msdn.microsoft.com/596fe0bd-ec11-44f3-bffe-333758171ea6">NSPv2SetServiceEx</a>



<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

