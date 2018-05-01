---
UID: NF:ws2spi.WSAAdvertiseProvider
title: WSAAdvertiseProvider function
author: windows-driver-content
description: Makes a specific namespace version-2 provider available for all eligible clients.
old-location: winsock\wsaadvertiseprovider.htm
old-project: WinSock
ms.assetid: 574ebfa4-d7f2-43c2-b1ec-35ce3db9151f
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: WSAAdvertiseProvider, WSAAdvertiseProvider function [Winsock], winsock.wsaadvertiseprovider, ws2spi/WSAAdvertiseProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WSC_PROVIDER_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ws2_32.dll
api_name:
-	WSAAdvertiseProvider
product: Windows
targetos: Windows
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSAAdvertiseProvider function


## -description


The 
<b>WSAAdvertiseProvider</b> function makes a specific namespace version-2 provider available for all eligible clients.


## -parameters




### -param puuidProviderId [in]

A pointer to the provider ID of the namespace provider to be advertised.


### -param pNSPv2Routine [in]

A pointer to a <b>NSPV2_ROUTINE</b> structure with the namespace service provider version-2 entry points supported by the provider.


## -returns



If no error occurs, 
<a href="https://msdn.microsoft.com/2bbc20ae-ad6d-47f6-8ca9-dd5559236fbe">WSAProviderCompleteAsyncCall</a> returns zero.

If the function fails, the return value is SOCKET_ERROR. To get extended error information, call 
<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>, which returns one of the following extended error values.

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
There was insufficient memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
A parameter was not valid. This error is returned if the <i>puuidProviderId</i> or <i>pNSPv2Routine</i> parameters were <b>NULL</b>. 

This error is also returned if the <b>NSPv2LookupServiceBegin</b>, <b>NSPv2LookupServiceNextEx</b>, or <b>NSPv2LookupServiceEnd</b> members of the <b>NSPV2_ROUTINE</b> structure pointed to by the <i>pNSPv2Routine</i> parameter are <b>NULL</b>. A namespace version-2 provider must at least support name resolution which this minimum set of functions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVALIDPROVIDER</a></b></dt>
</dl>
</td>
<td width="60%">
The namespace provider could not be found for the specified <i>puuidProviderId</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSANOTINITIALISED</a></b></dt>
</dl>
</td>
<td width="60%">
The <i>Ws2_32.dll</i> has not been initialized. The application must first call 
<a href="https://msdn.microsoft.com/08299592-867c-491d-9769-d16602133659">WSAStartup</a> before calling any Windows Sockets functions.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAAdvertiseProvider</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>WSAAdvertiseProvider</b> function can only be used for operations on NS_EMAIL namespace providers.

The 
<b>WSAAdvertiseProvider</b> function advertises an instance of a NSPv2 provider for clients to find. If the instance to be advertised is an instance of an application-type provider (a namespace provider where the <b>dwProvideType</b> member of the <a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a> structure is <b>ProviderType_Application</b>), the advertised provider instance will be visible to all the client processes running under the same user and in the same session as the caller of <b>WSAAdvertiseProvider</b>. 

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as a result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the <b>WSAAdvertiseProvider</b> and <a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a> functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).

The 
<b>WSAAdvertiseProvider</b> function is called by any application that wants to make a specific provider available for all eligible clients (currently all the applications running with the same credentials as the hosting application, and in the same user session). 



A process can implement and advertise multiple providers at the same time. Windows Sockets will manage the namespace providers by dispatching calls to the correct one. It will also hide RPC interface details and translates cross-process calls into in-process calls. So that the NSPv2 provider has only to implement a table of entry point functions similar to the <a href="https://msdn.microsoft.com/8f7736d5-ea77-472a-a94f-e422398fae3f">NSP_ROUTINE</a> structure used by an NSPv1 provider. A NSPv2 provider does not have to worry about RPC specific requirements (data marshalling and serialization, for example).



The <b>WSAAdvertiseProvider</b> caller passes a pointer to an <a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>  structure in the <i>pNSPv2Routine</i> parameter with the NSPv2 entry points supported by the provider. 


The 
<a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a> function makes a specific namespace provider no longer available for clients.




## -see-also




<a href="https://msdn.microsoft.com/3444ad63-444a-481d-8fe7-f40b2b7d5283">NAPI_PROVIDER_INSTALLATION_BLOB</a>



<a href="https://msdn.microsoft.com/0d845cc5-a84a-43fe-b9e7-d1a9153bae73">NAPI_PROVIDER_TYPE</a>



<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/2bbc20ae-ad6d-47f6-8ca9-dd5559236fbe">WSAProviderCompleteAsyncCall</a>



<a href="https://msdn.microsoft.com/21a8ff26-4c9e-4846-a75a-1a27c746edab">WSASetService</a>



<a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a>



<a href="https://msdn.microsoft.com/544120b2-7575-4deb-8429-2bd4582eceef">WSCEnumNameSpaceProvidersEx32</a>
 

 

