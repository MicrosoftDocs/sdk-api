---
UID: NF:synchapi.LeaveCriticalSection
title: LeaveCriticalSection function (synchapi.h)
description: Releases ownership of the specified critical section object.
helpviewer_keywords: ["LeaveCriticalSection","LeaveCriticalSection function","_win32_leavecriticalsection","base.leavecriticalsection","synchapi/LeaveCriticalSection","winbase/LeaveCriticalSection"]
old-location: base\leavecriticalsection.htm
tech.root: backup
ms.assetid: cf740e1d-351f-478c-bdbb-4a776b84acc5
ms.date: 12/05/2018
ms.keywords: LeaveCriticalSection, LeaveCriticalSection function, _win32_leavecriticalsection, base.leavecriticalsection, synchapi/LeaveCriticalSection, winbase/LeaveCriticalSection
f1_keywords:
- synchapi/LeaveCriticalSection
dev_langs:
- c++
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
- vertdll.dll
api_name:
- LeaveCriticalSection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LeaveCriticalSection function


## -description


Releases ownership of the specified critical section object.


## -parameters




### -param lpCriticalSection [in, out]

A pointer to the critical section object.


## -remarks



The threads of a single process can use a critical-section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical-section object, which it can do by declaring a variable of type <b>CRITICAL_SECTION</b>. Before using a critical section, some thread of the process must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection">InitializeCriticalSection</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount">InitializeCriticalSectionAndSpinCount</a> function to initialize the object.

A thread uses the 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection">EnterCriticalSection</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-tryentercriticalsection">TryEnterCriticalSection</a> function to acquire ownership of a critical section object. To release its ownership, the thread must call 
<b>LeaveCriticalSection</b> once for each time that it entered the critical section.

If a thread calls 
<b>LeaveCriticalSection</b> when it does not have ownership of the specified critical section object, an error occurs that may cause another thread using 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection">EnterCriticalSection</a> to wait indefinitely.

Any thread of the process can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection">DeleteCriticalSection</a> function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.


#### Examples

For an example that uses 
<b>LeaveCriticalSection</b>, see 
<a href="https://docs.microsoft.com/windows/desktop/Sync/using-critical-section-objects">Using Critical Section Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/critical-section-objects">Critical Section Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection">DeleteCriticalSection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection">EnterCriticalSection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection">InitializeCriticalSection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsectionandspincount">InitializeCriticalSectionAndSpinCount</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-tryentercriticalsection">TryEnterCriticalSection</a>
 

 

