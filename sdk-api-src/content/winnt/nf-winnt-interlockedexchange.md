---
UID: NF:winnt.InterlockedExchange
title: InterlockedExchange function (winnt.h)
description: Sets a 32-bit variable to the specified value as an atomic operation.
helpviewer_keywords: ["InterlockedExchange","InterlockedExchange function","_win32_interlockedexchange","base.interlockedexchange","winnt/InterlockedExchange"]
old-location: base\interlockedexchange.htm
tech.root: backup
ms.assetid: 22142195-b592-4a7b-9b23-e31984cc1d41
ms.date: 12/05/2018
ms.keywords: InterlockedExchange, InterlockedExchange function, _win32_interlockedexchange, base.interlockedexchange, winnt/InterlockedExchange
f1_keywords:
- winnt/InterlockedExchange
dev_langs:
- c++
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
- InterlockedExchange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InterlockedExchange function


## -description


Sets a 32-bit variable to the specified value as an atomic operation.

To operate on a pointer variable, use the 
<a href="https://docs.microsoft.com/en-us/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer">InterlockedExchangePointer</a> function.

To operate on a 16-bit variable, use the <a href="https://docs.microsoft.com/en-us/windows/win32/api/winnt/nf-winnt-interlockedexchange16">InterlockedExchange16</a> function.

To operate on a 64-bit variable, use the <a href="https://docs.microsoft.com/en-us/windows/win32/api/winnt/nf-winnt-interlockedexchange64">InterlockedExchange64</a> function.


## -parameters




### -param Target [in, out]

A pointer to the value to be exchanged. The function sets this variable to <i>Value</i>, and returns its prior value.


### -param Value [in]

The value to be exchanged with the value pointed to by <i>Target</i>.


## -returns



The function returns the initial value of the <i>Target</i> parameter.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://docs.microsoft.com/en-us/cpp/intrinsics/interlockedexchange-intrinsic-functions">_InterlockedExchange</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://docs.microsoft.com/en-us/previous-versions/windows/desktop/legacy/ms683594(v%3Dvs.85)">InterlockedExchangeAcquire</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchange</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchange16</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchange16Acquire</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchange16NoFence</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchange64</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchange8</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAcquire</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAcquire64</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAdd</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAdd64</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAddAcquire</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAddAcquire64</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAddNoFence</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAddNoFence64</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAddRelease</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeAddRelease64</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeNoFence</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeNoFence64</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangePointer</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangePointerAcquire</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangePointerNoFence</a>



<a href="/windows/win32/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeSubtract</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

