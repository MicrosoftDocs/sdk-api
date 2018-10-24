---
UID: NF:processthreadsapi.GetThreadIOPendingFlag
title: GetThreadIOPendingFlag function
author: windows-sdk-content
description: Determines whether a specified thread has any I/O requests pending.
old-location: base\getthreadiopendingflag.htm
tech.root: ProcThread
ms.assetid: 5502f735-38f5-44a4-908d-1b421ee66aec
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetThreadIOPendingFlag, GetThreadIOPendingFlag function, base.getthreadiopendingflag, processthreadsapi/GetThreadIOPendingFlag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadIOPendingFlag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadIOPendingFlag function


## -description


Determines whether a specified thread has any I/O requests pending.


## -parameters




### -param hThread [in]

A handle to the thread in question. This handle must have been created with the THREAD_QUERY_INFORMATION access right. For more information, see <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param lpIOIsPending [in, out]

A pointer to a  variable which the function sets to TRUE if the specified thread has one or more I/O requests pending, or to FALSE otherwise.


## -returns



If the  function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Keep in mind that the I/O status of the specified thread can change  rapidly, and may already have changed by the time the function returns. For example, a pending I/O operation could complete between the time the function sets  <i>lpIOIsPending</i> and the time it returns.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

