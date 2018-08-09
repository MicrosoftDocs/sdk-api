---
UID: NF:threadpoolapiset.DisassociateCurrentThreadFromCallback
title: DisassociateCurrentThreadFromCallback function
author: windows-sdk-content
description: Removes the association between the currently executing callback function and the object that initiated the callback. The current thread will no longer count as executing a callback on behalf of the object.
old-location: base\disassociatecurrentthreadfromcallback.htm
old-project: procthread
ms.assetid: f25f936c-2570-4e8c-807b-42000cd878bb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DisassociateCurrentThreadFromCallback, DisassociateCurrentThreadFromCallback function, base.disassociatecurrentthreadfromcallback, threadpoolapiset/DisassociateCurrentThreadFromCallback, winbase/DisassociateCurrentThreadFromCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: TS_TEXTCHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - DisassociateCurrentThreadFromCallback
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# DisassociateCurrentThreadFromCallback function


## -description


Removes the association between the currently executing callback function and the object that initiated the callback.  The current thread will no longer count as executing a callback on behalf of the object.


## -parameters




### -param pci [in, out]

A <b>TP_CALLBACK_INSTANCE</b> structure that defines the callback instance. The structure is passed to the callback function.


## -returns



This function does not return a value.




## -remarks



If this is the last thread executing a callback on behalf of the object, any threads waiting for the object's callbacks to complete will be released.

The thread remains associated with the object's <a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">cleanup group</a> until the thread returns to the thread pool. This lets DLL shutdown routines safely synchronize with outstanding callbacks and proceed with unloading the DLL's code when all callbacks have completed.

The callback-generating object remains valid for the duration of the callback. The callback object may be reused or released (although synchronization with cleanup group release is still required).

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/59364b91-d78b-46e2-b298-42f77e712577">CallbackMayRunLong</a>



<a href="https://msdn.microsoft.com/a29ba988-5d66-4914-9e37-a229bce75af2">FreeLibraryWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/43ce27ee-207c-4317-9771-d82f1f4edda2">LeaveCriticalSectionWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/0e82c041-8191-477d-8a2e-819b8920bbc8">ReleaseMutexWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/d5c8d6a0-6bb1-4ecb-aaba-665d81cb3d14">ReleaseSemaphoreWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/50e127bc-d518-4f84-88ea-b262572d5248">SetEventWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/689d197e-195f-419c-9317-b30c614038c4">TrySubmitThreadpoolCallback</a>
 

 

