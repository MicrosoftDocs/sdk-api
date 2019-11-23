---
UID: NF:processthreadsapi.SetThreadIdealProcessorEx
title: SetThreadIdealProcessorEx function (processthreadsapi.h)

description: Sets the ideal processor for the specified thread and optionally retrieves the previous ideal processor.
old-location: base\setthreadidealprocessorex.htm
tech.root: ProcThread
ms.assetid: 6b599a99-41c5-45c7-8aeb-87d8f34e9e82

ms.date: 12/05/2018
ms.keywords: SetThreadIdealProcessorEx, SetThreadIdealProcessorEx function, base.setthreadidealprocessorex, processthreadsapi/SetThreadIdealProcessorEx, winbase/SetThreadIdealProcessorEx
ms.topic: function
f1_keywords:
- processthreadsapi/SetThreadIdealProcessorEx
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- kernel32.dll
- KernelBase.dll
- API-MS-Win-Core-ProcessThreads-l1-1-1.dll
- MinKernelBase.dll
- API-MS-Win-Core-ProcessThreads-l1-1-2.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
- SetThreadIdealProcessorEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetThreadIdealProcessorEx function


## -description


Sets the ideal processor for the specified thread and optionally retrieves the previous ideal processor.


## -parameters




### -param hThread [in]

A handle to the thread for which to set the ideal processor. This handle must have been created with the THREAD_SET_INFORMATION access right. For more information, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.


### -param lpIdealProcessor [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a> structure that specifies the processor number of the desired ideal processor.


### -param lpPreviousIdealProcessor [out, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a> structure to receive the previous ideal processor. This parameter can point to the same memory location as the <i>lpIdealProcessor</i> parameter. This parameter can be NULL if the previous ideal processor is not required.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero. To get extended error information, use <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Specifying a thread ideal processor provides a hint to the scheduler about the preferred processor for a thread. The scheduler runs the thread on the thread's ideal processor when possible. 

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later.

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex">GetThreadIdealProcessorEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor">SetThreadIdealProcessor</a>
 

 

