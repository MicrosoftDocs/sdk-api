---
UID: NF:winsvc.QueryServiceStatus
title: QueryServiceStatus function
author: windows-sdk-content
description: Retrieves the current status of the specified service.
old-location: base\queryservicestatus.htm
old-project: services
ms.assetid: dcd2d8a1-10ef-4229-b873-b4fc3ec9293f
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: QueryServiceStatus, QueryServiceStatus function, _win32_queryservicestatus, base.queryservicestatus, winsvc/QueryServiceStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - QueryServiceStatus
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# QueryServiceStatus function


## -description


Retrieves the current status of the specified service.

This function has been superseded by the 
<a href="https://msdn.microsoft.com/3fe02245-97b1-49f3-8f35-2dcd6f221547">QueryServiceStatusEx</a> function. 
<b>QueryServiceStatusEx</b> returns the same information 
<b>QueryServiceStatus</b> returns, with the addition of the process identifier and additional information for the service.


## -parameters




### -param hService [in]

A handle to the service. This handle is returned by the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or the 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function, and it must have the SERVICE_QUERY_STATUS access right. For more information, see 
<a href="https://msdn.microsoft.com/23d1c382-6ba4-49e2-8039-c2a91471076c">Service Security and Access Rights</a>.


### -param lpServiceStatus [out]

A pointer to a 
<a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a> structure that receives the status information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes can be set by the service control manager. Other error codes can be set by the registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The handle does not have the SERVICE_QUERY_STATUS access right.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 




## -remarks



The 
<b>QueryServiceStatus</b> function returns the most recent service status information reported to the service control manager. If the service just changed its status, it may not have updated the service control manager yet.




## -see-also




<a href="https://msdn.microsoft.com/c112b587-7455-4f15-93e1-ded73de6dbbd">ControlService</a>



<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/3fe02245-97b1-49f3-8f35-2dcd6f221547">QueryServiceStatusEx</a>



<a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>



<a href="https://msdn.microsoft.com/7d2ee779-1554-436a-a65c-f0322745f46a">Service Startup</a>



<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a>
 

 

