---
UID: NF:winbase.Wow64SetThreadContext
title: Wow64SetThreadContext function (winbase.h)
author: windows-sdk-content
description: Sets the context of the specified WOW64 thread.
old-location: base\wow64setthreadcontext.htm
tech.root: Debug
ms.assetid: 4119c945-b654-4634-a88b-e41bc762018a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Wow64SetThreadContext, Wow64SetThreadContext function, base.wow64setthreadcontext, winbase/Wow64SetThreadContext
ms.topic: function
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
product: Windows
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

A <a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">WOW64_CONTEXT</a> structure. The caller must 
      initialize the <b>ContextFlags</b> member of this structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function allows the selective context to be set based on the value of the 
    <b>ContextFlags</b> member of the context structure. The thread handle identified by the 
    <i>hThread</i> parameter is typically being debugged, but the function can also operate even 
    when it is not being debugged.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and 
    set the last error code to <b>ERROR_INVALID_FUNCTION</b>. A 32-bit application can call this 
    function on a WOW64 thread; the result is the same as calling the 
    <a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a> function.

Do not try to set the context for a running thread; the results are unpredictable. Use the 
    <a href="https://msdn.microsoft.com/d976675a-5400-41ac-a11d-c39a1b2dd50d">Wow64SuspendThread</a> function to suspend the thread 
    before calling <b>Wow64SetThreadContext</b>.




## -see-also




<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/D9A8D0B6-21E3-46B7-AB88-CE2FF4025A17">GetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>



<a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">WOW64_CONTEXT</a>



<a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a>
 

 

