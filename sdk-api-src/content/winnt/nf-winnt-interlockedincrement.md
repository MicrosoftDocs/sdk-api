---
UID: NF:winnt.InterlockedIncrement
title: InterlockedIncrement function
author: windows-sdk-content
description: Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.
old-location: base\interlockedincrement.htm
tech.root: Sync
ms.assetid: 87eda7fb-966d-4630-9da6-8933b53daadd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: InterlockedIncrement, InterlockedIncrement function, _win32_interlockedincrement, base.interlockedincrement, winnt/InterlockedIncrement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - InterlockedIncrement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- InterlockedIncrement
: 
---

# InterlockedIncrement function


## -description


Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.

To operate on 64-bit values, use the <a href="https://msdn.microsoft.com/f18b63fa-201f-436d-a152-41e458959a5c">InterlockedIncrement64</a> function.


## -parameters




### -param Addend [in, out]

A pointer to the variable to be incremented.


## -returns



The function returns the resulting incremented value.
     




## -remarks



The variable pointed to by the <i>Addend</i> parameter must be aligned on a 32-bit boundary; otherwise, this function will behave unpredictably on multiprocessor x86 systems and any non-x86 systems. See <b>_aligned_malloc</b>.

The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="37700615-f372-438b-bcef-d76e11839482">_InterlockedIncrement</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/d6ae8212-ae47-47cf-8787-83780ecf1d61">InterlockedIncrementAcquire</a> or <a href="https://msdn.microsoft.com/6ea906b2-0c85-4f08-b53b-61d730fa4930">InterlockedIncrementRelease</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/d6ed6cb1-aa10-48f4-9b62-73708ff4d1e3">InterlockedDecrement</a>



<a href="https://msdn.microsoft.com/93460ed0-2c2c-4686-a8ed-02669c4df214">InterlockedIncrement16</a>



<a href="https://msdn.microsoft.com/d9ecc468-6aff-4905-8308-fb2e4b482401">InterlockedIncrement16Acquire</a>



<a href="https://msdn.microsoft.com/1f780934-726f-47dd-bbfc-53e9f46a08a0">InterlockedIncrement16NoFence</a>



<a href="https://msdn.microsoft.com/52d34ef7-80e2-4e77-a9fa-791bd54e6666">InterlockedIncrement16Release</a>



<a href="https://msdn.microsoft.com/f18b63fa-201f-436d-a152-41e458959a5c">InterlockedIncrement64</a>



<a href="https://msdn.microsoft.com/d6ae8212-ae47-47cf-8787-83780ecf1d61">InterlockedIncrementAcquire</a>



<a href="https://msdn.microsoft.com/68628282-7076-4cae-af69-32fd02dbd87b">InterlockedIncrementAcquire64</a>



<a href="https://msdn.microsoft.com/17492f3a-e44c-4cd5-89d1-716954576fe0">InterlockedIncrementNoFence</a>



<a href="https://msdn.microsoft.com/63ac068a-c446-417a-acaf-e55da3d67b40">InterlockedIncrementNoFence64</a>



<a href="https://msdn.microsoft.com/6ea906b2-0c85-4f08-b53b-61d730fa4930">InterlockedIncrementRelease</a>



<a href="https://msdn.microsoft.com/2e216c4d-598a-447b-87cd-91bc1f551af3">InterlockedIncrementRelease64</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

