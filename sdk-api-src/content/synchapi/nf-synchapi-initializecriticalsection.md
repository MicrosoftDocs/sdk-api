---
UID: NF:synchapi.InitializeCriticalSection
title: InitializeCriticalSection function
author: windows-sdk-content
description: Initializes a critical section object.
old-location: base\initializecriticalsection.htm
tech.root: sync
ms.assetid: ad4b182d-a65d-4890-9eda-fdd6d044f736
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InitializeCriticalSection, InitializeCriticalSection function, _win32_initializecriticalsection, base.initializecriticalsection, synchapi/InitializeCriticalSection, winbase/InitializeCriticalSection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - InitializeCriticalSection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeCriticalSection function


## -description


Initializes a critical section object.


## -parameters




### -param lpCriticalSection [out]

A pointer to the critical section object.


## -returns



This function does not return a value.



<b>Windows Server 2003 and Windows XP:  </b>In low memory situations, 
<b>InitializeCriticalSection</b> can raise a <b>STATUS_NO_MEMORY</b> exception. Starting with Windows Vista, this exception was eliminated and <b>InitializeCriticalSection</b> always succeeds, even in low memory situations.




## -remarks



The threads of a single process can use a critical section object for mutual-exclusion synchronization. There is no guarantee about the order in which threads will obtain ownership of the critical section, however, the system will be fair to all threads.

The process is responsible for allocating the memory used by a critical section object, which it can do by declaring a variable of type <b>CRITICAL_SECTION</b>. Before using a critical section, some thread of the process must initialize the object.

After a critical section object has been initialized, the threads of the process can specify the object in the 
<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a>, 
<a href="https://msdn.microsoft.com/5225bda1-6e20-4f6b-9f9b-633c62acfdce">TryEnterCriticalSection</a>, or 
<a href="https://msdn.microsoft.com/cf740e1d-351f-478c-bdbb-4a776b84acc5">LeaveCriticalSection</a> function to provide mutually exclusive access to a shared resource. For similar synchronization between the threads of different processes, use a mutex object.

A critical section object cannot be moved or copied. The process must also not modify the object, but must treat it as logically opaque. Use only the critical section functions to manage critical section objects. When you have finished using the critical section, call the 
<a href="https://msdn.microsoft.com/97e29fc3-b155-448e-aaa9-19f0fc2d841e">DeleteCriticalSection</a> function.

A critical section object must be deleted before it can be reinitialized. Initializing a critical section that has already been initialized results in undefined behavior.




## -see-also




<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a>



<a href="https://msdn.microsoft.com/2ec11a42-3d12-4d60-9dd7-dc38926d56e1">Critical Section Objects</a>



<a href="https://msdn.microsoft.com/97e29fc3-b155-448e-aaa9-19f0fc2d841e">DeleteCriticalSection</a>



<a href="https://msdn.microsoft.com/bb307b7a-66fc-4d19-b774-deca8bf90492">EnterCriticalSection</a>



<a href="https://msdn.microsoft.com/4b84b305-8bc0-4592-9378-b757bbc0de19">InitializeCriticalSectionAndSpinCount</a>



<a href="https://msdn.microsoft.com/cf740e1d-351f-478c-bdbb-4a776b84acc5">LeaveCriticalSection</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>



<a href="https://msdn.microsoft.com/5225bda1-6e20-4f6b-9f9b-633c62acfdce">TryEnterCriticalSection</a>
 

 

