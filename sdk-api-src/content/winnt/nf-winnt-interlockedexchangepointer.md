---
UID: NF:winnt.InterlockedExchangePointer
title: InterlockedExchangePointer function (winnt.h)
author: windows-sdk-content
description: Atomically exchanges a pair of addresses.
old-location: base\interlockedexchangepointer.htm
tech.root: Sync
ms.assetid: 479aede8-e9e3-42c2-9081-94c150c7f274
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InterlockedExchangePointer, InterlockedExchangePointer function, _win32_interlockedexchangepointer, base.interlockedexchangepointer, winnt/InterlockedExchangePointer
ms.topic: function
f1_keywords: ["winnt/InterlockedExchangePointer"]
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
 - InterlockedExchangePointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InterlockedExchangePointer function


## -description


Atomically exchanges a pair of addresses.


## -parameters




### -param Target [in, out]

A pointer to the address to exchange. The function sets the  address pointed to by the <i>Target</i> parameter (<code>*Target</code>) to the address that is the value of the <i>Value</i> parameter, and returns the prior value of the <i>Target</i> parameter. 


### -param Value [in]

The address to be exchanged with the address pointed to by the <i>Target</i> parameter (<code>*Target</code>).


## -returns



The function returns the initial address pointed to by the <i>Target</i> parameter.




## -remarks



This function copies the address passed as the second parameter to the first and returns the original address of the first.

On a 64-bit system, the parameters are 64 bits and the <i>Target</i> parameter must be aligned on 64-bit boundaries; otherwise, the function will behave unpredictably. On a 32-bit system, the parameters are 32 bits and the <i>Target</i> parameter must be aligned on 32-bit boundaries.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://docs.microsoft.com/previous-versions//853x471w(v=vs.85)">_InterlockedExchangePointer</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683611(v=vs.85)">InterlockedExchangePointerAcquire</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchange">InterlockedExchange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-interlockedexchange16">InterlockedExchange16</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972654(v=vs.85)">InterlockedExchange16Acquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972655(v=vs.85)">InterlockedExchange16NoFence</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-interlockedexchange64">InterlockedExchange64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-interlockedexchange8">InterlockedExchange8</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683594(v=vs.85)">InterlockedExchangeAcquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683596(v=vs.85)">InterlockedExchangeAcquire64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchangeadd">InterlockedExchangeAdd</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972659(v=vs.85)">InterlockedExchangeNoFence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972660(v=vs.85)">InterlockedExchangeNoFence64</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683611(v=vs.85)">InterlockedExchangePointerAcquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972661(v=vs.85)">InterlockedExchangePointerNoFence</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeSubtract</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

