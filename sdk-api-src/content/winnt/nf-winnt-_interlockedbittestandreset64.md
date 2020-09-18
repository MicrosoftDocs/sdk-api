---
UID: NF:winnt._interlockedbittestandreset64
title: _interlockedbittestandreset64 function (winnt.h)
description: Tests the specified bit of the specified LONG64 value and sets it to 0. The operation is atomic.
helpviewer_keywords: ["InterlockedBitTestAndReset64","InterlockedBitTestAndReset64 function","_interlockedbittestandreset64","base.interlockedbittestandreset64","winnt/InterlockedBitTestAndReset64"]
old-location: base\interlockedbittestandreset64.htm
tech.root: backup
ms.assetid: a0f05333-d391-4596-b4f1-3146b46a6108
ms.date: 12/05/2018
ms.keywords: InterlockedBitTestAndReset64, InterlockedBitTestAndReset64 function, _interlockedbittestandreset64, base.interlockedbittestandreset64, winnt/InterlockedBitTestAndReset64
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
 - _interlockedbittestandreset64
 - winnt/_interlockedbittestandreset64
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
 - InterlockedBitTestAndReset64
---

# _interlockedbittestandreset64 function


## -description

Tests the specified bit of the specified <b>LONG64</b> value and sets it to 0. The operation is atomic.

## -parameters

### -param Base [in]

A pointer to a variable.

### -param Offset [in]

The bit position to be tested.

## -returns

The value of the specified bit.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/h1haebfw(v=vs.85)">_interlockedbittestandreset64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-_interlockedbittestandreset">InterlockedBitTestAndReset</a>



<a href="/previous-versions/windows/desktop/legacy/hh972636(v=vs.85)">InterlockedBitTestAndResetAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972637(v=vs.85)">InterlockedBitTestAndResetRelease</a>



<a href="/windows/win32/api/winnt/nf-winnt-_interlockedbittestandset">InterlockedBitTestAndSet</a>



<a href="/windows/win32/api/winnt/nf-winnt-_interlockedbittestandset64">InterlockedBitTestAndSet64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972638(v=vs.85)">InterlockedBitTestAndSetAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972639(v=vs.85)">InterlockedBitTestAndSetRelease</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>