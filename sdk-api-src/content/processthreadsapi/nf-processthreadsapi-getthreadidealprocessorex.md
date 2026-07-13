---
UID: NF:processthreadsapi.GetThreadIdealProcessorEx
title: GetThreadIdealProcessorEx function (processthreadsapi.h)
description: Retrieves the processor number of the ideal processor for the specified thread.
helpviewer_keywords: ["GetThreadIdealProcessorEx","GetThreadIdealProcessorEx function","base.getthreadidealprocessorex","processthreadsapi/GetThreadIdealProcessorEx","winbase/GetThreadIdealProcessorEx"]
old-location: base\getthreadidealprocessorex.htm
tech.root: processthreadsapi
ms.assetid: 4fbe1b85-352f-4576-9056-5ba1b0b85874
ms.date: 12/05/2018
ms.keywords: GetThreadIdealProcessorEx, GetThreadIdealProcessorEx function, base.getthreadidealprocessorex, processthreadsapi/GetThreadIdealProcessorEx, winbase/GetThreadIdealProcessorEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetThreadIdealProcessorEx
 - processthreadsapi/GetThreadIdealProcessorEx
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
 - kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadIdealProcessorEx
---

# GetThreadIdealProcessorEx function


## -description

Retrieves the processor number of the ideal processor for the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread for which to retrieve the ideal processor. This handle must have been created with the THREAD_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param lpIdealProcessor [out]

Points to <a href="/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a> structure to receive the number of the ideal processor.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero. To get extended error information, use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex">SetThreadIdealProcessorEx</a>