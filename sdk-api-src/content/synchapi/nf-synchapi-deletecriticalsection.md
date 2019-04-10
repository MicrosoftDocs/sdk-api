---
UID: NF:synchapi.DeleteCriticalSection
title: DeleteCriticalSection function (synchapi.h)
author: windows-sdk-content
description: Releases all resources used by an unowned critical section object.
old-location: base\deletecriticalsection.htm
tech.root: Sync
ms.assetid: 97e29fc3-b155-448e-aaa9-19f0fc2d841e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteCriticalSection, DeleteCriticalSection function, _win32_deletecriticalsection, base.deletecriticalsection, synchapi/DeleteCriticalSection, winbase/DeleteCriticalSection
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
 - API-MS-Win-Core-Synch-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - DeleteCriticalSection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteCriticalSection function


## -description


Releases all resources used by an unowned critical section object.


## -parameters




### -param lpCriticalSection [in, out]

A pointer to the critical section object. The object must have been previously initialized with the 
<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a> function.


## -returns



This function does not return a value.




## -remarks



Deleting a critical section object releases all system resources used by the object. The caller is responsible for ensuring that the critical section object is unowned and the specified CRITICAL_SECTION structure is not being accessed by any critical section functions called by other threads in the process.

After a critical section object has been deleted, do not reference the object in any function that operates on critical sections (such as <a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a>, <a href="https://msdn.microsoft.com/5225bda1-6e20-4f6b-9f9b-633c62acfdce">TryEnterCriticalSection</a>, and <a href="https://msdn.microsoft.com/cf740e1d-351f-478c-bdbb-4a776b84acc5">LeaveCriticalSection</a>) other than <a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a> and <a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a>. If you attempt to do so, memory corruption and other unexpected errors can occur.

If a critical section is deleted while it is still owned, the state of the threads waiting for ownership of the deleted critical section is undefined.


#### Examples

For an example that uses 
<b>DeleteCriticalSection</b>, see 
<a href="https://msdn.microsoft.com/3c96414b-97e7-4ebb-a629-bfdb7a77c576">Using Critical Section Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2ec11a42-3d12-4d60-9dd7-dc38926d56e1">Critical Section Objects</a>



<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a>



<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a>



<a href="https://msdn.microsoft.com/cf740e1d-351f-478c-bdbb-4a776b84acc5">LeaveCriticalSection</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/5225bda1-6e20-4f6b-9f9b-633c62acfdce">TryEnterCriticalSection</a>
 

 

