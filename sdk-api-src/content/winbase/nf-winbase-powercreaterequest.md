---
UID: NF:winbase.PowerCreateRequest
title: PowerCreateRequest function
author: windows-sdk-content
description: Creates a new power request object.
old-location: base\powercreaterequest.htm
old-project: power
ms.assetid: 2122bf00-9e6b-48ab-89b0-f53dd6804902
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: PowerCreateRequest, PowerCreateRequest function, base.powercreaterequest, winbase/PowerCreateRequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - PowerCreateRequest
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PowerCreateRequest function


## -description


Creates a new power request object. 


## -parameters




### -param Context [in]

Points to a <a href="https://msdn.microsoft.com/006bb84f-5e51-4f6e-8a44-6b50e763c5ca">REASON_CONTEXT</a> structure that contains information about the power request.


## -returns



If the function succeeds, the return value is a handle to the power request object.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When the power request object is no longer needed, use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to free the handle and clean up the object.




## -see-also




<a href="https://msdn.microsoft.com/794248b1-5aa8-495e-aca6-1a1f35dc9c7f">PowerClearRequest</a>



<a href="https://msdn.microsoft.com/85249de8-5832-4f25-bbd9-3576cfd1caa0">PowerSetRequest</a>
 

 

