---
UID: NF:winbase.DeleteUmsThreadContext
title: DeleteUmsThreadContext function
author: windows-driver-content
description: Deletes the specified user-mode scheduling (UMS) thread context. The thread must be terminated.
old-location: base\deleteumsthreadcontext.htm
old-project: ProcThread
ms.assetid: cdd118fc-f664-44ce-958d-857216ceb9a7
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: DeleteUmsThreadContext, DeleteUmsThreadContext function, base.deleteumsthreadcontext, winbase/DeleteUmsThreadContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-ums-l1-1-0.dll
api_name:
-	DeleteUmsThreadContext
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DeleteUmsThreadContext function


## -description


Deletes  the specified user-mode scheduling (UMS) thread context. The thread must be terminated. 


## -parameters




### -param UmsThread [in]

A pointer to the UMS thread context to be deleted. The <a href="https://msdn.microsoft.com/b27ce81a-8463-46af-8acf-2de091f625df">CreateUmsThreadContext</a> function provides this pointer.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



A UMS thread context cannot be deleted until the associated thread has terminated. 

When a UMS worker thread finishes running (for example, by returning from its thread entry point function),   the system terminates the thread,  sets the  termination status in the thread's UMS thread context, and queues the UMS thread context to the associated completion list.

 Any attempt to execute the  UMS thread will fail because the thread is already terminated. 

To check the termination status of a thread, the application's scheduler should call <a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a> with the <b>UmsIsThreadTerminated</b> information class. 




## -see-also




<a href="https://msdn.microsoft.com/b27ce81a-8463-46af-8acf-2de091f625df">CreateUmsThreadContext</a>



<a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a>
 

 

