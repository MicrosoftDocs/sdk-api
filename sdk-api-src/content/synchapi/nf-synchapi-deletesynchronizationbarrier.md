---
UID: NF:synchapi.DeleteSynchronizationBarrier
title: DeleteSynchronizationBarrier function (synchapi.h)
description: Deletes a synchronization barrier.
helpviewer_keywords: ["DeleteSynchronizationBarrier","DeleteSynchronizationBarrier function","base.deletesynchronizationbarrier","synchapi/DeleteSynchronizationBarrier"]
old-location: base\deletesynchronizationbarrier.htm
tech.root: base
ms.assetid: 04626b6f-f5f7-4042-9786-7cabd68636ac
ms.date: 02/05/2024
ms.keywords: DeleteSynchronizationBarrier, DeleteSynchronizationBarrier function, base.deletesynchronizationbarrier, synchapi/DeleteSynchronizationBarrier
req.header: synchapi.h
req.include-header: 
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
 - DeleteSynchronizationBarrier
 - synchapi/DeleteSynchronizationBarrier
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
 - DeleteSynchronizationBarrier
---

# DeleteSynchronizationBarrier function

## -description

Deletes a synchronization barrier.

## -parameters

### -param lpBarrier [in, out]

A pointer to the synchronization barrier to delete.

## -returns

The **DeleteSynchronizationBarrier** function always returns `TRUE`.

## -remarks

**DeleteSynchronizationBarrier** releases a synchronization barrier when it is no longer needed. It is safe to call **DeleteSynchronizationBarrier** immediately after calling [EnterSynchronizationBarrier](nf-synchapi-entersynchronizationbarrier.md) because that function ensures that all threads in the barrier have finished using it before allowing the barrier to be released.

If a synchronization barrier will never be deleted, threads can specify the **SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE** flag when they enter the barrier. This flag causes the function to skip the extra work required for deletion safety, which can improve performance. All threads using the barrier must specify this flag; if any thread does not, the flag is ignored. Be careful when using **SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE**, because deleting a barrier while this flag is in effect  may result in an invalid handle access and cause one or more threads to become permanently blocked.

## -see-also

[EnterSynchronizationBarrier](nf-synchapi-entersynchronizationbarrier.md)

[InitializeSynchronizationBarrier](nf-synchapi-initializesynchronizationbarrier.md)

[Synchronization Barriers](/windows/win32/Sync/synchronization-barriers)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
