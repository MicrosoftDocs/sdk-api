---
UID: NF:processthreadsapi.GetCurrentProcessorNumber
title: GetCurrentProcessorNumber function (processthreadsapi.h)
description: Retrieves the number of the processor the current thread was running on during the call to this function.
helpviewer_keywords: ["GetCurrentProcessorNumber","GetCurrentProcessorNumber function","base.getcurrentprocessornumber","processthreadsapi/GetCurrentProcessorNumber","winbase/GetCurrentProcessorNumber"]
old-location: base\getcurrentprocessornumber.htm
tech.root: processthreadsapi
ms.assetid: 1f2bebc7-a548-409a-ab74-78a4b55c8fa7
ms.date: 12/05/2018
ms.keywords: GetCurrentProcessorNumber, GetCurrentProcessorNumber function, base.getcurrentprocessornumber, processthreadsapi/GetCurrentProcessorNumber, winbase/GetCurrentProcessorNumber
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentProcessorNumber
 - processthreadsapi/GetCurrentProcessorNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - ntdll.dll
api_name:
 - GetCurrentProcessorNumber
 - RtlGetCurrentProcessorNumber
---

# GetCurrentProcessorNumber function


## -description

Retrieves the number of the processor the current thread was running on during the call to this function.

## -returns

The function returns the current processor number.

## -remarks

This function is used to provide information for estimating process performance.

On systems with more than 64 logical processors, the <b>GetCurrentProcessorNumber</b> function returns the processor number within the <a href="/windows/desktop/ProcThread/processor-groups">processor group</a> to which the logical processor is assigned. Use the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex">GetCurrentProcessorNumberEx</a> function to retrieve the processor group and number of the current processor.

## -see-also

<a href="/windows/desktop/ProcThread/multiple-processors">Multiple Processors</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>
