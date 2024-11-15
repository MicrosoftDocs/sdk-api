---
UID: NF:processthreadsapi.GetThreadContext
title: GetThreadContext function (processthreadsapi.h)
description: Retrieves the context of the specified thread.
helpviewer_keywords: ["GetThreadContext","GetThreadContext function","_win32_getthreadcontext","base.getthreadcontext","processthreadsapi/GetThreadContext"]
old-location: base\getthreadcontext.htm
tech.root: processthreadsapi
ms.assetid: 3b65283e-34d2-4374-87fe-fa8ae45fbbcf
ms.date: 12/05/2018
ms.keywords: GetThreadContext, GetThreadContext function, _win32_getthreadcontext, base.getthreadcontext, processthreadsapi/GetThreadContext
req.header: processthreadsapi.h
req.include-header: Windows.h
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
 - GetThreadContext
 - processthreadsapi/GetThreadContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetThreadContext
---

# GetThreadContext function


## -description

Retrieves the context of the specified thread.

A 64-bit application can retrieve the context of a WOW64 thread using the [Wow64GetThreadContext](../winbase/nf-winbase-wow64getthreadcontext.md).

## -parameters

### -param hThread [in]

A handle to the thread whose context is to be retrieved. The handle must have **THREAD_GET_CONTEXT** access to the thread. For more information, see [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).
      

**Windows XP or Windows Server 2003:** The handle must also have **THREAD_QUERY_INFORMATION** access.

### -param lpContext [in, out]

A pointer to a [CONTEXT](../winnt/ns-winnt-context.md) structure (such as [ARM64_NT_CONTEXT](../winnt/ns-winnt-arm64_nt_context.md)) that receives the appropriate context of the specified thread. The value of the **ContextFlags** member of this structure specifies which portions of a thread's context are retrieved. The       **CONTEXT** structure is highly processor specific. Refer to the WinNT.h header file for processor-specific definitions of this structures and any alignment requirements.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

This function is used to retrieve the thread context of the specified thread. The function retrieves a selective context based on the value of the **ContextFlags** member of the context structure. The thread identified by the *hThread* parameter is typically being debugged, but the function can also operate when the thread is not being debugged.

You cannot get a valid context for a running thread. Use the [SuspendThread](../processthreadsapi/nf-processthreadsapi-suspendthread.md) function to suspend the thread before calling **GetThreadContext**.

If you call **GetThreadContext** for the current thread, the function returns successfully; however, the context returned is not valid.

## -see-also

- [CONTEXT](../winnt/ns-winnt-context.md)
- [ARM64_NT_CONTEXT](../winnt/ns-winnt-arm64_nt_context.md)
- [Debugging Functions](/windows/desktop/Debug/debugging-functions)
- [GetXStateFeaturesMask](../winbase/nf-winbase-getxstatefeaturesmask.md)
- [SetThreadContext](../processthreadsapi/nf-processthreadsapi-setthreadcontext.md)
- [SuspendThread](../processthreadsapi/nf-processthreadsapi-suspendthread.md)
- [Wow64GetThreadContext](../wow64apiset/nf-wow64apiset-wow64getthreadcontext.md)
