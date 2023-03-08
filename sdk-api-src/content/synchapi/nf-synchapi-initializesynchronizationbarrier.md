---
UID: NF:synchapi.InitializeSynchronizationBarrier
title: InitializeSynchronizationBarrier function (synchapi.h)
description: Initializes a new synchronization barrier.
helpviewer_keywords: ["InitializeSynchronizationBarrier","InitializeSynchronizationBarrier function","base.initializesynchronizationbarrier","synchapi/InitializeSynchronizationBarrier"]
old-location: base\initializesynchronizationbarrier.htm
tech.root: base
ms.assetid: f69934a1-ee1f-4400-ae3e-cb9a19feff93
ms.date: 12/05/2018
ms.keywords: InitializeSynchronizationBarrier, InitializeSynchronizationBarrier function, base.initializesynchronizationbarrier, synchapi/InitializeSynchronizationBarrier
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeSynchronizationBarrier
 - synchapi/InitializeSynchronizationBarrier
dev_langs:
 - c++
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
      <a href="/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier">EnterSynchronizationBarrier</a> with 
      <b>SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY</b>.

## -returns

<b>TRUE </b> if the barrier was successfully initialized. If the barrier was not 
      successfully initialized, this function returns <b>FALSE</b>. Use 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-deletesynchronizationbarrier">DeleteSynchronizationBarrier</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier">EnterSynchronizationBarrier</a>



<a href="/windows/desktop/Sync/synchronization-barriers">Synchronization Barriers</a>