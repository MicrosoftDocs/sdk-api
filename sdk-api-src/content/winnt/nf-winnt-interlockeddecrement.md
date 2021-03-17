---
UID: NF:winnt.InterlockedDecrement
title: InterlockedDecrement function (winnt.h)
description: Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.
helpviewer_keywords: ["InterlockedDecrement","InterlockedDecrement function","_win32_interlockeddecrement","base.interlockeddecrement","winnt/InterlockedDecrement"]
old-location: base\interlockeddecrement.htm
tech.root: backup
ms.assetid: d6ed6cb1-aa10-48f4-9b62-73708ff4d1e3
ms.date: 12/05/2018
ms.keywords: InterlockedDecrement, InterlockedDecrement function, _win32_interlockeddecrement, base.interlockeddecrement, winnt/InterlockedDecrement
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
 - InterlockedDecrement
 - winnt/InterlockedDecrement
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
 - InterlockedDecrement
---

# InterlockedDecrement function


## -description

Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.

To operate on 64-bit values, use the <a href="/windows/desktop/api/winnt/nf-winnt-interlockeddecrement64">InterlockedDecrement64</a> function.

## -parameters

### -param Addend [in, out]

A pointer to the variable to be decremented.

## -returns

The function returns the resulting decremented value.

## -remarks

The variable pointed to by the <i>Addend</i> parameter must be aligned on a 32-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/f24ya7ct(v=vs.85)">_InterlockedDecrement</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)">InterlockedDecrementAcquire</a> or <a href="/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)">InterlockedDecrementRelease</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockeddecrement16">InterlockedDecrement16</a>



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



<a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>