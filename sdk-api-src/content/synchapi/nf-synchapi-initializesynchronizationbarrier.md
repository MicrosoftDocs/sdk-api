---
UID: NF:synchapi.InitializeSynchronizationBarrier
title: InitializeSynchronizationBarrier function (synchapi.h)
author: windows-sdk-content
description: Initializes a new synchronization barrier.
old-location: base\initializesynchronizationbarrier.htm
tech.root: Sync
ms.assetid: f69934a1-ee1f-4400-ae3e-cb9a19feff93
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitializeSynchronizationBarrier, InitializeSynchronizationBarrier function, base.initializesynchronizationbarrier, synchapi/InitializeSynchronizationBarrier
ms.topic: function
req.header: synchapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - API-MS-Win-Core-Synch-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Synch-l1-2-1.dll
 - MinKernelBase.dll
api_name:
 - InitializeSynchronizationBarrier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeSynchronizationBarrier function


## -description


Initializes a new synchronization barrier. 


## -parameters




### -param lpBarrier [out]

A pointer to the <b>SYNCHRONIZATION_BARRIER</b> structure to initialize. This is an 
      opaque structure that should not be modified by applications.


### -param lTotalThreads [in]

The maximum number of threads that can enter this barrier. After the maximum number of threads have entered 
      the barrier, all threads continue.


### -param lSpinCount [in]

The number of times an individual thread should spin while waiting for other threads to arrive at the 
      barrier. If this parameter is -1, the thread spins 2000 times. If the thread exceeds 
      <i>lSpinCount</i>, the thread blocks unless it called 
      <a href="https://msdn.microsoft.com/cd938370-b046-4369-931d-5c7c8db7303a">EnterSynchronizationBarrier</a> with 
      <b>SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY</b>.


## -returns



<b>TRUE </b>if the barrier was successfully initialized. If the barrier was not 
      successfully initialized, this function returns <b>FALSE</b>. Use 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to get extended error information.




## -see-also




<a href="https://msdn.microsoft.com/04626b6f-f5f7-4042-9786-7cabd68636ac">DeleteSynchronizationBarrier</a>



<a href="https://msdn.microsoft.com/cd938370-b046-4369-931d-5c7c8db7303a">EnterSynchronizationBarrier</a>



<a href="https://msdn.microsoft.com/3A76E6F7-C38B-4843-9496-36F3C78B700C">Synchronization Barriers</a>
 

 

