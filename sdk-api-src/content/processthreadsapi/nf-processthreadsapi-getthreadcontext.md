---
UID: NF:processthreadsapi.GetThreadContext
title: GetThreadContext function
author: windows-sdk-content
description: Retrieves the context of the specified thread.
old-location: base\getthreadcontext.htm
tech.root: debug
ms.assetid: 3b65283e-34d2-4374-87fe-fa8ae45fbbcf
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetThreadContext, GetThreadContext function, _win32_getthreadcontext, base.getthreadcontext, processthreadsapi/GetThreadContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThreadContext function


## -description


Retrieves the context of the specified thread.

A 64-bit application can retrieve the context of a WOW64 thread using the 
    <a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a> function.


## -parameters




### -param hThread [in]

A handle to the thread whose context is to be retrieved. The handle must have 
      <b>THREAD_GET_CONTEXT</b> access to the thread. For more information, see 
      <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.
      

<b>WOW64:  </b>The handle must also have <b>THREAD_QUERY_INFORMATION</b> access.


### -param lpContext [in, out]

A pointer to a <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure that receives the 
      appropriate context of the specified thread. The value of the <b>ContextFlags</b> member of 
      this structure specifies which portions of a thread's context are retrieved. The 
      <b>CONTEXT</b> structure is highly processor specific. Refer to 
      the WinNT.h header file for processor-specific definitions of this structures and any alignment 
      requirements.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function is used to retrieve the thread context of the specified thread. The function retrieves a 
    selective context based on the value of the <b>ContextFlags</b> member of the 
    context structure. The thread identified by the <i>hThread</i> parameter is typically being 
    debugged, but the function can also operate when the thread is not being debugged.

You cannot get a valid context for a running thread. Use the 
    <a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a> function to suspend the thread before 
    calling <b>GetThreadContext</b>.

If you call <b>GetThreadContext</b> for the current 
    thread, the function returns successfully; however, the context returned is not valid.




## -see-also




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/95a838a2-f138-4682-b733-3f363b6c4a4b">Debugging Functions</a>



<a href="https://msdn.microsoft.com/D9A8D0B6-21E3-46B7-AB88-CE2FF4025A17">GetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>



<a href="https://msdn.microsoft.com/1332abcb-3356-4890-a03c-843358c1a3ce">SuspendThread</a>



<a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a>
 

 

