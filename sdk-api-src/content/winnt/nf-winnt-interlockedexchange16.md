---
UID: NF:winnt.InterlockedExchange16
title: InterlockedExchange16 function
author: windows-sdk-content
description: Sets a 16-bit variable to the specified value as an atomic operation.
old-location: base\interlockedexchange16.htm
tech.root: sync
ms.assetid: 06756ec6-9c1c-4aac-99de-c45186c89af1
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: InterlockedExchange16, InterlockedExchange16 function, base.interlockedexchange16, winnt/InterlockedExchange16
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
 - InterlockedExchange16
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InterlockedExchange16 function


## -description


Sets a 16-bit variable to the specified value as an atomic operation.

To operate on a 32-bit variable, use the <a href="https://msdn.microsoft.com/22142195-b592-4a7b-9b23-e31984cc1d41">InterlockedExchange</a> function.

To operate on a 64-bit variable, use the <a href="https://msdn.microsoft.com/80d34f5d-3491-4653-959b-6b9efebf764b">InterlockedExchange64</a> function.


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

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/30df63a3-bd28-430b-ab30-057bbd03f9e4">InterlockedExchangeAcquire64</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/c0da780c-5fd0-4c88-a283-8d057db812ac">InterlockedCompareExchange</a>



<a href="https://msdn.microsoft.com/22142195-b592-4a7b-9b23-e31984cc1d41">InterlockedExchange</a>



<a href="https://msdn.microsoft.com/647ca78a-0dee-4312-8911-4b5167d73d7e">InterlockedExchange16Acquire</a>



<a href="https://msdn.microsoft.com/d0a2a934-067b-4aa8-99d1-15647d977684">InterlockedExchange16NoFence</a>



<a href="https://msdn.microsoft.com/80d34f5d-3491-4653-959b-6b9efebf764b">InterlockedExchange64</a>



<a href="https://msdn.microsoft.com/fe07fac0-b9f2-419e-a086-09bc73125c4e">InterlockedExchange8</a>



<a href="https://msdn.microsoft.com/985dd245-ac9e-4a47-b819-5a9fb7852885">InterlockedExchangeAcquire</a>



<a href="https://msdn.microsoft.com/30df63a3-bd28-430b-ab30-057bbd03f9e4">InterlockedExchangeAcquire64</a>



<a href="https://msdn.microsoft.com/e48b67a0-133b-4e88-b451-432f26b4881a">InterlockedExchangeAdd</a>



<a href="https://msdn.microsoft.com/92075e5b-4461-4d18-8936-9e98419553a9">InterlockedExchangeNoFence</a>



<a href="https://msdn.microsoft.com/c624e317-7904-4603-90fb-b436742a79b9">InterlockedExchangeNoFence64</a>



<a href="https://msdn.microsoft.com/479aede8-e9e3-42c2-9081-94c150c7f274">InterlockedExchangePointer</a>



<a href="https://msdn.microsoft.com/a949fce4-ab18-4702-9324-0912c9b56bf5">InterlockedExchangePointerAcquire</a>



<a href="https://msdn.microsoft.com/d8158b7f-f420-4cb0-8ada-dcdd282e4d7e">InterlockedExchangePointerNoFence</a>



<a href="https://msdn.microsoft.com/9917323D-38C4-446E-B59A-52493A6020ED">InterlockedExchangeSubtract</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

