---
UID: NF:processthreadsapi.GetThreadIdealProcessorEx
title: GetThreadIdealProcessorEx function
author: windows-sdk-content
description: Retrieves the processor number of the ideal processor for the specified thread.
old-location: base\getthreadidealprocessorex.htm
tech.root: procthread
ms.assetid: 4fbe1b85-352f-4576-9056-5ba1b0b85874
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: GetThreadIdealProcessorEx, GetThreadIdealProcessorEx function, base.getthreadidealprocessorex, processthreadsapi/GetThreadIdealProcessorEx, winbase/GetThreadIdealProcessorEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadIdealProcessorEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadIdealProcessorEx function


## -description


Retrieves the processor number of the ideal processor for the specified thread.


## -parameters




### -param hThread [in]

A handle to the thread for which to retrieve the ideal processor. This handle must have been created with the THREAD_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param lpIdealProcessor [out]

Points to <a href="https://msdn.microsoft.com/9005c6d4-07a9-4ce0-9ee2-54880d7244c3">PROCESSOR_NUMBER</a> structure to receive the number of the ideal processor.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero. To get extended error information, use <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/6b599a99-41c5-45c7-8aeb-87d8f34e9e82">SetThreadIdealProcessorEx</a>
 

 

