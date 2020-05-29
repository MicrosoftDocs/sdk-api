---
UID: NF:winnt.InterlockedXor64
title: InterlockedXor64 function (winnt.h)
description: Performs an atomic XOR operation on the specified LONGLONG values.
helpviewer_keywords: ["InterlockedXor64","InterlockedXor64 function","base.interlockedxor64","winnt/InterlockedXor64"]
old-location: base\interlockedxor64.htm
tech.root: Sync
ms.assetid: b0eef2c9-5b28-462b-91cb-20a337efca7e
ms.date: 12/05/2018
ms.keywords: InterlockedXor64, InterlockedXor64 function, base.interlockedxor64, winnt/InterlockedXor64
f1_keywords:
- winnt/InterlockedXor64
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
- InterlockedXor64
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InterlockedXor64 function


## -description


Performs an atomic XOR operation on the specified <b>LONGLONG</b> values. The function prevents more than one thread from using the same variable simultaneously.


## -parameters




### -param Destination [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the original value of the <i>Destination</i> parameter.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/a8swb4hb(v=vs.85)">_InterlockedXor64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms684107(v=vs.85)">InterlockedXor64Acquire</a> or <a href="/previous-versions/windows/desktop/legacy/ms684108(v=vs.85)">InterlockedXor64Release</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedxor">InterlockedXor</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedxor16">InterlockedXor16</a>



<a href="/previous-versions/windows/desktop/legacy/ms684026(v=vs.85)">InterlockedXor16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972674(v=vs.85)">InterlockedXor16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684033(v=vs.85)">InterlockedXor16Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms684107(v=vs.85)">InterlockedXor64Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972675(v=vs.85)">InterlockedXor64NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684108(v=vs.85)">InterlockedXor64Release</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedxor8">InterlockedXor8</a>



<a href="/previous-versions/windows/desktop/legacy/ms684112(v=vs.85)">InterlockedXor8Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972676(v=vs.85)">InterlockedXor8NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684113(v=vs.85)">InterlockedXor8Release</a>



<a href="/previous-versions/windows/desktop/legacy/ms684117(v=vs.85)">InterlockedXorAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972677(v=vs.85)">InterlockedXorNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms684118(v=vs.85)">InterlockedXorRelease</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

