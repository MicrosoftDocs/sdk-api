---
UID: NF:winnt.InterlockedCompareExchange128
title: InterlockedCompareExchange128 function (winnt.h)
description: Performs an atomic compare-and-exchange operation on the specified values. The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.
helpviewer_keywords: ["InterlockedCompareExchange128","InterlockedCompareExchange128 function","base.interlockedcompareexchange128","winnt/InterlockedCompareExchange128"]
old-location: base\interlockedcompareexchange128.htm
tech.root: backup
ms.assetid: 55a5ec1d-9c81-479e-a630-81756bf620d1
ms.date: 12/05/2018
ms.keywords: InterlockedCompareExchange128, InterlockedCompareExchange128 function, base.interlockedcompareexchange128, winnt/InterlockedCompareExchange128
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
 - InterlockedCompareExchange128
 - winnt/InterlockedCompareExchange128
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
 - InterlockedCompareExchange128
---

# InterlockedCompareExchange128 function


## -description

Performs an atomic compare-and-exchange operation on the specified values. The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.

To operate on 16-bit values, use the <a href="/windows/desktop/api/winnt/nf-winnt-interlockedcompareexchange16">InterlockedCompareExchange16</a> function.

To operate on 32-bit values, use the <a href="/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a> function.

To operate on 64-bit values, use the <a href="/windows/desktop/api/winnt/nf-winnt-interlockedcompareexchange64">InterlockedCompareExchange64</a> function.

## -parameters

### -param Destination [in, out]

 A pointer to the destination value.  This parameter is an array of two 64-bit integers considered as a 128-bit field.

### -param ExchangeHigh [in]

The high part of the exchange value.

### -param ExchangeLow [in]

The low part of the exchange value.

### -param ComparandResult [in, out]

The value to compare to. This parameter is an array of two 64-bit integers considered as a 128-bit field. On output, this is overwritten with the original value of the destination.

## -returns

The function returns 1 if <i>ComparandResult</i> equals the original value of the <i>Destination</i> parameter, or 0 if <i>ComparandResult</i> does not equal the original value of the <i>Destination</i> parameter.

## -remarks

The 
function compares the <i>Destination</i> value with the <i>ComparandResult</i> value:

<ul>
<li>If the <i>Destination</i> value is equal to the <i>ComparandResult</i> value, the <i>ExchangeHigh</i> and <i>ExchangeLow</i> values are stored in the array specified by <i>Destination</i>, and also in the array specified by <i>ComparandResult</i>.</li>
<li>Otherwise, the <i>Destination</i> is left unmodified. </li>
</ul>
Regardless of the result of the comparison, the original <i>Destination</i> value is stored in the array specified by <i>ComparandResult</i>.

The parameters for this function must be aligned on a 16-byte boundary; otherwise, the function will behave unpredictably on x64 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is only available on x64-based systems, and it is implemented using a compiler intrinsic. For more information, see the WinBase.h header file and <a href="/previous-versions/ttk2z1ws(v=vs.85)">_InterlockedCompareExchange128</a>.

This function generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)">InterlockedCompare64Exchange128</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedcompareexchange16">InterlockedCompareExchange16</a>



<a href="/previous-versions/windows/desktop/legacy/hh972642(v=vs.85)">InterlockedCompareExchange16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972643(v=vs.85)">InterlockedCompareExchange16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972644(v=vs.85)">InterlockedCompareExchange16Release</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedcompareexchange64">InterlockedCompareExchange64</a>



<a href="/previous-versions/windows/desktop/legacy/ms683564(v=vs.85)">InterlockedCompareExchangeAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)">InterlockedCompareExchangeAcquire64</a>



<a href="/previous-versions/windows/desktop/legacy/hh972645(v=vs.85)">InterlockedCompareExchangeNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972646(v=vs.85)">InterlockedCompareExchangeNoFence64</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedcompareexchangepointer">InterlockedCompareExchangePointer</a>



<a href="/previous-versions/windows/desktop/legacy/ms683570(v=vs.85)">InterlockedCompareExchangePointerAcquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972647(v=vs.85)">InterlockedCompareExchangePointerNoFence</a>



<a href="/previous-versions/windows/desktop/legacy/ms683571(v=vs.85)">InterlockedCompareExchangePointerRelease</a>



<a href="/previous-versions/windows/desktop/legacy/ms683574(v=vs.85)">InterlockedCompareExchangeRelease</a>



<a href="/previous-versions/windows/desktop/legacy/ms683576(v=vs.85)">InterlockedCompareExchangeRelease64</a>



<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>