---
UID: NF:processthreadsapi.GetThreadId
title: GetThreadId function
author: windows-sdk-content
description: Retrieves the thread identifier of the specified thread.
old-location: base\getthreadid.htm
old-project: procthread
ms.assetid: 198dfe9e-713f-46ce-90eb-24bfe42d2bf6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetThreadId, GetThreadId function, base.getthreadid, processthreadsapi/GetThreadId, winbase/GetThreadId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetThreadId
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# GetThreadId function


## -description


Retrieves the thread identifier of the specified thread.


## -parameters




### -param Thread [in]

A handle to the thread. The handle must have the THREAD_QUERY_INFORMATION or THREAD_QUERY_LIMITED_INFORMATION access right. For more information about access rights, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the THREAD_QUERY_INFORMATION access right.


## -returns



If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Until a thread terminates, its thread identifier uniquely identifies it on the system.

To compile an application that uses this function, define _WIN32_WINNT as 0x0502 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546542">GetCurrentThreadId</a>



<a href="https://msdn.microsoft.com/9a024147-8bfe-427a-af12-a63f23328e38">GetProcessId</a>



<a href="https://msdn.microsoft.com/1878088b-e0fd-4009-b608-f491805948b5">GetProcessIdOfThread</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

