---
UID: NF:winnt.InterlockedExchange8
title: InterlockedExchange8 function (winnt.h)
description: Sets an 8-bit variable to the specified value as an atomic operation.
helpviewer_keywords: ["InterlockedExchange8","InterlockedExchange8 function","base.interlockedexchange8","winnt/InterlockedExchange8"]
old-location: base\interlockedexchange8.htm
tech.root: backup
ms.assetid: fe07fac0-b9f2-419e-a086-09bc73125c4e
ms.date: 12/05/2018
ms.keywords: InterlockedExchange8, InterlockedExchange8 function, base.interlockedexchange8, winnt/InterlockedExchange8
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - InterlockedExchange8
 - winnt/InterlockedExchange8
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
 - InterlockedExchange8
---

# InterlockedExchange8 function


## -description

Sets an 8-bit variable to the specified value as an atomic operation.

To operate on a pointer variable, use the 
<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer">InterlockedExchangePointer</a> function.

To operate on a 16-bit variable, use the <a href="/windows/win32/api/winbase/nf-winbase-interlockedexchange16">InterlockedExchange16</a> function.

To operate on a 32-bit variable, use the <a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange">InterlockedExchange</a> function.

To operate on a 64-bit variable, use the <a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange64">InterlockedExchange64</a> function.

## -parameters

### -param Target [in, out]

A pointer to the value to be exchanged. The function sets this variable to <i>Value</i>, and returns its prior value.

### -param Value [in]

The value to be exchanged with the value pointed to by <i>Target</i>.

## -returns

The function returns the initial value of the <i>Target</i> parameter.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/cpp/intrinsics/interlockedexchange-intrinsic-functions">_InterlockedExchange8</a>.

This function generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange">InterlockedExchange</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchange16">InterlockedExchange16</a>



<a href="/previous-versions/windows/desktop/legacy/hh972654(v=vs.85)">InterlockedExchange16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972655(v=vs.85)">InterlockedExchange16NoFence</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange64">InterlockedExchange64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683594(v=vs.85)">InterlockedExchangeAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/ms683596(v=vs.85)">InterlockedExchangeAcquire64</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd">InterlockedExchangeAdd</a>



<a href="/previous-versions/windows/desktop/legacy/hh972659(v=vs.85)">InterlockedExchangeNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972660(v=vs.85)">InterlockedExchangeNoFence64</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer">InterlockedExchangePointer</a>



<a href="/previous-versions/windows/desktop/legacy/ms683611(v=vs.85)">InterlockedExchangePointerAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972661(v=vs.85)">InterlockedExchangePointerNoFence</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeSubtract</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>