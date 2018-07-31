---
UID: NF:winbase.Wow64GetThreadContext
title: Wow64GetThreadContext function
author: windows-sdk-content
description: Retrieves the context of the specified WOW64 thread.
old-location: base\wow64getthreadcontext.htm
old-project: Debug
ms.assetid: 1bac28e1-3558-43c4-97e4-d8bb9514c38e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Wow64GetThreadContext, Wow64GetThreadContext function, base.wow64getthreadcontext, winbase/Wow64GetThreadContext
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - Wow64GetThreadContext
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# Wow64GetThreadContext function


## -description


Retrieves the context of the specified WOW64 thread.


## -parameters




### -param hThread [in]

A handle to the thread whose context is to be retrieved. The handle must have 
      <b>THREAD_GET_CONTEXT</b> access to the thread. For more information, see 
      <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param lpContext [in, out]

A <a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">WOW64_CONTEXT</a> structure. The caller must 
      initialize the <b>ContextFlags</b> member of this structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is used to retrieve the thread context of the specified thread. The function retrieves a 
    selective context based on the value of the <b>ContextFlags</b> member of the context 
    structure. The thread identified by the <i>hThread</i> parameter is typically being debugged, 
    but the function can also operate when the thread is not being debugged.

You cannot get a valid context for a running thread. Use the 
    <a href="https://msdn.microsoft.com/d976675a-5400-41ac-a11d-c39a1b2dd50d">Wow64SuspendThread</a> function to suspend the thread 
    before calling <b>Wow64GetThreadContext</b>.

If you call <b>Wow64GetThreadContext</b> for the 
    current thread, the function returns successfully; however, the context returned is not valid.

This function is intended for 64-bit applications. It is not supported on 32-bit Windows; such calls fail and 
    set the last error code to <b>ERROR_INVALID_FUNCTION</b>. A 32-bit application can call this 
    function on a WOW64 thread; the result is the same as calling the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff549291">GetThreadContext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549291">GetThreadContext</a>



<a href="https://msdn.microsoft.com/D9A8D0B6-21E3-46B7-AB88-CE2FF4025A17">GetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">WOW64_CONTEXT</a>



<a href="https://msdn.microsoft.com/4119c945-b654-4634-a88b-e41bc762018a">Wow64SetThreadContext</a>
 

 

