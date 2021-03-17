---
UID: NF:winnt.InterlockedOr64
title: InterlockedOr64 function (winnt.h)
description: Performs an atomic OR operation on the specified LONGLONG values.
helpviewer_keywords: ["InterlockedOr64","InterlockedOr64 function","base.interlockedor64","winnt/InterlockedOr64"]
old-location: base\interlockedor64.htm
tech.root: backup
ms.assetid: ba0b03dc-de6c-4ecb-8f64-54c7c83f154a
ms.date: 12/05/2018
ms.keywords: InterlockedOr64, InterlockedOr64 function, base.interlockedor64, winnt/InterlockedOr64
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
 - InterlockedOr64
 - winnt/InterlockedOr64
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
 - InterlockedOr64
---

# InterlockedOr64 function


## -description

Performs an atomic OR operation on the specified <b>LONGLONG</b> values. The function prevents more than one thread from using the same variable simultaneously.

## -parameters

### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.

### -param Value [in]

The second operand.

## -returns

The function returns the original value of the <i>Destination</i> parameter.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and [_InterlockedOr64](/cpp/intrinsics/interlockedor-intrinsic-functions).

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683634(v=vs.85)">InterlockedOr64Acquire</a> or <a href="/previous-versions/windows/desktop/legacy/ms683636(v=vs.85)">InterlockedOr64Release</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedor">InterlockedOr</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedor16">InterlockedOr16</a>



<a href="/previous-versions/windows/desktop/legacy/ms683629(v=vs.85)">InterlockedOr16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972669(v=vs.85)">InterlockedOr16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683631(v=vs.85)">InterlockedOr16Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms683634(v=vs.85)">InterlockedOr64Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972670(v=vs.85)">InterlockedOr64NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683636(v=vs.85)">InterlockedOr64Release</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedor8">InterlockedOr8</a>



<a href="/previous-versions/windows/desktop/legacy/ms683639(v=vs.85)">InterlockedOr8Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972671(v=vs.85)">InterlockedOr8NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683640(v=vs.85)">InterlockedOr8Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms683643(v=vs.85)">InterlockedOrAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972672(v=vs.85)">InterlockedOrNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683646(v=vs.85)">InterlockedOrRelease</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>

