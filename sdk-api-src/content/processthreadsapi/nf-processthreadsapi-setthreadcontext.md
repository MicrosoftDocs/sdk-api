---
UID: NF:processthreadsapi.SetThreadContext
title: SetThreadContext function
author: windows-sdk-content
description: Sets the context for the specified thread.
old-location: base\setthreadcontext.htm
tech.root: debug
ms.assetid: be134953-b569-48ea-80ac-ab14dee24500
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: SetThreadContext, SetThreadContext function, _win32_setthreadcontext, base.setthreadcontext, processthreadsapi/SetThreadContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SetThreadContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadContext function


## -description


Sets the context for the specified thread.

A 64-bit application can set the context of a WOW64 thread using the 
    <a href="https://msdn.microsoft.com/4119c945-b654-4634-a88b-e41bc762018a">Wow64SetThreadContext</a> function.


## -parameters




### -param hThread [in]

A handle to the thread whose context is to be set. The handle must have the 
      <b>THREAD_SET_CONTEXT</b> access right to the thread. For more information, see 
      <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.
     


### -param lpContext [in]

A pointer to a <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure that contains the 
      context to be set in the specified thread. The value of the <b>ContextFlags</b> member of 
      this structure specifies which portions of a thread's context to set. Some values in the 
      <b>CONTEXT</b> structure that cannot be specified are silently 
      set to the correct value. This includes bits in the CPU status register that specify the privileged processor 
      mode, global enabling bits in the debugging register, and other states that must be controlled by the operating 
      system.


## -returns



If the context was set, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function sets the thread context based on the value of the <b>ContextFlags</b> member 
    of the context structure. The thread identified by the <i>hThread</i> parameter is typically 
    being debugged, but the function can also operate even when the thread is not being debugged.

Do not try to set the context for a running thread; the results are unpredictable. Use the 
    <a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a> function to suspend the thread before 
    calling <b>SetThreadContext</b>.




## -see-also




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/3b65283e-34d2-4374-87fe-fa8ae45fbbcf">GetThreadContext</a>



<a href="https://msdn.microsoft.com/D9A8D0B6-21E3-46B7-AB88-CE2FF4025A17">GetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a>
 

 

