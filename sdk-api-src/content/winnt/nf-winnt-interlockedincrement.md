---
UID: NF:winnt.InterlockedIncrement
title: InterlockedIncrement function (winnt.h)
description: Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.
helpviewer_keywords: ["InterlockedIncrement","InterlockedIncrement function","_win32_interlockedincrement","base.interlockedincrement","winnt/InterlockedIncrement"]
old-location: base\interlockedincrement.htm
tech.root: backup
ms.assetid: 87eda7fb-966d-4630-9da6-8933b53daadd
ms.date: 12/05/2018
ms.keywords: InterlockedIncrement, InterlockedIncrement function, _win32_interlockedincrement, base.interlockedincrement, winnt/InterlockedIncrement
req.header: winnt.h
req.include-header: Windows.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedIncrement
 - winnt/InterlockedIncrement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Interlocked-l1-1-0.dll
 - API-MS-Win-Core-Interlocked-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - InterlockedIncrement
---

# InterlockedIncrement function


## -description

Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.

To operate on 64-bit values, use the <a href="/windows/desktop/api/winnt/nf-winnt-interlockedincrement64">InterlockedIncrement64</a> function.

## -parameters

### -param Addend [in, out]

A pointer to the variable to be incremented.

## -returns

The function returns the resulting incremented value.

## -remarks

The variable pointed to by the <i>Addend</i> parameter must be aligned on a 32-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/2ddez55b(v=vs.85)">_InterlockedIncrement</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)">InterlockedIncrementAcquire</a> or <a href="/previous-versions/windows/desktop/legacy/ms683622(v=vs.85)">InterlockedIncrementRelease</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedincrement16">InterlockedIncrement16</a>



<a href="/previous-versions/windows/desktop/legacy/hh972663(v=vs.85)">InterlockedIncrement16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972664(v=vs.85)">InterlockedIncrement16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972665(v=vs.85)">InterlockedIncrement16Release</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedincrement64">InterlockedIncrement64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)">InterlockedIncrementAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/ms683620(v=vs.85)">InterlockedIncrementAcquire64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972667(v=vs.85)">InterlockedIncrementNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972668(v=vs.85)">InterlockedIncrementNoFence64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683622(v=vs.85)">InterlockedIncrementRelease</a>



<a href="/previous-versions/windows/desktop/legacy/ms683624(v=vs.85)">InterlockedIncrementRelease64</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>