---
UID: NF:winbase.Wow64GetThreadContext
title: Wow64GetThreadContext function (winbase.h)
description: Retrieves the context of the specified WOW64 thread.
helpviewer_keywords: ["Wow64GetThreadContext","Wow64GetThreadContext function","base.wow64getthreadcontext","winbase/Wow64GetThreadContext"]
old-location: base\wow64getthreadcontext.htm
tech.root: Debug
ms.assetid: 1bac28e1-3558-43c4-97e4-d8bb9514c38e
ms.date: 07/09/2024
ms.keywords: Wow64GetThreadContext, Wow64GetThreadContext function, base.wow64getthreadcontext, winbase/Wow64GetThreadContext
f1_keywords:
- winbase/Wow64GetThreadContext
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
api_name:
- Wow64GetThreadContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Wow64GetThreadContext function


## -description


Retrieves the context of the specified WOW64 thread.


## -parameters




### -param hThread [in]

A handle to the thread whose context is to be retrieved. The handle must have <b>THREAD_GET_CONTEXT</b> access to the thread. For more information, see <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.


### -param lpContext [in, out]

A <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a> structure. The caller must initialize the <b>ContextFlags</b> member of this structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function is used to retrieve the thread context of the specified thread. The function retrieves a selective context based on the value of the <b>ContextFlags</b> member of the context structure. The thread identified by the <i>hThread</i> parameter is typically being debugged, but the function can also operate when the thread is not being debugged.

You cannot get a valid context for a running thread. Use the <a href="/windows/desktop/api/winbase/nf-winbase-wow64suspendthread">Wow64SuspendThread</a> function to suspend the thread before calling <b>Wow64GetThreadContext</b>.

If you call <b>Wow64GetThreadContext</b> for the current thread, the function returns successfully; however, the context returned is not valid.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and set the last error code to <b>ERROR_INVALID_FUNCTION</b>. A 32-bit application can call this function on a WOW64 thread; the result is the same as calling the [GetThreadContext function](../processthreadsapi/nf-processthreadsapi-getthreadcontext.md) function.




## -see-also




<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



[GetThreadContext function](../processthreadsapi/nf-processthreadsapi-getthreadcontext.md)


<a href="/windows/desktop/api/winbase/nf-winbase-getxstatefeaturesmask">GetXStateFeaturesMask</a>



<a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a>



<a href="/windows/win32/api/wow64apiset/">Wow64SetThreadContext</a>
 

 