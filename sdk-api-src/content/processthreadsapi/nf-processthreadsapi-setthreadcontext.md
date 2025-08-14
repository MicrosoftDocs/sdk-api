---
UID: NF:processthreadsapi.SetThreadContext
title: SetThreadContext function (processthreadsapi.h)
description: Sets the context for the specified thread.
helpviewer_keywords: ["SetThreadContext","SetThreadContext function","_win32_setthreadcontext","base.setthreadcontext","processthreadsapi/SetThreadContext"]
old-location: base\setthreadcontext.htm
tech.root: processthreadsapi
ms.assetid: be134953-b569-48ea-80ac-ab14dee24500
ms.date: 06/13/2025
ms.keywords: SetThreadContext, SetThreadContext function, _win32_setthreadcontext, base.setthreadcontext, processthreadsapi/SetThreadContext
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadContext
 - processthreadsapi/SetThreadContext
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
api_name:
 - SetThreadContext
---

# SetThreadContext function

## -description

Sets the context for the specified thread.

> [!NOTE]
> A 64-bit application can set the context of a WOW64 thread using the [Wow64SetThreadContext function](../wow64apiset/nf-wow64apiset-wow64setthreadcontext.md).

## -parameters

### -param hThread [in]

A handle to the thread whose context is to be set. The handle must have the **THREAD_SET_CONTEXT** access right to the thread. For more information, see <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param lpContext [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that contains the context to be set in the specified thread. The value of the **ContextFlags** member of this structure specifies which portions of a thread's context to set. Some values in the **CONTEXT** structure that cannot be specified are silently set to the correct value. This includes bits in the CPU status register that specify the privileged processor mode, global enabling bits in the debugging register, and other states that must be controlled by the operating system.

## -returns

If the context was set, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The function sets the thread context based on the value of the **ContextFlags** member of the context structure. The thread identified by the *hThread* parameter is typically being debugged, but the function can also operate even when the thread is not being debugged.

Do not try to set the context for a running thread; the results are unpredictable. Use the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread">SuspendThread</a> function to suspend the thread before calling **SetThreadContext**.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>

<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>

<a href="/windows/desktop/api/winbase/nf-winbase-getxstatefeaturesmask">GetXStateFeaturesMask</a>

<a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread">SuspendThread</a>
