---
UID: NF:winnt.InterlockedAnd64
title: InterlockedAnd64 function (winnt.h)
description: Performs an atomic AND operation on the specified LONGLONG values.
helpviewer_keywords: ["InterlockedAnd64","InterlockedAnd64 function","base.interlockedand64","winnt/InterlockedAnd64"]
old-location: base\interlockedand64.htm
tech.root: backup
ms.assetid: 544b0710-3394-4123-88e1-0621de5fe7b6
ms.date: 12/05/2018
ms.keywords: InterlockedAnd64, InterlockedAnd64 function, base.interlockedand64, winnt/InterlockedAnd64
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedAnd64
 - winnt/InterlockedAnd64
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
 - InterlockedAnd64
---

# InterlockedAnd64 function


## -description

Performs an atomic AND operation on the specified <b>LONGLONG</b> values.

## -parameters

### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.

### -param Value [in]

The second operand.

## -returns

The function returns the original value of the <i>Destination</i> parameter.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/dsx2t7yd(v=vs.85)">_InterlockedAnd64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683529(v=vs.85)">InterlockedAnd64Acquire</a> or <a href="/previous-versions/windows/desktop/legacy/ms683530(v=vs.85)">InterlockedAnd64Release</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedand">InterlockedAnd</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedand16">InterlockedAnd16</a>



<a href="/previous-versions/windows/desktop/legacy/ms683521(v=vs.85)">InterlockedAnd16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972631(v=vs.85)">InterlockedAnd16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683525(v=vs.85)">InterlockedAnd16Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms683529(v=vs.85)">InterlockedAnd64Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972632(v=vs.85)">InterlockedAnd64NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683530(v=vs.85)">InterlockedAnd64Release</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedand8">InterlockedAnd8</a>



<a href="/previous-versions/windows/desktop/legacy/ms683535(v=vs.85)">InterlockedAnd8Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972633(v=vs.85)">InterlockedAnd8NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683537(v=vs.85)">InterlockedAnd8Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms683539(v=vs.85)">InterlockedAndAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972634(v=vs.85)">InterlockedAndNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683543(v=vs.85)">InterlockedAndRelease</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>