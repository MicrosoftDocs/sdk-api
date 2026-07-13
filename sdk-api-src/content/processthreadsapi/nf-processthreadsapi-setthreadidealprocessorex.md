---
UID: NF:processthreadsapi.SetThreadIdealProcessorEx
title: SetThreadIdealProcessorEx function (processthreadsapi.h)
description: Sets the ideal processor for the specified thread and optionally retrieves the previous ideal processor.
helpviewer_keywords: ["SetThreadIdealProcessorEx","SetThreadIdealProcessorEx function","base.setthreadidealprocessorex","processthreadsapi/SetThreadIdealProcessorEx","winbase/SetThreadIdealProcessorEx"]
old-location: base\setthreadidealprocessorex.htm
tech.root: processthreadsapi
ms.assetid: 6b599a99-41c5-45c7-8aeb-87d8f34e9e82
ms.date: 12/05/2018
ms.keywords: SetThreadIdealProcessorEx, SetThreadIdealProcessorEx function, base.setthreadidealprocessorex, processthreadsapi/SetThreadIdealProcessorEx, winbase/SetThreadIdealProcessorEx
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
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: Kernel32.dll; KernelBase.dll on Windows Phone 8.1
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadIdealProcessorEx
 - processthreadsapi/SetThreadIdealProcessorEx
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
 - KernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SetThreadIdealProcessorEx
---

# SetThreadIdealProcessorEx function


## -description

Sets the ideal processor for the specified thread and optionally retrieves the previous ideal processor.

## -parameters

### -param hThread [in]

A handle to the thread for which to set the ideal processor. This handle must have been created with the THREAD_SET_INFORMATION access right. For more information, see <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param lpIdealProcessor [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a> structure that specifies the processor number of the desired ideal processor.

### -param lpPreviousIdealProcessor [out, optional]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a> structure to receive the previous ideal processor. This parameter can point to the same memory location as the <i>lpIdealProcessor</i> parameter. This parameter can be NULL if the previous ideal processor is not required.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero. To get extended error information, use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Specifying a thread ideal processor provides a hint to the scheduler about the preferred processor for a thread. The scheduler runs the thread on the thread's ideal processor when possible. 

Starting with Windows 11 and Windows Server 2022, on a system with more than 64 processors, process and thread affinities span all processors in the system, across all <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a>, by default.
The <b>SetThreadIdealProcessorEx</b>, in setting the preferred processor, also sets the thread's primary group to the group of the preferred processor.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex">GetThreadIdealProcessorEx</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor">SetThreadIdealProcessor</a>
