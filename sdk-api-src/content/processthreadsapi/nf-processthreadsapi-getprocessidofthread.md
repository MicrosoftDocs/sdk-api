---
UID: NF:processthreadsapi.GetProcessIdOfThread
title: GetProcessIdOfThread function
author: windows-sdk-content
description: Retrieves the process identifier of the process associated with the specified thread.
old-location: base\getprocessidofthread.htm
old-project: ProcThread
ms.assetid: 1878088b-e0fd-4009-b608-f491805948b5
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetProcessIdOfThread, GetProcessIdOfThread function, base.getprocessidofthread, processthreadsapi/GetProcessIdOfThread, winbase/GetProcessIdOfThread
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-0.dll
-	KernelBase.dll
-	MinKernelBase.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-1.dll
-	API-MS-Win-Core-ProcessThreads-l1-1-2.dll
-	api-ms-win-downlevel-kernel32-l1-1-0.dll
-	API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
-	GetProcessIdOfThread
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetProcessIdOfThread function


## -description


Retrieves the process identifier of the process associated with the specified thread.


## -parameters




### -param Thread [in]

 A handle to the thread. The handle must have the THREAD_QUERY_INFORMATION or THREAD_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the THREAD_QUERY_INFORMATION access right. 


## -returns



If the function succeeds, the return value is the process identifier of the process associated with the specified thread.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Until a process terminates, its process identifier uniquely identifies it on the system. For more information about access rights, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546542">GetCurrentThreadId</a>



<a href="https://msdn.microsoft.com/9a024147-8bfe-427a-af12-a63f23328e38">GetProcessId</a>



<a href="https://msdn.microsoft.com/198dfe9e-713f-46ce-90eb-24bfe42d2bf6">GetThreadId</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>
 

 

