---
UID: NF:synchapi.LeaveCriticalSection
title: LeaveCriticalSection function
author: windows-sdk-content
description: Releases ownership of the specified critical section object.
old-location: base\leavecriticalsection.htm
old-project: Sync
ms.assetid: cf740e1d-351f-478c-bdbb-4a776b84acc5
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: LeaveCriticalSection, LeaveCriticalSection function, _win32_leavecriticalsection, base.leavecriticalsection, synchapi/LeaveCriticalSection, winbase/LeaveCriticalSection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: synchapi.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ITEMPROP, *LPITEMPROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Synch-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Synch-l1-2-0.dll
-	API-MS-Win-Core-Synch-l1-2-1.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	LeaveCriticalSection
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# LeaveCriticalSection function


## -description


Releases ownership of the specified critical section object.


## -parameters




### -param lpCriticalSection [in, out]

A pointer to the critical section object.


## -returns



This function does not return a value.




## -remarks



The threads of a single process can use a critical-section object for mutual-exclusion synchronization. The process is responsible for allocating the memory used by a critical-section object, which it can do by declaring a variable of type <b>CRITICAL_SECTION</b>. Before using a critical section, some thread of the process must call the 
<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a> or 
<a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a> function to initialize the object.

A thread uses the 
<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a> or 
<a href="https://msdn.microsoft.com/5225bda1-6e20-4f6b-9f9b-633c62acfdce">TryEnterCriticalSection</a> function to acquire ownership of a critical section object. To release its ownership, the thread must call 
<b>LeaveCriticalSection</b> once for each time that it entered the critical section.

If a thread calls 
<b>LeaveCriticalSection</b> when it does not have ownership of the specified critical section object, an error occurs that may cause another thread using 
<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a> to wait indefinitely.

Any thread of the process can use the 
<a href="https://msdn.microsoft.com/97e29fc3-b155-448e-aaa9-19f0fc2d841e">DeleteCriticalSection</a> function to release the system resources that were allocated when the critical section object was initialized. After this function has been called, the critical section object can no longer be used for synchronization.


#### Examples

For an example that uses 
<b>LeaveCriticalSection</b>, see 
<a href="https://msdn.microsoft.com/3c96414b-97e7-4ebb-a629-bfdb7a77c576">Using Critical Section Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2ec11a42-3d12-4d60-9dd7-dc38926d56e1">Critical Section Objects</a>



<a href="https://msdn.microsoft.com/97e29fc3-b155-448e-aaa9-19f0fc2d841e">DeleteCriticalSection</a>



<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a>



<a href="https://msdn.microsoft.com/ad4b182d-a65d-4890-9eda-fdd6d044f736">InitializeCriticalSection</a>



<a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/5225bda1-6e20-4f6b-9f9b-633c62acfdce">TryEnterCriticalSection</a>
 

 

