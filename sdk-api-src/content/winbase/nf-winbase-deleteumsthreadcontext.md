---
UID: NF:winbase.DeleteUmsThreadContext
title: DeleteUmsThreadContext function (winbase.h)
description: Deletes the specified user-mode scheduling (UMS) thread context. The thread must be terminated.
old-location: base\deleteumsthreadcontext.htm
tech.root: ProcThread
ms.assetid: cdd118fc-f664-44ce-958d-857216ceb9a7
ms.date: 12/05/2018
ms.keywords: DeleteUmsThreadContext, DeleteUmsThreadContext function, base.deleteumsthreadcontext, winbase/DeleteUmsThreadContext
ms.topic: function
f1_keywords:
- winbase/DeleteUmsThreadContext
dev_langs:
- c++
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-ums-l1-1-0.dll
api_name:
- DeleteUmsThreadContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteUmsThreadContext function


## -description


Deletes  the specified user-mode scheduling (UMS) thread context. The thread must be terminated. 


## -parameters




### -param UmsThread [in]

A pointer to the UMS thread context to be deleted. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createumsthreadcontext">CreateUmsThreadContext</a> function provides this pointer.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



A UMS thread context cannot be deleted until the associated thread has terminated. 

When a UMS worker thread finishes running (for example, by returning from its thread entry point function),   the system terminates the thread,  sets the  termination status in the thread's UMS thread context, and queues the UMS thread context to the associated completion list.

 Any attempt to execute the  UMS thread will fail because the thread is already terminated. 

To check the termination status of a thread, the application's scheduler should call <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-queryumsthreadinformation">QueryUmsThreadInformation</a> with the <b>UmsIsThreadTerminated</b> information class. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createumsthreadcontext">CreateUmsThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-queryumsthreadinformation">QueryUmsThreadInformation</a>
 

 

