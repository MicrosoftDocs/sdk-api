---
UID: NS:ws2spi._NSPV2_ROUTINE
title: "_NSPV2_ROUTINE"
author: windows-sdk-content
description: Contains information on the functions implemented by a namespace service provider version-2 (NSPv2) provider.
old-location: winsock\nspv2_routine.htm
tech.root: WinSock
ms.assetid: 22a4ee47-030b-4aee-b9b1-c9e33b3e4fce
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPNSPV2_ROUTINE, *PNSPV2_ROUTINE, NSPV2_ROUTINE, NSPV2_ROUTINE structure [Winsock], PNSPV2_ROUTINE, PNSPV2_ROUTINE structure pointer [Winsock], _NSPV2_ROUTINE, winsock.nspv2_routine, ws2spi/NSPV2_ROUTINE, ws2spi/PNSPV2_ROUTINE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - NSPV2_ROUTINE
product: Windows
targetos: Windows
req.typenames: NSPV2_ROUTINE, *PNSPV2_ROUTINE, *LPNSPV2_ROUTINE
req.redist: 
---

# _NSPV2_ROUTINE structure


## -description


The <b>NSPV2_ROUTINE</b> structure contains information on the functions implemented by a namespace service provider version-2 (NSPv2) provider.<div class="alert"><b>Note</b>  The <i>Ws2spi.h</i> header file structure contains complete prototypes for all the NSPV2 function pointers.</div>
<div> </div>



## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of the structure.


### -field dwMajorVersion

Type: <b>DWORD</b>

The major version of the service provider specification supported by this provider.


### -field dwMinorVersion

Type: <b>DWORD</b>

The minor version of the service provider specification supported by this provider.


### -field NSPv2Startup

Type: <b> LPNSPV2STARTUP</b>

A pointer to the <a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a> function for this NSPv2 provider.


### -field NSPv2Cleanup

Type: <b>LPNSPV2CLEANUP</b>

A pointer to the <a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a> function for this NSPv2 provider.


### -field NSPv2LookupServiceBegin

Type: <b>LPNSPV2LOOKUPSERVICEBEGIN</b>

A pointer to the <a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a> function for this NSPv2 provider.


### -field NSPv2LookupServiceNextEx

Type: <b>LPNSPV2LOOKUPSERVICENEXTEX</b>

A pointer to the <a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a> function for this NSPv2 provider.


### -field NSPv2LookupServiceEnd

Type: <b>LPNSPV2LOOKUPSERVICEEND</b>

A pointer to the <a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a> function for this NSPv2 provider.


### -field NSPv2SetServiceEx

Type: <b>LPNSPV2SETSERVICEEX</b>

A pointer to the <a href="https://msdn.microsoft.com/596fe0bd-ec11-44f3-bffe-333758171ea6">NSPv2SetServiceEx</a> function for this NSPv2 provider.


### -field NSPv2ClientSessionRundown

Type: <b>LPNSPV2CLIENTSESSIONRUNDOWN</b>

A pointer to the <a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a> function for this NSPv2 provider.


## -remarks



The 
<b>NSPV2_ROUTINE</b> structure is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>NSPV2_ROUTINE</b> structure can only be used for operations on NS_EMAIL namespace providers.

The 
<a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a> function advertises an instance of a NSPv2 provider for clients to find. The <b>WSAAdvertiseProvider</b> caller passes a pointer to an <b>NSPV2_ROUTINE</b>  structure in the <i>pNSPv2Routine</i> parameter with the NSPv2 entry points supported by the provider. 


A NSPv2 provider is required to implement the following functions:<ul>
<li>
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a>
</li>
</ul>All other functions are optional, dependent on the requirements of the NSPv2 provider. 

 If a function isn't implemented, then calls to that function should be intercepted by a stub function that returns <a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a>.  The NSPv2 function pointer to the unimplemented function in the <b>NSPV2_ROUTINE</b> structure should point be to the stub function. 

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as a result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the <a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a> and <a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a> functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).

A process can implement and advertise multiple providers at the same time. Windows Sockets will manage the namespace providers by dispatching calls to the correct one. It will also hide RPC interface details and translates cross-process calls into in-process calls. So that the NSPv2 provider has only to implement a table of entry point functions similar to the <a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a> structure used by an NSPv1 provider. A NSPv2 provider does not have to worry about RPC specific requirements (data marshalling and serialization, for example).



The 
<a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a> function makes a specific namespace provider no longer available for clients.




## -see-also




<a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a>



<a href="https://msdn.microsoft.com/36064c0e-c83c-4819-a3e4-c89df50eb659">NSPv2Cleanup</a>



<a href="https://msdn.microsoft.com/7379b502-129a-4dac-b7eb-e6fae8fb23f8">NSPv2ClientSessionRundown</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPv2LookupServiceBegin</a>



<a href="https://msdn.microsoft.com/5f2b56c5-3a8e-4bf9-8f28-d2a06543227b">NSPv2LookupServiceEnd</a>



<a href="https://msdn.microsoft.com/957fe544-9a3f-47f4-a98c-0624747650f4">NSPv2LookupServiceNextEx</a>



<a href="https://msdn.microsoft.com/596fe0bd-ec11-44f3-bffe-333758171ea6">NSPv2SetServiceEx</a>



<a href="https://msdn.microsoft.com/93224e66-9c94-4b5c-af11-ae988b74bc03">NSPv2Startup</a>



<a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a>



<a href="https://msdn.microsoft.com/2bbc20ae-ad6d-47f6-8ca9-dd5559236fbe">WSAProviderCompleteAsyncCall</a>



<a href="https://msdn.microsoft.com/ffe71de0-3561-481f-b81f-835c6c3a3ee4">WSAQUERYSET2</a>



<a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a>
 

 

