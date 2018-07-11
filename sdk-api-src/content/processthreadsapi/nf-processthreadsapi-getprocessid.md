---
UID: NF:processthreadsapi.GetProcessId
title: GetProcessId function
author: windows-sdk-content
description: Retrieves the process identifier of the specified process.
old-location: base\getprocessid.htm
old-project: ProcThread
ms.assetid: 9a024147-8bfe-427a-af12-a63f23328e38
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetProcessId, GetProcessId function, base.getprocessid, processthreadsapi/GetProcessId, winbase/GetProcessId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps | UWP apps]
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
 - GetProcessId
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# GetProcessId function


## -description


Retrieves the process identifier of the specified process.


## -parameters




### -param Process [in]

A handle to the process. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.


## -remarks



Until a process terminates, its process identifier uniquely identifies it on the system. For more information about access rights, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545836">GetCurrentProcessId</a>



<a href="https://msdn.microsoft.com/1878088b-e0fd-4009-b608-f491805948b5">GetProcessIdOfThread</a>



<a href="https://msdn.microsoft.com/198dfe9e-713f-46ce-90eb-24bfe42d2bf6">GetThreadId</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

