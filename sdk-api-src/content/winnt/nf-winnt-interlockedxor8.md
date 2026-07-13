---
UID: NF:winnt.InterlockedXor8
title: InterlockedXor8 function (winnt.h)
description: Performs an atomic XOR operation on the specified char values.
helpviewer_keywords: ["InterlockedXor8","InterlockedXor8 function","base.interlockedxor8","winnt/InterlockedXor8"]
old-location: base\interlockedxor8.htm
tech.root: backup
ms.assetid: 9b96417e-dc2e-4b67-8084-0c0219444299
ms.date: 12/05/2018
ms.keywords: InterlockedXor8, InterlockedXor8 function, base.interlockedxor8, winnt/InterlockedXor8
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
 - InterlockedXor8
 - winnt/InterlockedXor8
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
 - InterlockedXor8
---

# InterlockedXor8 function


## -description

Performs an atomic XOR operation on the specified <b>char</b> values. The function prevents more than one thread from using the same variable simultaneously.

## -parameters

### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.

### -param Value [in]

The second operand.

## -returns

The function returns the original value of the <i>Destination</i> parameter.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

For the Intel Itanium-based systems and x64 architectures, this function is implemented using the compiler intrinsic. For the x86 architecture, use the <a href="/previous-versions/a8swb4hb(v=vs.85)">_InterlockedXor8</a> compiler intrinsic directly.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms684112(v=vs.85)">InterlockedXor8Acquire</a> or <a href="/previous-versions/windows/desktop/legacy/ms684113(v=vs.85)">InterlockedXor8Release</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedxor">InterlockedXor</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedxor16">InterlockedXor16</a>



<a href="/previous-versions/windows/desktop/legacy/ms684026(v=vs.85)">InterlockedXor16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972674(v=vs.85)">InterlockedXor16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684033(v=vs.85)">InterlockedXor16Release</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedxor64">InterlockedXor64</a>



<a href="/previous-versions/windows/desktop/legacy/ms684107(v=vs.85)">InterlockedXor64Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972675(v=vs.85)">InterlockedXor64NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684108(v=vs.85)">InterlockedXor64Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms684112(v=vs.85)">InterlockedXor8Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972676(v=vs.85)">InterlockedXor8NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684113(v=vs.85)">InterlockedXor8Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms684117(v=vs.85)">InterlockedXorAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972677(v=vs.85)">InterlockedXorNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684118(v=vs.85)">InterlockedXorRelease</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>