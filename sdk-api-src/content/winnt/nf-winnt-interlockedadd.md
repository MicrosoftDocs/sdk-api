---
UID: NF:winnt.InterlockedAdd
title: InterlockedAdd function (winnt.h)
description: Performs an atomic addition operation on the specified LONG values.
helpviewer_keywords: ["InterlockedAdd","InterlockedAdd function","base.interlockedadd","winnt/InterlockedAdd"]
old-location: base\interlockedadd.htm
tech.root: backup
ms.assetid: c3ff4c2f-ac84-4046-ac4e-600569b874be
ms.date: 12/05/2018
ms.keywords: InterlockedAdd, InterlockedAdd function, base.interlockedadd, winnt/InterlockedAdd
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
 - InterlockedAdd
 - winnt/InterlockedAdd
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
 - InterlockedAdd
---

# InterlockedAdd function


## -description

Performs an atomic addition operation on the specified <b>LONG</b> values.

## -parameters

### -param Addend [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.

### -param Value [in]

The second operand.

## -returns

The function returns the result of the operation.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/51s265a6(v=vs.85)">_InterlockedAdd</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-_inlineinterlockedadd64">InterlockedAdd64</a>



<a href="/windows/win32/api/winnt/nf-winnt-_inlineinterlockedadd">InterlockedAddAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/ms683510(v=vs.85)">InterlockedAddAcquire64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972629(v=vs.85)">InterlockedAddNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972630(v=vs.85)">InterlockedAddNoFence64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683513(v=vs.85)">InterlockedAddRelease</a>



<a href="/previous-versions/windows/desktop/legacy/ms683514(v=vs.85)">InterlockedAddRelease64</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd">InterlockedExchangeAdd</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>