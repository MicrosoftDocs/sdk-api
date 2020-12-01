---
UID: NF:winnt.InterlockedOr
title: InterlockedOr function (winnt.h)
description: Performs an atomic OR operation on the specified LONG values.
helpviewer_keywords: ["InterlockedOr","InterlockedOr function","base.interlockedor","winnt/InterlockedOr"]
old-location: base\interlockedor.htm
tech.root: backup
ms.assetid: c677e9fb-4188-466a-8283-9d65a50d150e
ms.date: 12/05/2018
ms.keywords: InterlockedOr, InterlockedOr function, base.interlockedor, winnt/InterlockedOr
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
 - InterlockedOr
 - winnt/InterlockedOr
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
 - InterlockedOr
---

# InterlockedOr function


## -description

Performs an atomic OR operation on the specified <b>LONG</b> values. The function prevents more than one thread from using the same variable simultaneously.

## -parameters

### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.

### -param Value [in]

The second operand.

## -returns

The function returns the original value of the <i>Destination</i> parameter.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

For the Intel Itanium-based systems and x64 architectures, this function is implemented using the compiler intrinsic. For the x86 architecture, use the <a href="/previous-versions/b11125ze(v=vs.85)">_InterlockedOr</a> compiler intrinsic directly.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683643(v=vs.85)">InterlockedOrAcquire</a> or <a href="/previous-versions/windows/desktop/legacy/ms683646(v=vs.85)">InterlockedOrRelease</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedor16">InterlockedOr16</a>



<a href="/previous-versions/windows/desktop/legacy/ms683629(v=vs.85)">InterlockedOr16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972669(v=vs.85)">InterlockedOr16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683631(v=vs.85)">InterlockedOr16Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms683633(v=vs.85)">InterlockedOr64</a>



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