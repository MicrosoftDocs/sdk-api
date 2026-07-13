---
UID: NF:winnt.InterlockedExchange16
title: InterlockedExchange16 function (winnt.h)
description: Sets a 16-bit variable to the specified value as an atomic operation.
helpviewer_keywords: ["InterlockedExchange16","InterlockedExchange16 function","base.interlockedexchange16","winnt/InterlockedExchange16"]
old-location: base\interlockedexchange16.htm
tech.root: backup
ms.assetid: 06756ec6-9c1c-4aac-99de-c45186c89af1
ms.date: 12/05/2018
ms.keywords: InterlockedExchange16, InterlockedExchange16 function, base.interlockedexchange16, winnt/InterlockedExchange16
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InterlockedExchange16
 - winnt/InterlockedExchange16
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
 - InterlockedExchange16
---

# InterlockedExchange16 function


## -description

Sets a 16-bit variable to the specified value as an atomic operation.

To operate on a 32-bit variable, use the <a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange">InterlockedExchange</a> function.

To operate on a 64-bit variable, use the <a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange64">InterlockedExchange64</a> function.

## -parameters

### -param Destination [in, out]

A pointer to the value to be exchanged. The function sets this variable to <i>ExChange</i>, and returns its prior value.

### -param ExChange [in]

The value to be exchanged with the value pointed to by <i>Destination</i>.

## -returns

The function returns the initial value of the <i>Destination</i> parameter.

## -remarks

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <b>_InterlockedExchange16</b>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="/previous-versions/windows/desktop/legacy/ms683596(v=vs.85)">InterlockedExchangeAcquire64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange">InterlockedExchange</a>



<a href="/previous-versions/windows/desktop/legacy/hh972654(v=vs.85)">InterlockedExchange16Acquire</a>



<a href="/previous-versions/windows/desktop/legacy/hh972655(v=vs.85)">InterlockedExchange16NoFence</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange64">InterlockedExchange64</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedexchange8">InterlockedExchange8</a>



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