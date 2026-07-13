---
UID: NF:processthreadsapi.GetCurrentProcess
title: GetCurrentProcess function (processthreadsapi.h)
description: Retrieves a pseudo handle for the current process.
helpviewer_keywords: ["GetCurrentProcess","GetCurrentProcess function","_win32_getcurrentprocess","base.getcurrentprocess","processthreadsapi/GetCurrentProcess","winbase/GetCurrentProcess"]
old-location: base\getcurrentprocess.htm
tech.root: processthreadsapi
ms.assetid: 0471790c-3bb9-4180-8676-941e655b1812
ms.date: 02/02/2024
ms.keywords: GetCurrentProcess, GetCurrentProcess function, _win32_getcurrentprocess, base.getcurrentprocess, processthreadsapi/GetCurrentProcess, winbase/GetCurrentProcess
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
 - GetCurrentProcess
 - processthreadsapi/GetCurrentProcess
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
 - GetCurrentProcess
---

# GetCurrentProcess function

## -description

Retrieves a pseudo handle for the current process.

## -returns

The return value is a pseudo handle to the current process.

## -remarks

A pseudo handle is a special constant, currently (<b>HANDLE</b>)-1, that is interpreted as the current process handle. For compatibility with future operating systems, it is best to call <b>GetCurrentProcess</b> instead of hard-coding this constant value. The calling process can use a pseudo handle to specify its own process whenever a process handle is required. Pseudo handles are not inherited by child processes.

This handle has the <b>PROCESS_ALL_ACCESS</b> access right to the process object. For more information, see <a href="/windows/win32/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP: </b>This handle has the maximum access allowed by the security descriptor of the process to the primary token of the process.

A process can create a "real" handle to itself that is valid in the context of other processes, or that can be inherited by other processes, by specifying the pseudo handle as the source handle in a call to the <a href="/windows/win32/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function. A process can also use the <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess">OpenProcess</a> function to open a real handle to itself.

The pseudo handle need not be closed when it is no longer needed. Calling the <a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function with a pseudo handle has no effect. If the pseudo handle is duplicated by <a href="/windows/win32/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>, the duplicate handle must be closed.

#### Examples

For an example, see <a href="/windows/win32/ProcThread/creating-a-child-process-with-redirected-input-and-output">Creating a Child Process with Redirected Input and Output</a>.

## -see-also

[CloseHandle](../handleapi/nf-handleapi-closehandle.md)

[DuplicateHandle](../handleapi/nf-handleapi-duplicatehandle.md)

[GetCurrentProcessId](nf-processthreadsapi-getcurrentprocessid.md)

[GetCurrentThread](nf-processthreadsapi-getcurrentthread.md)

[OpenProcess](nf-processthreadsapi-openprocess.md)

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Processes](/windows/win32/ProcThread/child-processes)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
