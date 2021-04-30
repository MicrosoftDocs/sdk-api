---
UID: NF:synchapi.EnterSynchronizationBarrier
title: EnterSynchronizationBarrier function (synchapi.h)
description: Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.
helpviewer_keywords: ["EnterSynchronizationBarrier","EnterSynchronizationBarrier function","SYNCHRONIZATION_BARRIER_FLAGS_BLOCK_ONLY","SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE","SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY","base.entersynchronizationbarrier","synchapi/EnterSynchronizationBarrier"]
old-location: base\entersynchronizationbarrier.htm
tech.root: base
ms.assetid: cd938370-b046-4369-931d-5c7c8db7303a
ms.date: 12/05/2018
ms.keywords: EnterSynchronizationBarrier, EnterSynchronizationBarrier function, SYNCHRONIZATION_BARRIER_FLAGS_BLOCK_ONLY, SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE, SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY, base.entersynchronizationbarrier, synchapi/EnterSynchronizationBarrier
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
 - EnterSynchronizationBarrier
 - synchapi/EnterSynchronizationBarrier
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
 - EnterSynchronizationBarrier
---

# EnterSynchronizationBarrier function


## -description

Causes the calling thread to wait at a synchronization barrier until the maximum number of threads 
    have entered the barrier.

## -parameters

### -param lpBarrier [in, out]

A pointer to an initialized synchronization barrier. Use the 
      <a href="/windows/desktop/api/synchapi/nf-synchapi-initializesynchronizationbarrier">InitializeSynchronizationBarrier</a> 
      function to initialize the barrier. <b>SYNCHRONIZATION_BARRIER</b> is an opaque 
      structure that should not be modified by the application.

### -param dwFlags [in]

Flags that control the behavior of threads that enter this barrier. This parameter can be one or more of 
      the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYNCHRONIZATION_BARRIER_FLAGS_BLOCK_ONLY"></a><a id="synchronization_barrier_flags_block_only"></a><dl>
<dt><b>SYNCHRONIZATION_BARRIER_FLAGS_BLOCK_ONLY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Specifies that the thread entering the barrier should block immediately until the last thread enters the 
        barrier. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY"></a><a id="synchronization_barrier_flags_spin_only"></a><dl>
<dt><b>SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Specifies that the thread entering the barrier should spin until the last thread enters the barrier, even 
        if the spinning thread exceeds the barrier's maximum spin count. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE"></a><a id="synchronization_barrier_flags_no_delete"></a><dl>
<dt><b>SYNCHRONIZATION_BARRIER_FLAGS_NO_DELETE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Specifies that the function can skip the work required to ensure that it is safe to delete the barrier, 
        which can improve performance. All threads that enter this barrier must specify the flag; otherwise, the flag 
        is ignored. This flag should be used only if the barrier will never be deleted.

</td>
</tr>
</table>

## -returns

<b>TRUE</b> for the last thread to signal the barrier. Threads that signal the barrier 
      before the last thread signals it receive a return value of <b>FALSE</b>.

## -remarks

The default behavior for threads entering a synchronization barrier is to spin until the maximum spin count of 
    the barrier is reached, and then block. This allows threads to resume quickly if the last thread enters the 
    barrier in a relatively short time.  However, if the last thread takes relatively longer to arrive, threads 
    already in the barrier block so they stop consuming processor time while waiting.

A thread can override the default behavior of the barrier by specifying 
    <b>SYNCHRONIZATION_BARRIER_FLAGS_BLOCK_ONLY</b> or 
    <b>SYNCHRONIZATION_BARRIER_FLAGS_SPIN_ONLY</b>. However, keep in mind that using these flags 
    can affect performance. Spinning indefinitely keeps a processor from servicing other threads, while premature 
    blocking incurs the overhead of swapping the thread off the processor, awakening the thread when it unblocks, and 
    swapping it back onto the processor again. In general it is better to allow the barrier to manage threads and use 
    these flags only if performance testing indicates the application would benefit from them.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-deletesynchronizationbarrier">DeleteSynchronizationBarrier</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-initializesynchronizationbarrier">InitializeSynchronizationBarrier</a>



<a href="/windows/desktop/Sync/synchronization-barriers">Synchronization Barriers</a>