---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WSAProviderCompleteAsyncCall function


## -description


The 
<b>WSAProviderCompleteAsyncCall</b> function notifies a client when an asynchronous call to a namespace version-2 provider is completed.


## -parameters




### -param hAsyncCall

The handle passed to the asynchronous call being completed. This handle is passed by the client to the namespace version-2 provider in the asynchronous function call. 


### -param iRetCode

The return code for the asynchronous call to the namespace version-2 provider.


## -returns



If no error occurs, 
<b>WSAProviderCompleteAsyncCall</b> returns zero.

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
A parameter was not valid. This error is returned if the <i>hAsyncCall</i> parameter was <b>NULL</b>. 

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
<b>WSAProviderCompleteAsyncCall</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a> function can only be used for operations on NS_EMAIL namespace providers. Asynchronous calls to NSPv2 providers are not supported on Windows Vista and Windows Server 2008. So the <b>WSAProviderCompleteAsyncCall</b> is not currently applicable. This function is planned for use in later versions of Windows when asynchronous calls to namespace providers are supported. 

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the <a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a> and <a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a> functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).




## -see-also




<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a>



<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>



<a href="https://msdn.microsoft.com/5975b496-53a7-4f8a-8efc-27ef447596c2">WSAUnadvertiseProvider</a>
 

 

