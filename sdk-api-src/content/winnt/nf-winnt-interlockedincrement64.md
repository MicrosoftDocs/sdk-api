---
UID: NF:winnt.InterlockedIncrement64
title: InterlockedIncrement64 function
author: windows-sdk-content
description: Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.
old-location: base\interlockedincrement64.htm
tech.root: Sync
ms.assetid: f18b63fa-201f-436d-a152-41e458959a5c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InterlockedIncrement64, InterlockedIncrement64 function, base.interlockedincrement64, winnt/InterlockedIncrement64
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
 - InterlockedIncrement64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InterlockedIncrement64 function


## -description


Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.

To operate on 32-bit values, use the <a href="https://msdn.microsoft.com/en-us/library/ms683614(v=VS.85).aspx">InterlockedIncrement</a> function.


## -parameters




### -param Addend [in, out]

A pointer to the variable to be incremented.


## -returns



The function returns the resulting incremented value.




## -remarks



The variable pointed to by the <i>Addend</i> parameter must be aligned on a 64-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://msdn.microsoft.com/library/2ddez55b(v=VS.85).aspx">_InterlockedIncrement64</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/68628282-7076-4cae-af69-32fd02dbd87b">InterlockedIncrementAcquire64</a> or <a href="https://msdn.microsoft.com/2e216c4d-598a-447b-87cd-91bc1f551af3">InterlockedIncrementRelease64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683580(v=VS.85).aspx">InterlockedDecrement</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683614(v=VS.85).aspx">InterlockedIncrement</a>



<a href="https://msdn.microsoft.com/93460ed0-2c2c-4686-a8ed-02669c4df214">InterlockedIncrement16</a>



<a href="https://msdn.microsoft.com/d9ecc468-6aff-4905-8308-fb2e4b482401">InterlockedIncrement16Acquire</a>



<a href="https://msdn.microsoft.com/1f780934-726f-47dd-bbfc-53e9f46a08a0">InterlockedIncrement16NoFence</a>



<a href="https://msdn.microsoft.com/52d34ef7-80e2-4e77-a9fa-791bd54e6666">InterlockedIncrement16Release</a>



<a href="https://msdn.microsoft.com/d6ae8212-ae47-47cf-8787-83780ecf1d61">InterlockedIncrementAcquire</a>



<a href="https://msdn.microsoft.com/68628282-7076-4cae-af69-32fd02dbd87b">InterlockedIncrementAcquire64</a>



<a href="https://msdn.microsoft.com/17492f3a-e44c-4cd5-89d1-716954576fe0">InterlockedIncrementNoFence</a>



<a href="https://msdn.microsoft.com/63ac068a-c446-417a-acaf-e55da3d67b40">InterlockedIncrementNoFence64</a>



<a href="https://msdn.microsoft.com/6ea906b2-0c85-4f08-b53b-61d730fa4930">InterlockedIncrementRelease</a>



<a href="https://msdn.microsoft.com/2e216c4d-598a-447b-87cd-91bc1f551af3">InterlockedIncrementRelease64</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

