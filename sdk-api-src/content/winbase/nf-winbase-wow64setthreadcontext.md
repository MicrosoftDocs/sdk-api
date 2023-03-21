---
UID: NF:winbase.Wow64SetThreadContext
title: Wow64SetThreadContext function (winbase.h)
description: Sets the context of the specified WOW64 thread.
helpviewer_keywords: ["Wow64SetThreadContext","Wow64SetThreadContext function","base.wow64setthreadcontext","winbase/Wow64SetThreadContext"]
old-location: base\wow64setthreadcontext.htm
tech.root: Debug
ms.assetid: 4119c945-b654-4634-a88b-e41bc762018a
ms.date: 12/05/2018
ms.keywords: Wow64SetThreadContext, Wow64SetThreadContext function, base.wow64setthreadcontext, winbase/Wow64SetThreadContext
f1_keywords:
- winbase/Wow64SetThreadContext
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
- Wow64SetThreadContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Wow64SetThreadContext function


## -description


Sets the context of the specified WOW64 thread.


## -parameters




### -param hThread [in]

A handle to the thread whose context is to be set.


### -param lpContext [in]

A <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a> structure. The caller must 
      initialize the <b>ContextFlags</b> member of this structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function allows the selective context to be set based on the value of the 
    <b>ContextFlags</b> member of the context structure. The thread handle identified by the 
    <i>hThread</i> parameter is typically being debugged, but the function can also operate even 
    when it is not being debugged.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and 
    set the last error code to <b>ERROR_INVALID_FUNCTION</b>. A 32-bit application can call this 
    function on a WOW64 thread; the result is the same as calling the 
    <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a> function.

Do not try to set the context for a running thread; the results are unpredictable. Use the 
    <a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64suspendthread">Wow64SuspendThread</a> function to suspend the thread 
    before calling <b>Wow64SetThreadContext</b>.




## -see-also




<a href="/windows/desktop/Debug/debugging-functions">Debugging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getxstatefeaturesmask">GetXStateFeaturesMask</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a>



<a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a>



<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64getthreadcontext.md">Wow64GetThreadContext</a>
 

 