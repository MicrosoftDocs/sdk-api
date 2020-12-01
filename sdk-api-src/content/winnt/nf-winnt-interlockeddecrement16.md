---
UID: NF:winnt.InterlockedDecrement16
title: InterlockedDecrement16 function (winnt.h)
description: Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.
helpviewer_keywords: ["InterlockedDecrement16","InterlockedDecrement16 function","base.interlockeddecrement16","winnt/InterlockedDecrement16"]
old-location: base\interlockeddecrement16.htm
tech.root: backup
ms.assetid: 64fbfe37-fce5-4d96-aecb-3850d1edd34e
ms.date: 12/05/2018
ms.keywords: InterlockedDecrement16, InterlockedDecrement16 function, base.interlockeddecrement16, winnt/InterlockedDecrement16
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedDecrement16
 - winnt/InterlockedDecrement16
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
 - InterlockedDecrement16
---

# InterlockedDecrement16 function


## -description

Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.

To operate on 32-bit values, use the <a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a> function.

To operate on 64-bit values, use the <a href="/windows/desktop/api/winnt/nf-winnt-interlockeddecrement64">InterlockedDecrement64</a> function.

## -parameters

### -param Addend [in, out]

A pointer to the variable to be decremented.

## -returns

The function returns the resulting decremented value.

## -remarks

The variable pointed to by the <i>Addend</i> parameter must be aligned on a 16-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/f24ya7ct(v=vs.85)">_InterlockedDecrement16</a>.

This function generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>



<a href="/previous-versions/windows/desktop/legacy/hh972649(v=vs.85)">InterlockedDecrement16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972650(v=vs.85)">InterlockedDecrement16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972651(v=vs.85)">InterlockedDecrement16Release</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockeddecrement64">InterlockedDecrement64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)">InterlockedDecrementAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/ms683585(v=vs.85)">InterlockedDecrementAcquire64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972652(v=vs.85)">InterlockedDecrementNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972653(v=vs.85)">InterlockedDecrementNoFence64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)">InterlockedDecrementRelease</a>



<a href="/previous-versions/windows/desktop/legacy/ms683588(v=vs.85)">InterlockedDecrementRelease64</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>