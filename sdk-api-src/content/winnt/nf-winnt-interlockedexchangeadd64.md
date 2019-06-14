---
UID: NF:winnt.InterlockedExchangeAdd64
title: InterlockedExchangeAdd64 function (winnt.h)
author: windows-sdk-content
description: Performs an atomic addition of two 64-bit values.
old-location: base\interlockedexchangeadd64.htm
tech.root: Sync
ms.assetid: f8cab5f8-8054-4c02-9a6d-80fd9d98cf74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InterlockedExchangeAdd64, InterlockedExchangeAdd64 function, base.interlockedexchangeadd64, winnt/InterlockedExchangeAdd64
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - InterlockedExchangeAdd64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InterlockedExchangeAdd64 function


## -description


Performs an atomic addition of two 64-bit values.

To operate on 32-bit values, use the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchangeadd">InterlockedExchangeAdd</a> function.


## -parameters




### -param Addend [in, out]

A pointer to a variable. The value of this variable will be replaced with the result of the operation.


### -param Value [in]

The value to be added to the variable pointed to by the <i>Addend</i> parameter.


## -returns



The function returns the initial value of  the <i>Addend</i> parameter.




## -remarks



The 
function performs an atomic addition of <i>Value</i> to the value pointed to by <i>Addend</i>. The result is stored in the address specified by <i>Addend</i>. The function returns the initial value of the variable pointed to by <i>Addend</i>.

The variables for this function must be aligned on a 64-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://docs.microsoft.com/previous-versions//191ca0sk(v=vs.85)">_InterlockedExchangeAdd64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683604(v=vs.85)">InterlockedExchangeAddAcquire64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Sync/interlocked-variable-access">Interlocked Variable Access</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedcompareexchange">InterlockedCompareExchange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchange">InterlockedExchange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchangeadd">InterlockedExchangeAdd</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683601(v=vs.85)">InterlockedExchangeAddAcquire</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683604(v=vs.85)">InterlockedExchangeAddAcquire64</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972657(v=vs.85)">InterlockedExchangeAddNoFence</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh972658(v=vs.85)">InterlockedExchangeAddNoFence64</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683605(v=vs.85)">InterlockedExchangeAddRelease</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms683607(v=vs.85)">InterlockedExchangeAddRelease64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedexchangesubtract">InterlockedExchangeSubtract</a>



<a href="https://docs.microsoft.com/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>
 

 

