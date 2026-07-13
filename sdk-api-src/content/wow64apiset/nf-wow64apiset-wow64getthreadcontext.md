---
UID: NF:wow64apiset.Wow64GetThreadContext
title: Wow64GetThreadContext
ms.date: 11/17/2022
targetos: Windows
description: Retrieves the thread context.
tech.root: fs
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: wow64apiset.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1903
req.target-min-winversvr: Windows Server, version 1903
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-wow64-l1-1-3.dll
 - wow64apiset.h
api_name:
 - Wow64GetThreadContext
f1_keywords:
 - Wow64GetThreadContext
 - wow64apiset/Wow64GetThreadContext
dev_langs:
 - c++
helpviewer_keywords:
 - Wow64GetThreadContext
---

# Wow64GetThreadContext function

## -description

Retrieves the context of the specified WOW64 thread.

## -parameters

### -param hThread [in]

A handle to the thread whose context is to be retrieved. The handle must have **THREAD_GET_CONTEXT** access to the thread. For more information, see <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param lpContext [in, out]

A <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a> structure. The caller must initialize the **ContextFlags** member of this structure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is used to retrieve the thread context of the specified thread. The function retrieves a selective context based on the value of the **ContextFlags** member of the context structure. The thread identified by the <i>hThread</i> parameter is typically being debugged, but the function can also operate when the thread is not being debugged.

You cannot get a valid context for a running thread. Use the <a href="/windows/desktop/api/winbase/nf-winbase-wow64suspendthread">Wow64SuspendThread</a> function to suspend the thread before calling **Wow64GetThreadContext**.

If you call **Wow64GetThreadContext** for the current thread, the function returns successfully; however, the context returned is not valid.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and set the last error code to **ERROR_INVALID_FUNCTION**. A 32-bit application can call this function on a WOW64 thread; the result is the same as calling the [GetThreadContext function](../processthreadsapi/nf-processthreadsapi-getthreadcontext.md) function.

## -see-also

<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>

[GetThreadContext function](../processthreadsapi/nf-processthreadsapi-getthreadcontext.md)

<a href="/windows/desktop/api/winbase/nf-winbase-getxstatefeaturesmask">GetXStateFeaturesMask</a>

<a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a>

<a href="/windows/win32/api/wow64apiset/">Wow64SetThreadContext</a>
