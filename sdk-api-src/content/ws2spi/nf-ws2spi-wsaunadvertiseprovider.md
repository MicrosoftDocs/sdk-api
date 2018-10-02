---
UID: NF:ws2spi.WSAUnadvertiseProvider
title: WSAUnadvertiseProvider function
author: windows-sdk-content
description: Makes a specific namespace version-2 provider no longer available for clients.
old-location: winsock\wsaunadvertiseprovider.htm
tech.root: WinSock
ms.assetid: 5975b496-53a7-4f8a-8efc-27ef447596c2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSAUnadvertiseProvider, WSAUnadvertiseProvider function [Winsock], winsock.wsaunadvertiseprovider, ws2spi/WSAUnadvertiseProvider
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
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - WSAUnadvertiseProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSAUnadvertiseProvider function


## -description


The 
<b>WSAUnadvertiseProvider</b> function makes a specific namespace version-2 provider no longer available for clients.


## -parameters




### -param puuidProviderId [in]

A pointer to the provider ID of the namespace provider.


## -returns



If no error occurs, 
<b>WSAUnadvertiseProvider</b> returns zero. Otherwise, it returns <b>SOCKET_ERROR</b>, and a specific error code is available by calling <a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="windows_sockets_error_codes_2.htm">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
A parameter was not valid. This error is returned if the <i>puuidProviderId</i> parameter was <b>NULL</b>. 

</td>
</tr>
</table>
 




## -remarks



The 
<b>WSAUnadvertiseProvider</b> function is used as part of the namespace service provider version-2 (NSPv2) architecture available on Windows Vista and later. 

On Windows Vista and Windows Server 2008, the <b>WSAUnadvertiseProvider</b> function can only be used for operations on NS_EMAIL namespace providers.

In general, NSPv2 providers are implemented in processes other than the calling applications. NSPv2 providers are not activated as result of client activity. Each provider hosting application decides when to make a specific provider available or unavailable by calling the <a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a> and <b>WSAUnadvertiseProvider</b> functions. The client activity only results in attempts to contact the provider, when available (when the namespace provider is advertised).




## -see-also




<a href="https://msdn.microsoft.com/22a4ee47-030b-4aee-b9b1-c9e33b3e4fce">NSPV2_ROUTINE</a>



<a href="https://msdn.microsoft.com/574ebfa4-d7f2-43c2-b1ec-35ce3db9151f">WSAAdvertiseProvider</a>



<a href="https://msdn.microsoft.com/f5b6cd42-c5cb-43b6-bb96-fd260217e252">WSAEnumNameSpaceProviders</a>



<a href="https://msdn.microsoft.com/34bc96aa-63f7-4ab8-9376-6f4b979225ca">WSAEnumNameSpaceProvidersEx</a>



<a href="https://msdn.microsoft.com/21a8ff26-4c9e-4846-a75a-1a27c746edab">WSASetService</a>
 

 

