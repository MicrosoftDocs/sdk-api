---
UID: NF:processthreadsapi.GetCurrentThreadId
title: GetCurrentThreadId function
author: windows-sdk-content
description: Retrieves the thread identifier of the calling thread.
old-location: base\getcurrentthreadid.htm
old-project: ProcThread
ms.assetid: a496f61a-e027-44e7-8b22-4f6651d7afb2
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetCurrentThreadId, GetCurrentThreadId function, _win32_getcurrentthreadid, base.getcurrentthreadid, processthreadsapi/GetCurrentThreadId, winbase/GetCurrentThreadId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetCurrentThreadId
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetCurrentThreadId function


## -description


Retrieves the thread identifier of the calling thread.


## -parameters






## -returns



The return value is the thread identifier of the calling thread.




## -remarks



Until the thread terminates, the thread identifier uniquely identifies the thread throughout the system.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b7f5a206-a827-4b6b-86f6-5e3aea1246b7">Using Thread Local Storage</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/91a11552-66c1-42bd-b837-8a7685977bc9">GetCurrentThread</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

