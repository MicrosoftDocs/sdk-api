---
UID: NF:winnt.InterlockedIncrement64
title: InterlockedIncrement64 function (winnt.h)
description: Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.
helpviewer_keywords: ["InterlockedIncrement64","InterlockedIncrement64 function","base.interlockedincrement64","winnt/InterlockedIncrement64"]
old-location: base\interlockedincrement64.htm
tech.root: backup
ms.assetid: f18b63fa-201f-436d-a152-41e458959a5c
ms.date: 12/05/2018
ms.keywords: InterlockedIncrement64, InterlockedIncrement64 function, base.interlockedincrement64, winnt/InterlockedIncrement64
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedIncrement64
 - winnt/InterlockedIncrement64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - InterlockedIncrement64
---

# InterlockedIncrement64 function


## -description

Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.

To operate on 32-bit values, use the <a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a> function.

## -parameters

### -param Addend [in, out]

A pointer to the variable to be incremented.

## -returns

The function returns the resulting incremented value.

## -remarks

The variable pointed to by the <i>Addend</i> parameter must be aligned on a 64-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/2ddez55b(v=vs.85)">_InterlockedIncrement64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683620(v=vs.85)">InterlockedIncrementAcquire64</a> or <a href="/previous-versions/windows/desktop/legacy/ms683624(v=vs.85)">InterlockedIncrementRelease64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedincrement16">InterlockedIncrement16</a>



<a href="/previous-versions/windows/desktop/legacy/hh972663(v=vs.85)">InterlockedIncrement16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972664(v=vs.85)">InterlockedIncrement16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972665(v=vs.85)">InterlockedIncrement16Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)">InterlockedIncrementAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/ms683620(v=vs.85)">InterlockedIncrementAcquire64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972667(v=vs.85)">InterlockedIncrementNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972668(v=vs.85)">InterlockedIncrementNoFence64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683622(v=vs.85)">InterlockedIncrementRelease</a>



<a href="/previous-versions/windows/desktop/legacy/ms683624(v=vs.85)">InterlockedIncrementRelease64</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>