---
UID: NF:winsvc.QueryServiceDynamicInformation
title: QueryServiceDynamicInformation function
author: windows-sdk-content
description: Retrieves dynamic information related to the current service start.
old-location: base\queryservicedynamicinformation.htm
old-project: services
ms.assetid: 499b63fd-e77b-4b90-9ee7-ff4b7b12c431
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: QueryServiceDynamicInformation, QueryServiceDynamicInformation function, SERVICE_DYNAMIC_INFORMATION_LEVEL_START_REASON, base.queryservicedynamicinformation, winsvc/QueryServiceDynamicInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Service-Core-l1-1-1.dll
 - sechost.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
api_name:
 - QueryServiceDynamicInformation
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# QueryServiceDynamicInformation function


## -description


Retrieves dynamic information related to the current service start.


## -parameters




### -param hServiceStatus [in]

A service status handle provided by <a href="https://msdn.microsoft.com/23eea346-9899-4214-88f4-9b7eb7ce1332">RegisterServiceCtrlHandlerEx</a>



### -param dwInfoLevel [in]

Indicates the information level.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_DYNAMIC_INFORMATION_LEVEL_START_REASON"></a><a id="service_dynamic_information_level_start_reason"></a><dl>
<dt><b>SERVICE_DYNAMIC_INFORMATION_LEVEL_START_REASON</b></dt>
</dl>
</td>
<td width="60%">
Indicates a request for dynamic information related to the current service start.

</td>
</tr>
</table>
 


### -param ppDynamicInfo

A dynamic information buffer. If this parameter is valid, the callback function must free the          buffer after use with the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function.


## -returns



If the function succeeds, the return value is TRUE.

If the function fails, the return value is FALSE. When this happens the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function should be called to retrieve the error code.




## -see-also




<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>



<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/364c5f61-dfbe-460b-8e42-5c457b65c050">QueryServiceConfig</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/5d95945f-f11b-42af-b302-8d924917b9ab">QueryServiceObjectSecurity</a>



<a href="https://msdn.microsoft.com/fc8c631e-076c-4745-8db0-90f46a202e6a">Service Configuration</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

