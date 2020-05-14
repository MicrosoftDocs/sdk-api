---
UID: NF:winnt.InterlockedAnd8
title: InterlockedAnd8 function (winnt.h)
description: Performs an atomic AND operation on the specified char values.helpviewer_keywords: ["InterlockedAnd8","InterlockedAnd8 function","base.interlockedand8","winnt/InterlockedAnd8"]
old-location: base\interlockedand8.htm
tech.root: Sync
ms.assetid: 1b900308-f1dd-465b-b67d-ec2655819425
ms.date: 12/05/2018
ms.keywords: InterlockedAnd8, InterlockedAnd8 function, base.interlockedand8, winnt/InterlockedAnd8
f1_keywords:
- winnt/InterlockedAnd8
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winnt.h
api_name:
- InterlockedAnd8
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InterlockedAnd8 function


## -description


Performs an atomic AND operation on the specified <b>char</b> values.


## -parameters




### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the original value of the <i>Destination</i> parameter.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

For the Intel Itanium-based systems and x64 architectures, this function is implemented using the compiler intrinsic. For the x86 architecture, use the <a href="https://docs.microsoft.com/previous-versions/dsx2t7yd(v=vs.85)">_InterlockedAnd8</a> compiler intrinsic directly.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683535(v=vs.85)">InterlockedAnd8Acquire</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683537(v=vs.85)">InterlockedAnd8Release</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedand">InterlockedAnd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-interlockedand16">InterlockedAnd16</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683521(v=vs.85)">InterlockedAnd16Acquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972631(v=vs.85)">InterlockedAnd16NoFence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683525(v=vs.85)">InterlockedAnd16Release</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-interlockedand64">InterlockedAnd64</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683529(v=vs.85)">InterlockedAnd64Acquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972632(v=vs.85)">InterlockedAnd64NoFence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683530(v=vs.85)">InterlockedAnd64Release</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683535(v=vs.85)">InterlockedAnd8Acquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972633(v=vs.85)">InterlockedAnd8NoFence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683537(v=vs.85)">InterlockedAnd8Release</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683539(v=vs.85)">InterlockedAndAcquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972634(v=vs.85)">InterlockedAndNoFence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683543(v=vs.85)">InterlockedAndRelease</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

