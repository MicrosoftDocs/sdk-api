---
UID: NF:winnt.InterlockedExchangeAdd64
title: InterlockedExchangeAdd64 function
author: windows-sdk-content
description: Performs an atomic addition of two 64-bit values.
old-location: base\interlockedexchangeadd64.htm
tech.root: sync
ms.assetid: f8cab5f8-8054-4c02-9a6d-80fd9d98cf74
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InterlockedExchangeAdd64, InterlockedExchangeAdd64 function, base.interlockedexchangeadd64, winnt/InterlockedExchangeAdd64
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# InterlockedExchangeAdd64 function


## -description


Performs an atomic addition of two 64-bit values.

To operate on 32-bit values, use the <a href="https://msdn.microsoft.com/e48b67a0-133b-4e88-b451-432f26b4881a">InterlockedExchangeAdd</a> function.


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

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://msdn.microsoft.com/library/191ca0sk(v=VS.85).aspx">_InterlockedExchangeAdd64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/a22e9ce8-1fe6-40ac-a65d-1177fbf2bfe4">InterlockedExchangeAddAcquire64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/c0da780c-5fd0-4c88-a283-8d057db812ac">InterlockedCompareExchange</a>



<a href="https://msdn.microsoft.com/22142195-b592-4a7b-9b23-e31984cc1d41">InterlockedExchange</a>



<a href="https://msdn.microsoft.com/e48b67a0-133b-4e88-b451-432f26b4881a">InterlockedExchangeAdd</a>



<a href="https://msdn.microsoft.com/920daad7-7c47-4e55-8aba-db63cf285d12">InterlockedExchangeAddAcquire</a>



<a href="https://msdn.microsoft.com/a22e9ce8-1fe6-40ac-a65d-1177fbf2bfe4">InterlockedExchangeAddAcquire64</a>



<a href="https://msdn.microsoft.com/68114e68-3ca9-4214-862e-4ba51d597b92">InterlockedExchangeAddNoFence</a>



<a href="https://msdn.microsoft.com/bd16406a-0740-45b8-ad15-bb5b183671d7">InterlockedExchangeAddNoFence64</a>



<a href="https://msdn.microsoft.com/bcc74dcf-2851-41ec-8497-dd4c05bb6a26">InterlockedExchangeAddRelease</a>



<a href="https://msdn.microsoft.com/7ab76bbb-25e1-4412-920c-f1f85f22da9b">InterlockedExchangeAddRelease64</a>



<a href="https://msdn.microsoft.com/9917323D-38C4-446E-B59A-52493A6020ED">InterlockedExchangeSubtract</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

