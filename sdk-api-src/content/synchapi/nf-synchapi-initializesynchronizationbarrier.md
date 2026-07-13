---
UID: NF:synchapi.InitializeSynchronizationBarrier
title: InitializeSynchronizationBarrier function (synchapi.h)
description: Initializes a new synchronization barrier.
helpviewer_keywords: ["InitializeSynchronizationBarrier","InitializeSynchronizationBarrier function","base.initializesynchronizationbarrier","synchapi/InitializeSynchronizationBarrier"]
old-location: base\initializesynchronizationbarrier.htm
tech.root: base
ms.assetid: f69934a1-ee1f-4400-ae3e-cb9a19feff93
ms.date: 02/05/2024
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
 - vertdll.dll
api_name:
 - InitializeSynchronizationBarrier
---

# InitializeSynchronizationBarrier function

## -description

Initializes a new synchronization barrier.

## -parameters

### -param lpBarrier [out]

A pointer to the **SYNCHRONIZATION_BARRIER** structure to initialize. This is an opaque structure that should not be modified by applications.

### -param lTotalThreads [in]

The maximum number of threads that can enter this barrier. After the maximum number of threads have entered the barrier, all threads continue.

### -param lSpinCount [in]

The number of times an individual thread should spin while waiting for other threads to arrive at the barrier. If this parameter is `-1`, the thread spins 2000 times. If the thread exceeds *lSpinCount*, the thread blocks unless it called [EnterSynchronizationBarrier](nf-synchapi-entersynchronizationbarrier.md) with **SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY**.

## -returns

`TRUE` if the barrier was successfully initialized. If the barrier was not successfully initialized, this function returns `FALSE`. Use [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) to get extended error information.

## -see-also

[DeleteSynchronizationBarrier](nf-synchapi-deletesynchronizationbarrier.md)

[EnterSynchronizationBarrier](nf-synchapi-entersynchronizationbarrier.md)

[Synchronization Barriers](/windows/win32/Sync/synchronization-barriers)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
