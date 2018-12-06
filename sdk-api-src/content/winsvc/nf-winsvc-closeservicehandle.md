---
UID: NF:winsvc.CloseServiceHandle
title: CloseServiceHandle function
author: windows-sdk-content
description: Closes a handle to a service control manager or service object.
old-location: base\closeservicehandle.htm
tech.root: services
ms.assetid: 6cf25994-4939-4aff-af38-5ffc8fc606ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CloseServiceHandle, CloseServiceHandle function, _win32_closeservicehandle, base.closeservicehandle, winsvc/CloseServiceHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winsvc.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Service-management-l1-1-0.dll
api_name:
 - CloseServiceHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseServiceHandle function


## -description


Closes a handle to a service control manager or service object.


## -parameters




### -param hSCObject [in]

A handle to the service control manager object or the service object to close. Handles to service control manager objects are returned by the 
<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a> function, and handles to service objects are returned by either the 
<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> or 
<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error code can be set by the service control manager. Other error codes can be set by registry functions that are called by the service control manager.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
</table>
 




## -remarks



The 
<b>CloseServiceHandle</b> function does not destroy the service control manager object referred to by the handle. A service control manager object cannot be destroyed. A service object can be destroyed by calling the 
<a href="https://msdn.microsoft.com/5b0fc714-60e0-4ae3-8fa8-ace36dab2fb0">DeleteService</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/3bfe4d42-a8a0-4613-9b0f-a80eef54b622">Deleting a Service</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a>



<a href="https://msdn.microsoft.com/5b0fc714-60e0-4ae3-8fa8-ace36dab2fb0">DeleteService</a>



<a href="https://msdn.microsoft.com/a0237989-e5a7-4a3a-ab23-e2474a995341">OpenSCManager</a>



<a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a>



<a href="https://msdn.microsoft.com/5ffdd1a9-1a66-4fc4-b35d-4f744bae4897">SCM Handles</a>



<a href="https://msdn.microsoft.com/63666848-cbac-4853-8b91-89303f9854c0">Service Functions</a>
 

 

