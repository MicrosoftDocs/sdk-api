---
UID: NF:wow64apiset.Wow64SetThreadContext
title: Wow64SetThreadContext
ms.date: 11/18/2022
targetos: Windows
description: Sets the thread context.
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
 - Wow64SetThreadContext
f1_keywords:
 - Wow64SetThreadContext
 - wow64apiset/Wow64SetThreadContext
dev_langs:
 - c++
helpviewer_keywords:
 - Wow64SetThreadContext
---

# Wow64SetThreadContext function

## -description

Sets the context of the specified WOW64 thread.

## -parameters

### -param hThread [in]

A handle to the thread whose context is to be set.

### -param lpContext [in]

A <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a> structure. The caller must initialize the **ContextFlags** member of this structure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function allows the selective context to be set based on the value of the **ContextFlags** member of the context structure. The thread handle identified by the <i>hThread</i> parameter is typically being debugged, but the function can also operate even when it is not being debugged.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and set the last error code to **ERROR_INVALID_FUNCTION**. A 32-bit application can call this function on a WOW64 thread; the result is the same as calling the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a> function.

Do not try to set the context for a running thread; the results are unpredictable. Use the <a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64suspendthread">Wow64SuspendThread</a> function to suspend the thread before calling **Wow64SetThreadContext**.

## -see-also

<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>

<a href="/windows/desktop/api/winbase/nf-winbase-getxstatefeaturesmask">GetXStateFeaturesMask</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>

<a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a>

<a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a>

<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64getthreadcontext.md">Wow64GetThreadContext</a>
