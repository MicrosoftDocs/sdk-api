---
UID: NF:processthreadsapi.TerminateProcess
title: TerminateProcess function (processthreadsapi.h)
description: Terminates the specified process and all of its threads.
helpviewer_keywords: ["TerminateProcess","TerminateProcess function","_win32_terminateprocess","base.terminateprocess","processthreadsapi/TerminateProcess","winbase/TerminateProcess"]
old-location: base\terminateprocess.htm
tech.root: processthreadsapi
ms.assetid: 0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a
ms.date: 02/02/2024
ms.keywords: TerminateProcess, TerminateProcess function, _win32_terminateprocess, base.terminateprocess, processthreadsapi/TerminateProcess, winbase/TerminateProcess
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
 - TerminateProcess
 - processthreadsapi/TerminateProcess
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - Vertdll.dll
api_name:
 - TerminateProcess
---

# TerminateProcess function

## -description

Terminates the specified process and all of its threads.

## -parameters

### -param hProcess [in]

A handle to the process to be terminated.

The handle must have the <b>PROCESS_TERMINATE</b> access right. For more information, see <a href="/windows/win32/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param uExitCode [in]

The exit code to be used by the process and threads terminated as a result of this call. Use the <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a> function to retrieve a process's exit value. Use the <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread">GetExitCodeThread</a> function to retrieve a thread's exit value.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>TerminateProcess</b> function is used to unconditionally cause a process to exit. The state of global data maintained by dynamic-link libraries (DLLs) may be compromised if <b>TerminateProcess</b> is used rather than <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess">ExitProcess</a>.

This function stops execution of all threads within the process and requests cancellation of all pending I/O. The terminated process cannot exit until all pending I/O has been completed or canceled. When a process terminates, its kernel object is not destroyed until all processes that have open handles to the process have released those handles.

When a process terminates itself, <b>TerminateProcess</b> stops execution of the calling thread and does not return. Otherwise, <b>TerminateProcess</b> is asynchronous; it initiates termination and returns immediately. If you need to be sure the process has terminated, call the <a href="/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a> function with a handle to the process.

A process cannot prevent itself from being terminated.

After a process has terminated, call to <b>TerminateProcess</b> with open handles to the process fails with <b>ERROR_ACCESS_DENIED</b> (5) error code.

## -see-also

[ExitProcess](nf-processthreadsapi-exitprocess.md)

[GetExitCodeProcess](nf-processthreadsapi-getexitcodeprocess.md)

[GetExitCodeThread](nf-processthreadsapi-getexitcodethread.md)

[OpenProcess](nf-processthreadsapi-openprocess.md)

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Processes](/windows/win32/ProcThread/child-processes)

[Terminating a Process](/windows/win32/ProcThread/terminating-a-process)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
