---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

