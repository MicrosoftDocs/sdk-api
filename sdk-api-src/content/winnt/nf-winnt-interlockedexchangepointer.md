---
UID: NF:winnt.InterlockedExchangePointer
title: InterlockedExchangePointer function
author: windows-sdk-content
description: Atomically exchanges a pair of addresses.
old-location: base\interlockedexchangepointer.htm
tech.root: Sync
ms.assetid: 479aede8-e9e3-42c2-9081-94c150c7f274
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: InterlockedExchangePointer, InterlockedExchangePointer function, _win32_interlockedexchangepointer, base.interlockedexchangepointer, winnt/InterlockedExchangePointer
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

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="https://msdn.microsoft.com/library/853x471w(v=VS.85).aspx">_InterlockedExchangePointer</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/a949fce4-ab18-4702-9324-0912c9b56bf5">InterlockedExchangePointerAcquire</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/c0da780c-5fd0-4c88-a283-8d057db812ac">InterlockedCompareExchange</a>



<a href="https://msdn.microsoft.com/22142195-b592-4a7b-9b23-e31984cc1d41">InterlockedExchange</a>



<a href="https://msdn.microsoft.com/06756ec6-9c1c-4aac-99de-c45186c89af1">InterlockedExchange16</a>



<a href="https://msdn.microsoft.com/647ca78a-0dee-4312-8911-4b5167d73d7e">InterlockedExchange16Acquire</a>



<a href="https://msdn.microsoft.com/d0a2a934-067b-4aa8-99d1-15647d977684">InterlockedExchange16NoFence</a>



<a href="https://msdn.microsoft.com/80d34f5d-3491-4653-959b-6b9efebf764b">InterlockedExchange64</a>



<a href="https://msdn.microsoft.com/fe07fac0-b9f2-419e-a086-09bc73125c4e">InterlockedExchange8</a>



<a href="https://msdn.microsoft.com/985dd245-ac9e-4a47-b819-5a9fb7852885">InterlockedExchangeAcquire</a>



<a href="https://msdn.microsoft.com/30df63a3-bd28-430b-ab30-057bbd03f9e4">InterlockedExchangeAcquire64</a>



<a href="https://msdn.microsoft.com/e48b67a0-133b-4e88-b451-432f26b4881a">InterlockedExchangeAdd</a>



<a href="https://msdn.microsoft.com/92075e5b-4461-4d18-8936-9e98419553a9">InterlockedExchangeNoFence</a>



<a href="https://msdn.microsoft.com/c624e317-7904-4603-90fb-b436742a79b9">InterlockedExchangeNoFence64</a>



<a href="https://msdn.microsoft.com/a949fce4-ab18-4702-9324-0912c9b56bf5">InterlockedExchangePointerAcquire</a>



<a href="https://msdn.microsoft.com/d8158b7f-f420-4cb0-8ada-dcdd282e4d7e">InterlockedExchangePointerNoFence</a>



<a href="https://msdn.microsoft.com/9917323D-38C4-446E-B59A-52493A6020ED">InterlockedExchangeSubtract</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

