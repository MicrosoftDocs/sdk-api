---
UID: NF:winnt.InterlockedExchange
title: InterlockedExchange function
author: windows-sdk-content
description: Sets a 32-bit variable to the specified value as an atomic operation.
old-location: base\interlockedexchange.htm
old-project: sync
ms.assetid: 22142195-b592-4a7b-9b23-e31984cc1d41
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InterlockedExchange, InterlockedExchange function, _win32_interlockedexchange, base.interlockedexchange, winnt/InterlockedExchange
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRANSACTION_OUTCOME
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# InterlockedExchange function


## -description


Sets a 32-bit variable to the specified value as an atomic operation.

To operate on a pointer variable, use the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff547904">InterlockedExchangePointer</a> function.

To operate on a 16-bit variable, use the <a href="https://msdn.microsoft.com/06756ec6-9c1c-4aac-99de-c45186c89af1">InterlockedExchange16</a> function.

To operate on a 64-bit variable, use the <a href="https://msdn.microsoft.com/80d34f5d-3491-4653-959b-6b9efebf764b">InterlockedExchange64</a> function.


## -parameters




### -param Target [in, out]

A pointer to the value to be exchanged. The function sets this variable to <i>Value</i>, and returns its prior value.


### -param Value [in]

The value to be exchanged with the value pointed to by <i>Target</i>.


## -returns



The function returns the initial value of the <i>Target</i> parameter.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="be2f232a-6301-462a-a92b-fcdeb8b0f209">_InterlockedExchange</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<b>Itanium-based systems:  </b>For performance-critical applications, use <a href="https://msdn.microsoft.com/985dd245-ac9e-4a47-b819-5a9fb7852885">InterlockedExchangeAcquire</a> instead.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547853">InterlockedCompareExchange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547892">InterlockedExchange</a>



<a href="https://msdn.microsoft.com/06756ec6-9c1c-4aac-99de-c45186c89af1">InterlockedExchange16</a>



<a href="https://msdn.microsoft.com/647ca78a-0dee-4312-8911-4b5167d73d7e">InterlockedExchange16Acquire</a>



<a href="https://msdn.microsoft.com/d0a2a934-067b-4aa8-99d1-15647d977684">InterlockedExchange16NoFence</a>



<a href="https://msdn.microsoft.com/80d34f5d-3491-4653-959b-6b9efebf764b">InterlockedExchange64</a>



<a href="https://msdn.microsoft.com/fe07fac0-b9f2-419e-a086-09bc73125c4e">InterlockedExchange8</a>



<a href="https://msdn.microsoft.com/985dd245-ac9e-4a47-b819-5a9fb7852885">InterlockedExchangeAcquire</a>



<a href="https://msdn.microsoft.com/30df63a3-bd28-430b-ab30-057bbd03f9e4">InterlockedExchangeAcquire64</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547903">InterlockedExchangeAdd</a>



<a href="https://msdn.microsoft.com/f8cab5f8-8054-4c02-9a6d-80fd9d98cf74">InterlockedExchangeAdd64</a>



<a href="https://msdn.microsoft.com/920daad7-7c47-4e55-8aba-db63cf285d12">InterlockedExchangeAddAcquire</a>



<a href="https://msdn.microsoft.com/a22e9ce8-1fe6-40ac-a65d-1177fbf2bfe4">InterlockedExchangeAddAcquire64</a>



<a href="https://msdn.microsoft.com/68114e68-3ca9-4214-862e-4ba51d597b92">InterlockedExchangeAddNoFence</a>



<a href="https://msdn.microsoft.com/bd16406a-0740-45b8-ad15-bb5b183671d7">InterlockedExchangeAddNoFence64</a>



<a href="https://msdn.microsoft.com/bcc74dcf-2851-41ec-8497-dd4c05bb6a26">InterlockedExchangeAddRelease</a>



<a href="https://msdn.microsoft.com/7ab76bbb-25e1-4412-920c-f1f85f22da9b">InterlockedExchangeAddRelease64</a>



<a href="https://msdn.microsoft.com/92075e5b-4461-4d18-8936-9e98419553a9">InterlockedExchangeNoFence</a>



<a href="https://msdn.microsoft.com/c624e317-7904-4603-90fb-b436742a79b9">InterlockedExchangeNoFence64</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547904">InterlockedExchangePointer</a>



<a href="https://msdn.microsoft.com/a949fce4-ab18-4702-9324-0912c9b56bf5">InterlockedExchangePointerAcquire</a>



<a href="https://msdn.microsoft.com/d8158b7f-f420-4cb0-8ada-dcdd282e4d7e">InterlockedExchangePointerNoFence</a>



<a href="https://msdn.microsoft.com/9917323D-38C4-446E-B59A-52493A6020ED">InterlockedExchangeSubtract</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

