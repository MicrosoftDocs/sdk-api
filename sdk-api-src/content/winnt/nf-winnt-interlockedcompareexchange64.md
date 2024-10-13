---
UID: NF:winnt.InterlockedCompareExchange64
title: InterlockedCompareExchange64 function (winnt.h)
description: Performs an atomic compare-and-exchange operation on the specified values. The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.
helpviewer_keywords: ["InterlockedCompareExchange64","InterlockedCompareExchange64 function","base.interlockedcompareexchange64","winnt/InterlockedCompareExchange64"]
old-location: base\interlockedcompareexchange64.htm
tech.root: backup
ms.assetid: b0799de3-49f9-4eef-9c14-d145f42ce57b
ms.date: 12/05/2018
ms.keywords: InterlockedCompareExchange64, InterlockedCompareExchange64 function, base.interlockedcompareexchange64, winnt/InterlockedCompareExchange64
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedCompareExchange64
 - winnt/InterlockedCompareExchange64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Interlocked-l1-1-0.dll
 - API-MS-Win-Core-Interlocked-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - InterlockedCompareExchange64
---

# InterlockedCompareExchange64 function


## -description

Performs an atomic compare-and-exchange operation on the specified values. The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.

## -parameters

### -param Destination [in, out]

A pointer to the destination value.

### -param ExChange [in]

The exchange value.

### -param Comperand [in]

The value to compare to <i>Destination</i>.

## -returns

The function returns the initial value of the <i>Destination</i> parameter.

## -remarks

The 
function compares the <i>Destination</i> value with the <i>Comparand</i> value. If the <i>Destination</i> value is equal to the <i>Comparand</i> value, the <i>Exchange</i> value is stored in the address specified by <i>Destination</i>. Otherwise, no operation is performed.

The variables for 
this function must be aligned on a 64-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. <b>malloc</b>, <b>calloc</b,> <b>HeapAlloc</b>, and <b>HeapReAlloc</b> provide sufficiently aligned memory.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="/previous-versions/ttk2z1ws(v=vs.85)">_InterlockedCompareExchange64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)">InterlockedCompareExchangeAcquire64</a> or <a href="/previous-versions/windows/desktop/legacy/ms683576(v=vs.85)">InterlockedCompareExchangeRelease64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)">InterlockedCompare64Exchange128</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedcompareexchange128">InterlockedCompareExchange128</a>



<a href="/windows/desktop/api/winnt/nf-winnt-interlockedcompareexchange16">InterlockedCompareExchange16</a>



<a href="/previous-versions/windows/desktop/legacy/hh972642(v=vs.85)">InterlockedCompareExchange16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972643(v=vs.85)">InterlockedCompareExchange16NoFence</a>



<a href="/previous-versions/windows/desktop/legacy/hh972644(v=vs.85)">InterlockedCompareExchange16Release</a>



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
