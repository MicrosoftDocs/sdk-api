---
UID: NF:winnt.InterlockedAdd
title: InterlockedAdd function
author: windows-driver-content
description: Performs an atomic addition operation on the specified LONG values.
old-location: base\interlockedadd.htm
old-project: Sync
ms.assetid: c3ff4c2f-ac84-4046-ac4e-600569b874be
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: InterlockedAdd, InterlockedAdd function, base.interlockedadd, winnt/InterlockedAdd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	InterlockedAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# InterlockedAdd function


## -description


Performs an atomic addition operation on the specified <b>LONG</b> values.


## -parameters




### -param Addend [in, out]

A pointer to the first operand. This value will be replaced with the result of the operation.


### -param Value [in]

The second operand.


## -returns



The function returns the result of the operation.




## -remarks



The interlocked functions provide a simple mechanism for synchronizing access to a variable that is shared by multiple threads. This function is atomic with respect to calls to other interlocked functions.

This function is implemented using a compiler intrinsic where possible. For more information, see the WinBase.h header file and <a href="3d319603-ea9c-4fdd-ae61-e52430ccc3b1">_InterlockedAdd</a>.

This function  generates a full memory barrier (or fence) to ensure that memory operations are completed in order.

<div class="alert"><b>Note</b>  This function is supported on Windows RT-based systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/729c0e68-ef52-4d6c-b771-a89043a937e6">Interlocked Variable Access</a>



<a href="https://msdn.microsoft.com/ab37292f-4291-4cca-826c-d6488e141db8">InterlockedAdd64</a>



<a href="https://msdn.microsoft.com/ec1746cc-aff9-440e-b7e1-15a3d7a0fa58">InterlockedAddAcquire</a>



<a href="https://msdn.microsoft.com/0bdce93f-a57a-40d3-a8fa-007edb8b5c6d">InterlockedAddAcquire64</a>



<a href="https://msdn.microsoft.com/98f29a64-27c9-455f-a7cf-c2c47ea512c8">InterlockedAddNoFence</a>



<a href="https://msdn.microsoft.com/f7c8c50a-805f-4963-8a5e-160776dd995e">InterlockedAddNoFence64</a>



<a href="https://msdn.microsoft.com/d09a6420-bf6c-43a7-aa7a-1cff03596afc">InterlockedAddRelease</a>



<a href="https://msdn.microsoft.com/24a88190-79e3-48bf-986e-d5d08c1bce08">InterlockedAddRelease64</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547903">InterlockedExchangeAdd</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

