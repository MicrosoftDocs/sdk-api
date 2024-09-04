---
UID: NF:winnt._interlockedbittestandset
title: _interlockedbittestandset function (winnt.h)
description: Tests the specified bit of the specified LONG value and sets it to 1. The operation is atomic.
helpviewer_keywords: ["InterlockedBitTestAndSet","InterlockedBitTestAndSet function","_interlockedbittestandset","base.interlockedbittestandset","winnt/InterlockedBitTestAndSet"]
old-location: base\interlockedbittestandset.htm
tech.root: backup
ms.assetid: 26c1f4b5-02db-4316-ab5d-23e60fc6b116
ms.date: 12/05/2018
ms.keywords: InterlockedBitTestAndSet, InterlockedBitTestAndSet function, _interlockedbittestandset, base.interlockedbittestandset, winnt/InterlockedBitTestAndSet
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
 - _interlockedbittestandset
 - winnt/_interlockedbittestandset
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
 - InterlockedBitTestAndSet
---

# _interlockedbittestandset function


## -description

Tests the specified bit of the specified <b>LONG</b> value and sets it to 1. The operation is atomic.

## -parameters

### -param Base [in]

A pointer to a variable.

### -param Offset [in]

The bit position to be tested. The offset is from the least-significant bit position, with zero testing the least-significant bit, and 31 testing the most-significant bit.

## -returns

The value of the specified bit.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/646k06sz(v=vs.85)">_interlockedbittestandset</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-_interlockedbittestandreset">InterlockedBitTestAndReset</a>



<a href="/windows/win32/api/winnt/nf-winnt-_interlockedbittestandreset64">InterlockedBitTestAndReset64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972636(v=vs.85)">InterlockedBitTestAndResetAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972637(v=vs.85)">InterlockedBitTestAndResetRelease</a>



<a href="/windows/win32/api/winnt/nf-winnt-_interlockedbittestandset64">InterlockedBitTestAndSet64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972638(v=vs.85)">InterlockedBitTestAndSetAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972639(v=vs.85)">InterlockedBitTestAndSetRelease</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
